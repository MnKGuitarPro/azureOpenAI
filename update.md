# chatGPT Bci

¡Hemos actualizado nuestra plataforma! A continuación encontrarás las novedades implementadas

## 🎉 Novedades 🎉

### 📂 Chatear con el contenido de un archivo 📚

- ¿Alguna vez intentaste subir con un archivo y recibiste un error? Se realizaron varios fixes a problemas generados al intentar chatear contra un archivo grande (superior a 20 páginas, por ejemplo) a la vez que se incorporó un estado de la subida del archivo para que no pierdas de vista el estado del proceso
- Se agregó una funcionalidad nueva que muestra una cita de dónde fue extraído el contenido que ha alimentado la respuesta que has recibido de parte del chat, de esta forma puedes evaluar el nivel de "alucinación" del modelo GPT para con una respuesta generada
- Ahora hemos agregado la facultad de subir múltiples archivos a hilos de conversación existentes, de esta manera podrás chatear contra el contenido de múltiples archivos de forma simultánea

<!---
### 🔑 Environment variable change

Please note that the solution has been upgraded to utilise the most recent version of the OpenAI JavaScript SDK, necessitating the use of the `OPENAI_API_KEY` environment variable.

Ensure that you update the variable name in both your '.env' file and the configuration within Azure App Service or Key Vault, changing it from `AZURE_OPENAI_API_KEY` to `OPENAI_API_KEY`.
-->

## 🚧 Estamos trabajando 🚧

## 🎙️ Speech

- Estamos trabajando en la capacidad de trabajar con Azure Speech, que es el servicio que permite utilizar tu micrófono para interactuar con el chatGPT Bci utilizando tu voz. ¡Quédate atent@ a esta página para que te enteres de la liberación de esta funcionalidad!

<!---
Ability to use Azure Speech in conversations. This feature is not enabled by default. To enable this feature, you must set the environment variable `PUBLIC_SPEECH_ENABLED=true` along with the Azure Speech subscription key and region.

```
PUBLIC_SPEECH_ENABLED=true
AZURE_SPEECH_REGION="REGION"
AZURE_SPEECH_KEY="1234...."
```
-->
