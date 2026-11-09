# Lector de listas de canciones

Web estática (sin servidor, sin instalación). Subes fotos con listas de canciones y obtienes cada título con su enlace de `youtube.com`.

## Cómo funciona

1. **OCR en el navegador** con [Tesseract.js](https://github.com/naptha/tesseract.js). Las imágenes no se envían a ningún servidor.
2. **Limpieza del texto**: quita numeración, viñetas, duraciones y líneas con ruido.
3. **Revisión manual**: puedes corregir la lista antes de buscar.
4. **Enlaces**:
   - Sin clave de API: `https://www.youtube.com/results?search_query=...`
   - Con clave de YouTube Data API v3: `https://www.youtube.com/watch?v=ID` (video directo)

Todos los enlaces pertenecen al dominio `youtube.com`.

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `song-list-reader`).
2. Sube `index.html` y `README.md` a la rama `main`.
3. Ve a **Settings → Pages**.
4. En **Source** elige `Deploy from a branch`, rama `main`, carpeta `/ (root)`.
5. Tu web quedará en `https://TU-USUARIO.github.io/song-list-reader/`.

## Clave de YouTube API (opcional)

1. Entra a [Google Cloud Console](https://console.cloud.google.com/) y crea un proyecto.
2. Activa **YouTube Data API v3**.
3. Crea una clave en **Credenciales → Crear credenciales → Clave de API**.
4. Restringe la clave por **referente HTTP** a `https://TU-USUARIO.github.io/*`.
5. Pégala en la sección "Enlaces directos al video" de la web. Se guarda solo en tu navegador.

La cuota gratuita permite unas 100 búsquedas al día. Si se agota, la web vuelve automáticamente a los enlaces de búsqueda.

## Consejos para mejores resultados

- Usa capturas nítidas y con buen contraste.
- Elige el idioma correcto antes de leer.
- Revisa el texto detectado: el OCR puede confundir letras en tipografías decorativas.

## Licencia

MIT
