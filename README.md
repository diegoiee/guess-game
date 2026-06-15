# Adivinanzas de Figuras — App para iPhone (PWA)

Juego de memoria convertido en app instalable. Se agrega a la pantalla de inicio
del iPhone y se abre a pantalla completa, como una app nativa.

## Archivos
- `index.html` — el juego (optimizado para iPhone: notch, sin zoom, botón salir).
- `manifest.webmanifest` — define nombre, ícono y modo pantalla completa.
- `service-worker.js` — hace que funcione sin internet una vez instalada.
- `icons/` — íconos de la app.

## Opción A — Probarla YA en el iPhone (misma red WiFi)
1. La Mac y el iPhone tienen que estar en la misma red WiFi.
2. En la Mac, dentro de esta carpeta, corré:
   ```
   python3 -m http.server 4599
   ```
3. En el iPhone, abrí **Safari** y entrá a:
   ```
   http://192.168.1.39:4599
   ```
4. Tocá el botón **Compartir** (cuadrado con flecha) → **Agregar a inicio**.
> Nota: por WiFi local el juego anda perfecto, pero el modo "sin internet"
> recién funciona del todo con la Opción B (hosting con https).

## Opción B — Instalación definitiva y offline (recomendada)
Subí esta carpeta a cualquier hosting estático gratis con https:
- **Netlify Drop**: entrá a https://app.netlify.com/drop y arrastrá la carpeta.
- **GitHub Pages**, **Cloudflare Pages**, etc.

Después abrí la URL `https://...` en Safari del iPhone y **Agregar a inicio**.
Así queda como app completa, con ícono propio y funcionando sin conexión.
