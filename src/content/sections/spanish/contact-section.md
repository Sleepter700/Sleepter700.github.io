---
enable: true # Controla la visibilidad de esta sección en todas las páginas donde se utiliza
title: "¿Tiene algún proyecto en mente?"
description: "¡Genial! Estamos emocionados de escucharte y empezar algo nuevo."

# image: "/images/about-us/about-one.jpg"
# imagePosition: "left" # Elige entre "left" (izquierda) o "right" (derecha)

map:
  enable: true
  position: "right" # Elige entre "left" o "right"
  title: "Mapa de la Ciudad"
  url: https://maps.google.com/maps?width=100%25&height=600&hl=en&q=1%20Grafton%20Street,%20Dublin,%20Ireland+(My%20Business%20Name)&t=&z=14&ie=UTF8&iwloc=B&output=embed # URL del iframe del mapa

# contactInformation:
#   - title: "Sede Principal"
#     icon: "/images/icons/svg/location-filled.svg"
#     description: "27 Division St, New York, NY 10002, USA"
#     button:
#       enable: true
#       label: "Cómo llegar"
#       url: "/"
#
#   - title: "Correo Electrónico"
#     icon: "/images/icons/svg/message-filled.svg"
#     description: |
#       folex.agency@mail.com
#       folex.agency@support.com
#     button:
#       enable: true
#       label: "Enviar Mensaje"
#       url: "mailto:folex.agency@mail.com"
#
#   - title: "Número de Teléfono"
#     icon: "/images/icons/svg/phone-filled.svg"
#     description: |
#       +1 800 123 654 987
#       +1 800 223 984 002
#     button:
#       enable: true
#       label: "Llamar ahora"
#       url: "tel:+1800123654987"

# Consulta el archivo config.toml para los ajustes relacionados con la acción del formulario
form:
  emailSubject: "Nuevo envío de formulario desde el sitio web de Folex" # Asunto del correo personalizado
  submitButton:
    enable: true
    label: "ENVIAR MENSAJE"

  # Esta nota aparecerá al final del formulario
  # note: |
  #   Sus datos están seguros con nosotros. Respetamos su privacidad y nunca compartimos su información. <br /> Lea nuestra [Política de Privacidad](/privacy-policy/).
  
  inputs:
    - label: ""
      placeholder: "Nombre completo *"
      name: "Nombre Completo" # Importante: nombre bajo el cual recibirás este campo
      required: true
      halfWidth: true
      defaultValue: ""
    - label: ""
      placeholder: "Correo electrónico *"
      name: "Correo Electrónico"
      required: true
      type: "email"
      halfWidth: true
      defaultValue: ""
    - label: ""
      placeholder: "Asunto *"
      name: "Asunto"
      required: false
      halfWidth: true
      dropdown:
        type: "" # select | search
        items:
          - label: "Consulta General"
            value: "Consulta General"
            selected: false
          - label: "Oportunidad de Asociación"
            value: "Oportunidad de Asociación"
            selected: false
          - label: "Oportunidad de Inversión"
            value: "Oportunidad de Inversión"
            selected: false
    - label: ""
      placeholder: "Asunto con búsqueda *"
      name: "Asunto con búsqueda"
      required: false
      halfWidth: true
      dropdown:
        type: "search"
        search:
          placeholder: "Buscar asunto"
        items:
          - label: "Consulta General"
            value: "General Inquiry"
            selected: false
          - label: "Oportunidad de Asociación"
            value: "Partnership Opportunity"
            selected: false
          - label: "Oportunidad de Carrera"
            value: "Career Opportunity"
            selected: false
          - label: "Oportunidad de Inversión"
            value: "Investment Opportunity"
            selected: false
          - label: "Consulta de Medios"
            value: "Media Inquiry"
            selected: false
    - label: ""
      tag: "textarea"
      defaultValue: ""
      rows: "2"
      placeholder: "¿Cómo podemos ayudarte? *"
      name: "Mensaje"
      required: true
      halfWidth: false
    - label: "Búsqueda en Google"
      checked: false
      name: "Origen del Usuario"
      required: true
      groupLabel: "¿Cómo se enteró de nosotros?" # Etiqueta del grupo de Radio Inputs
      group: "source"
      type: "radio"
      halfWidth: true
      defaultValue: ""
    - label: "Redes Sociales"
      name: "Origen del Usuario"
      required: true
      groupLabel: ""
      group: "source"
      type: "radio"
      halfWidth: true
      defaultValue: ""
    - label: "Acepto los términos y condiciones y la [política de privacidad](/)."
      id: "privacy-policy"
      name: "Privacidad Aceptada"
      value: "Aceptado"
      checked: false
      required: true
      type: "checkbox"
      halfWidth: false
      defaultValue: ""
    - note: success
      parentClass: "hidden text-sm message success"
      content: "¡Hemos recibido su mensaje! Nos pondremos en contacto con usted lo antes posible."
    - note: deprecated
      parentClass: "hidden text-sm message error"
      content: "¡Algo salió mal! Por favor, use este correo - [folex-astro-theme@gmail.com](mailto:folex-astro-theme@gmail.com) para enviar un ticket."
---
