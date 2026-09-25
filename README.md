# Ruta Disney — Familia Moracho

Agenda de bolsillo para los 4 días en Disneyland Paris (8–11 octubre 2026): horarios día a día, la cena en Captain Jack's, el intento de mesa en Bistrot Chez Rémy, alturas mínimas de atracciones para Jorge y Martina, y consejos para no caer en trampas de turista.

Es una sola página web (sin servidor, sin dependencias que instalar) pensada para abrirse desde el móvil. Marca cada parada como hecha y lo recuerda la próxima vez que la abras en ese mismo teléfono.

## Ponerla en GitHub Pages (gratis, 5 minutos)

1. Crea un repositorio nuevo en GitHub (público o privado, da igual) y sube estos archivos tal cual están, sin carpetas.
   ```bash
   cd disney-agenda
   git init
   git add .
   git commit -m "Agenda Disneyland Paris"
   git branch -M main
   git remote add origin https://github.com/<tu-usuario>/<tu-repo>.git
   git push -u origin main
   ```
2. En GitHub, entra en **Settings → Pages**.
3. En "Build and deployment", elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`.
4. Guarda. En un par de minutos la web estará en `https://<tu-usuario>.github.io/<tu-repo>/`.
5. Abre ese enlace desde el móvil de cada uno y, en el menú del navegador, elige **"Añadir a pantalla de inicio"** — queda como una app con su propio icono, sin necesidad de conexión una vez cargada.

Si el repositorio es privado, GitHub Pages necesita un plan de pago para publicarlo; con uno público funciona igual en el plan gratuito.

## Archivos

- `index.html` — la app completa (agenda, consejos, alturas). Un único archivo, sin dependencias externas más allá de las tipografías de Google Fonts.
- `manifest.json` — hace que se pueda instalar como app en el móvil.
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `favicon.ico` — iconos de la app.

## Editarla

Todo el contenido (horarios, textos, alturas, consejos) está en unos arrays de JavaScript al principio del `<script>` de `index.html` (`DAYS`, `TIPS`, `HEIGHTS`). Cambiar un texto o una hora es editar esa lista y volver a subir el archivo; no hace falta tocar el resto del código.
