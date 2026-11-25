# VOID BOT Dashboard (Vercel)

Esta carpeta contiene solo la **página/panel** para desplegar en Vercel desde GitHub. El bot y la API deben estar corriendo en Holy Hosting (u otro host).

## Despliegue en Vercel
1. Sube esta carpeta a un repositorio de GitHub.
2. En Vercel, importa el repo como proyecto estático.
3. No requiere build command. Output/public directory: raíz del repo.

## Conectar con el bot
El panel necesita la URL de la API del bot. Tienes 3 opciones:
- En la pantalla de login, abre **"Servidor API (Vercel / remoto)"** y escribe la URL del bot, por ejemplo: `https://tu-host:3100`
- O abre la página con query param: `https://tu-panel.vercel.app/?api=https://tu-host:3100`
- O define `window.DASHBOARD_API_BASE` antes del script (avanzado).

## Requisitos del lado del bot
- El bot debe exponer el dashboard/API en Holy Hosting.
- El servidor ya envía CORS (`Access-Control-Allow-Origin: *`), por lo que el panel en Vercel puede consumir la API.
- Usa HTTPS en ambos lados cuando sea posible.

## Archivos
- `index.html` - panel completo
- `void-bot.png` / `favicon.png` - logo
- `vercel.json` - configuración Vercel
