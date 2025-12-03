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

**URL de despliegue:** https://chatbot-gules-eta-69.vercel.app/

## 🔗 Integrar en tu sitio web (iframe)

Para insertar el chatbot en tu sitio web, usa este código iframe:

### Opción 1: Iframe básico (recomendado)
```html
<iframe 
    src="https://chatbot-gules-eta-69.vercel.app/" 
    width="100%" 
    height="600" 
    frameborder="0"
    allow="clipboard-read; clipboard-write"
    style="border: none; border-radius: 8px;">
</iframe>
```

### Opción 2: Iframe responsive
```html
<div style="position: relative; width: 100%; height: 0; padding-bottom: 75%;">
    <iframe 
        src="https://chatbot-gules-eta-69.vercel.app/" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none; border-radius: 8px;"
        allow="clipboard-read; clipboard-write">
    </iframe>
</div>
```

### Opción 3: Iframe flotante (botón de chat)
```html
<!-- Botón flotante -->
<button onclick="document.getElementById('chatbot-iframe').style.display='block'" 
        style="position: fixed; bottom: 20px; right: 20px; background: #2563eb; color: white; border: none; padding: 15px 20px; border-radius: 50px; cursor: pointer; box-shadow: 0 4px 6px rgba(0,0,0,0.3); z-index: 1000;">
    💬 Chat
</button>

<!-- Iframe oculto inicialmente -->
<div id="chatbot-iframe" style="display: none; position: fixed; bottom: 80px; right: 20px; width: 400px; height: 600px; z-index: 999; box-shadow: 0 10px 25px rgba(0,0,0,0.3); border-radius: 8px; overflow: hidden;">
    <div style="background: #2563eb; color: white; padding: 10px; display: flex; justify-content: space-between; align-items: center;">
        <span>Asistente Virtual</span>
        <button onclick="document.getElementById('chatbot-iframe').style.display='none'" 
                style="background: transparent; border: none; color: white; cursor: pointer; font-size: 20px;">×</button>
    </div>
    <iframe 
        src="https://chatbot-gules-eta-69.vercel.app/" 
        width="100%" 
        height="calc(100% - 40px)" 
        frameborder="0"
        allow="clipboard-read; clipboard-write"
        style="border: none;">
    </iframe>
</div>
```

📄 **Ver más ejemplos:** Abre el archivo `iframe-example.html` para ver todas las opciones con preview en vivo.

## 📝 Notas

- El archivo `index.html` es el punto de entrada principal
- No necesitas instalar dependencias (todo se carga desde CDN)
- El proyecto está listo para desplegarse directamente en Vercel

## 🔒 Seguridad

⚠️ **IMPORTANTE**: No subas tu API Key a GitHub. Si necesitas usar variables de entorno en Vercel:

1. Ve a la configuración de tu proyecto en Vercel
2. Añade una variable de entorno llamada `GEMINI_API_KEY`
3. Modifica el código para leerla desde `process.env.GEMINI_API_KEY` (requiere un pequeño ajuste)
