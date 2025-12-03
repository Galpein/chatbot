# Chatbot Agencia de Viajes

Asistente virtual para agencia de viajes con integración de Google Gemini AI.

## 🚀 Características

- Chatbot interactivo con IA (Google Gemini)
- Visualización de manual técnico operativo
- Diseño responsive (móvil y desktop)
- Interfaz moderna con Tailwind CSS
- React embebido sin necesidad de build

## 📋 Requisitos

- Una API Key de Google Gemini (obtener en [Google AI Studio](https://makersuite.google.com/app/apikey))

## 🔧 Configuración

1. Abre el archivo `index.html`
2. Busca la línea que dice: `const apiKey = "";`
3. Añade tu API Key de Google Gemini entre las comillas:
   ```javascript
   const apiKey = "TU_API_KEY_AQUI";
   ```

## 🌐 Despliegue en Vercel

1. Sube este proyecto a GitHub
2. Ve a [Vercel](https://vercel.com)
3. Importa tu repositorio de GitHub
4. Vercel detectará automáticamente el proyecto y lo desplegará
5. ¡Listo! Tu chatbot estará en línea

## 📝 Notas

- El archivo `index.html` es el punto de entrada principal
- No necesitas instalar dependencias (todo se carga desde CDN)
- El proyecto está listo para desplegarse directamente en Vercel

## 🔒 Seguridad

⚠️ **IMPORTANTE**: No subas tu API Key a GitHub. Si necesitas usar variables de entorno en Vercel:

1. Ve a la configuración de tu proyecto en Vercel
2. Añade una variable de entorno llamada `GEMINI_API_KEY`
3. Modifica el código para leerla desde `process.env.GEMINI_API_KEY` (requiere un pequeño ajuste)

