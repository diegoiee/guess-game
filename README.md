# Adivinanzas de Figuras — App para iPhone (PWA)

Juego de memoria convertido en app instalable. Se agrega a la pantalla de inicio
del iPhone y se abre a pantalla completa, como una app nativa.

**App online:** https://diegoiee.github.io/guess-game/

## Archivos
- `index.html` — el juego (optimizado para iPhone: notch, sin zoom, botón salir).
- `manifest.webmanifest` — define nombre, ícono y modo pantalla completa.
- `service-worker.js` — hace que funcione sin internet una vez instalada.
- `icons/` — íconos de la app.

## Instalar en el iPhone (recomendado)
1. Abrí en **Safari** (importante: Safari, no Chrome):
   ```
   https://diegoiee.github.io/guess-game/
   ```
2. Tocá el botón **Compartir** (cuadrado con flecha ↑).
3. **Agregar a inicio** → **Agregar**.
4. Te aparece el ícono en la pantalla de inicio y abre a pantalla completa.

> Tip: la primera vez abrila con internet para que cachee todo; después funciona
> **sin conexión**.

## Cómo está publicada (GitHub Pages)
La app se sirve sola con GitHub Pages desde este repo. Configuración:
- Repo **público**.
- En **Settings → Pages**: Source = **Deploy from a branch**, Branch = **main**,
  Folder = **/ (root)**.

Cada vez que hagas `git push` a `main`, GitHub Pages se actualiza solo en uno o
dos minutos.

### Publicarlo de cero (si clonás el repo en otra cuenta)
1. Subí los archivos a la rama `main`:
   ```
   git add -A
   git commit -m "deploy"
   git push origin main
   ```
2. En GitHub: **Settings → Pages → Source: Deploy from a branch →
   Branch: `main` / `/ (root)` → Save**.
3. Esperá ~1 min. Tu URL queda en:
   ```
   https://<tu-usuario>.github.io/<nombre-del-repo>/
   ```

## Alternativas para usarla sin publicarla
- **Archivo único offline:** `AdivinanzasFiguras.html` se juega completo sin
  internet; pasalo al iPhone por AirDrop y abrilo en Safari.
  (Limitación de iOS: un archivo local **no** se puede fijar a la pantalla de
  inicio con ícono; para eso hace falta una URL, como la de Pages.)
- **Probar por WiFi local:** en la Mac, dentro de esta carpeta, corré
  `python3 -m http.server 4599` y entrá desde el iPhone a `http://<IP-de-tu-Mac>:4599`.
