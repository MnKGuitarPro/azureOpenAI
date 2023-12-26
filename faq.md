# ❓ FAQ ❓

A continuación se detallan algunas de las preguntas/respuestas más frecuentes

---

## 📚 FAQ - Uso de archivos/documentos 📄

### 1. **¿Cuáles formatos son aceptados por el chatGPT?**
  **Respuesta**: \
  Los formatos de archivos y documentos aceptados por chatGPT Bci están definidos por el servicio encargado de realizar la tarea de OCR (Optical Character Recognition, o 'reconocimiento óptico de caracteres'). \
  En nuestro caso, el servicio de OCR utilizado se llama **Document Intelligence** y de momento Microsoft (quien mantiene el servicio) tiene declarados [en su documentación oficial](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/concept-read?view=doc-intel-4.0.0#input-requirements) **once tipos** de formatos de archivos, los cuales son:
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
    4. HTML (documentos de tipo Web) \

### 2. **¿Cómo puedo chatear utilizando uno o varios documentos?**
**Respuesta**: \
Primero, al iniciar un nuevo chat se debe dar clic a la opción "Archivo" y seleccionar un archivo dando clic a la sección que dice "Elegir archivo" donde, una vez seleccionado, se debe dar clic al botón que dice "Subir" \
![](https://raw.githubusercontent.com/MnKGuitarPro/azureOpenAI/main/img/chat001.png) \
Se mostrará el progreso del procesamiento del archivo en dos etapas, la primera corresponde a **subir** el archivo y la segunda corresponde a **indexar** al archivo (procesarlo, en otras palabras). La primer etapa (subir el archivo) se muestra en un mensaje de estado que dice "Subiendo documento...", como se muestra en la siguiente imagen \
![](https://github.com/MnKGuitarPro/azureOpenAI/blob/main/img/chat002.png?raw=true) \
Respecto de la segunda etapa (indexar el archivo, o dicho de otro modo, procesar el archivo), también se muestra un mensaje de estado que dice "Indexando archivo [X]/[Y]" donde `X` indica el fragmento que se está subiendo en ese momento y `Y` el total de fragmentos o partes que se deben subir \
![](https://github.com/MnKGuitarPro/azureOpenAI/blob/main/img/chat003.png?raw=true) \
Cuando `X` alcanza el valor de `Y` significa que el archivo ha sido indexado (procesado) en su totalidad y que, por tanto, el archivo se ha subido completamente. Cuando ocurre ese hito aparecerá un mensaje de éxito en la esquina inferior derecha que dice "Subida de archivo 'nombre-de-archivo' subido exitosamente." \
![](https://github.com/MnKGuitarPro/azureOpenAI/blob/main/img/chat004.png?raw=true) \
Con esto, ya podemos chatear usando como base de conocimiento el contenido del archivo que acabamos de subir. Sólo debemos interactuar en el campo de texto de la parte inferior que dice "Escribe un mensaje" y comenzaremos un hilo de conversación. Cabe mencionar que este tipo de interacciones es muy directa por lo que si nuestro mensaje no tiene relación o sus palabras no se mencionan en ninguna sección del documento subido, es probable que el chat responda indicando que no tiene contexto. Un tip es comenzar la conversación solicitando un resumen del contenido, lo que hará el chat comience una conversación coherente. Durante el proceso de generación de texto verán que en determinado momento el chat escribe algo como `{% citation items=[{name:"filename 1",id:"file id"}, {name:"filename 2",id:"file id"}] /%}`, no hay que preocuparse, es sólo la generación de botones que les permitirán ir a las secciones específicas que el chat utilizó para responder las preguntas o interacciones que nosotros tengamos (citas directas del documento que hemos subido) \
![](https://github.com/MnKGuitarPro/azureOpenAI/blob/main/img/chat005.png?raw=true) \
![](https://github.com/MnKGuitarPro/azureOpenAI/blob/main/img/chat006.png?raw=true) \
Una feature que se agregó es la de poder utilizar varios documentos para con ellos formar un único contexto que nuestro chat puede utilizar como base de sus respuestas. Para agregar un nuevo documento al hilo que ya tenemos creado, sólo se debe dar clic al ícono de 📄 que se encuentra al lado izquierdo del campo que utilizamos para escribir nuestros mensajes \
![](https://github.com/MnKGuitarPro/azureOpenAI/blob/main/img/chat007.png?raw=true) \
Al dar clic al ícono para agregar más documentos, se abrirá un panel al lado derecho que nos permitirá agregar más documentos (muy similar al del inicio de la conversación con un archivo). En este menú también se muestran mensajes de los estados de subida e indexación (o procesamiento) del archivo y, una vez el archivo ha sido completamente indexado, podemos subir más archivos hasta completar el contexto que necesitemos \
![](https://github.com/MnKGuitarPro/azureOpenAI/blob/main/img/chat008.png?raw=true) \

### 3. **¿Es seguro subir documentos a este chat?**
**Respuesta**: \
Sí. A diferencia del "chatgpt" público [que se accede a través de Internet](https://chat.openai.com/) y que tenemos bloqueado internamente, esta versión es privada y utiliza servicios que se encuentran en nuestra infraestructura tecnológica. Por lo tanto, es seguro utilizar esta versión de chat para conversar en base al contenido de documentos incluso cuando ese contenido es de índole privado. \
Una característica importante de mencionar es que el contexto de conversación que un usuario tenga con chatGPT Bci no se puede compartir con otro usuario. Por ende, si la usuaria 'María González' sube un archivo cuyo contenido tiene relación a 'cómo hacer violines' y 'Juan Pérez' consulta al chatGPT Bci '¿cómo puedo hacer un violín?' no se utilizará el contenido subido por 'María González', ya que ese contenido es sólo accesible por el hilo de conversación que ella ha creado. \ 
Es posible que un usuario quiera la característica o funcionalidad de tener "contextos compartidos" o sea, que un usuario pueda conversar con el contenido o contexto que otro usuario tiene o ha creado. Esta funcionalidad puede permitir que dos usuarios no tengan que subir el mismo documento dos veces, o poder tener acceso colaborativo a una conversación enriquecida por la interacción entre dos o más usuarios. Sin embargo, esa funcionalidad o característica pasa por alto la privacidad, y para el caso de chatGPT Bci la privacidad y seguridad de las conversaciones que los usuarios tengan es fundamental. Dado lo anterior, no se implementarán funcionalidades de contextos compartidos y estos seguirán siendo privados \

---

## 👥 FAQ - Subir usuarios al chatGPT 👨🏻‍💻

### 1. **¿Cómo me puedo agregar a mí o a alguien más al piloto?**
**Respuesta**: \
Para agregar a alguien más al chat, sólo le debes pedir (o en su defecto, explicar) que siga los pasos descritos [en el siguiente documento de Confluence](https://bcibank.atlassian.net/wiki/spaces/AT/pages/3950773388). \
Si tienes alguna duda, puedes contactar a [Daniel Pavez Sandoval vía chat de Google](https://mail.google.com/mail/u/0/#chat/home) o bien [vía Slack](https://bci.enterprise.slack.com/archives/D01QV5BP8PN) \

---

## 💡 FAQ - Alcance del chatGPT interno 🎨

### 1. **¿Se integrará esta solución a otros sistemas, como un agente o una extensión?**
**Respuesta**: \
No. Se debe tener claro que el **caso de uso** que resuelve el presente chat está conformado por dos funcionalidades principales:
1. Poder chatear contra un modelo de GPT-4 usando la base de contexto de Microsoft (detalles de hasta cuando está actualizada [en el siguiente enlace](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/models#gpt-4-and-gpt-4-turbo-preview-models), nosotros estamos utilizando la versión `gpt-4-32k (0613)` que está actualizada hasta Septiembre del 2021, pero a penas tengamos acceso al modelo `gpt-4 (1106)` que está actualizado hasta abril del 2023, lo anunciaremos en la sección de [Novedades](https://chatgpt.bci.cl/change-log))
2. Poder chatear contra un [modelo de Embeddings](https://learn.microsoft.com/en-us/azure/ai-services/openai/tutorials/embeddings), lo que permite chatear usando como base el contexto provisto por archivos o documentos que un usuario sube al chatGPT Bci \
\
Otros casos de uso distintos a los mencionados, como por ejemplo integrar esta solución con otras, implementar agentes o bots, o que este chat realice cualquier acción distinta a las dos anteriormente mencionadas se debe implementar como una 
solución que satisfaga a dicho caso de uso de forma específica. Lo anterior no implica que chatGPT Bci no seguirá evolucionando, teniendo mejoras o nuevas funcionalidades o características, pero se debe considerar que siempre estas mejoras estarán relacionadas a satisfacer el caso de uso descrito en los dos puntos anteriores \
