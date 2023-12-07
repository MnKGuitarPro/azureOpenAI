# ❓ FAQ ❓

A continuación se detallan algunas de las preguntas/respuestas más frecuentes

## 📚 FAQ - Uso de archivos/documentos 📄

1. **¿Cuáles formatos son aceptados por el chatGPT?** \
  \
  **Respuesta**: \
  Los formatos de archivos aceptados por el chatGPT están definidos por el servicio encargado de realizar la tarea de OCR (Optical Character Recognition). \
  En nuestro caso, el servicio de OCR que chatGPT está utilizando se llama **Document Intelligence** y de momento Microsoft (quien mantiene el servicio) tiene declarados [en su documentación oficial](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/concept-read?view=doc-intel-4.0.0#input-requirements) **once tipos** de archivos, los cuales son:
    1. Para documentos
        1. PDF
    2. Para formatos de tipo imagen
        1. JPEG
        2. JPG
        3. PNG
        4. BMP
        5. TIFF
        6. HEIF
    3. Para formatos de documentos de Microsoft Office
        1. DOCX (documentos de tipo Word)
        2. XLSX (documentos de tipo Excel)
        3. PPTX (documentos de tipo Power Point)
        4. HTML (documentos de tipo Web)

## 👥 FAQ - Subir usuarios al chatGPT 👨🏻‍💻

1. **¿Cómo me puedo agregar a mí o a alguien más al piloto?** \
  \
  **Respuesta**: \
  Para agregar a alguien más al chat, sólo le debes pedir (o en su defecto, explicar) que siga los pasos descritos [en el siguiente documento de Confluence](https://bcibank.atlassian.net/wiki/spaces/AT/pages/3950773388)

## 💡 FAQ - Alcance del chatGPT interno 🎨

1. **¿Se integrará esta solución a otros sistemas, como un agente?** \
  \
  **Respuesta**: \
  No. Se debe tener muy en claro que el **caso de uso** que resuelve el presente chat está conformado por dos partes principales:
    1. Poder chatear contra un modelo de GPT-4 usando la base de conocimiento de Microsoft (detalles de hasta cuando está actualizada [en el siguiente enlace](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/models#gpt-4-and-gpt-4-turbo-preview-models))
    2. Poder chatear contra un [modelo de Embeddings](https://learn.microsoft.com/en-us/azure/ai-services/openai/tutorials/embeddings), lo que permite chatear usando como base el contexto provisto por archivos o documentos
  \
  Otros casos de uso distintos a los mencionados, como por ejemplo integrar esta solución con otras, implementar agentes o bots, o que este chat realice cualquier acción distinta a las dos anteriormente mencionadas se debe implementar como una 
  solución que satisfaga a dicho caso de uso. Lo anterior no implica que este chat siga evolucionando y teniendo mejoras o nuevas features, pero siempre esas mejoras estarán relacionadas a satisfacer el caso de uso descrito en los dos puntos 
  anteriores
