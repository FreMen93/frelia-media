# frelia-media

Repositorio público solo para alojar las fotos/videos que `instagram_bot`
publica en `@frelia18k` vía la Instagram Graph API (que exige URLs públicas,
no acepta archivos locales).

**Este repo es público a propósito** — así `raw.githubusercontent.com` puede
servir los archivos sin autenticación, que es lo que Meta necesita para
descargarlos. No subas aquí nada que no quieras que sea público.

## Estructura

- `posts/` — fotos/videos para publicaciones normales del feed.
- `carousels/<nombre-del-carrusel>/` — una subcarpeta por carrusel, con las
  imágenes/videos en el orden en que deben aparecer (ej. `01.jpg`, `02.jpg`).
- `reels/` — videos para Reels.
- `stories/` — fotos/videos para Historias (no llevan caption).

## Cómo se usa

1. Freddy deja los archivos nuevos en la carpeta local `C:\frelia-media\...`.
2. El asistente hace commit + push aquí y arma la URL pública:
   `https://raw.githubusercontent.com/FreMen93/frelia-media/main/<ruta>`
3. Esa URL se usa como `media_url` / `children_urls` en el
   `content_calendar.json` de `instagram_bot`, con el caption y la fecha
   propuestos para revisión antes de programar/publicar.
