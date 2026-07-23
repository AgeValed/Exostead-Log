# Exostead-Log

Bitácora pública de avance de [Exostead](https://github.com/AgeValed/exostead). Muestra qué ya está entregado y qué está en la cola, sin nada del código del juego.

## Estructura

- `index.html` — la página. Lee `backlog.csv` al cargar, no tiene datos hardcodeados.
- `backlog.csv` — la fuente de datos. Se edita a mano y se sobreescribe cada vez que hay algo nuevo para reflejar.

## Cómo actualizar

1. Abrí `backlog.csv` (Excel, Google Sheets, o directamente en el editor).
2. Agregá o editá filas. Columnas:
   - `name` — nombre corto de la feature, en criollo, sin jerga técnica.
   - `status` — `done` o `backlog` (nada más, no hay "en progreso").
   - `category` — agrupador libre (Mundo, Combate, Edificios, etc). Si usás una categoría nueva, la página le asigna un color automático — no hace falta tocar el HTML.
   - `description` — una línea explicando qué es, para alguien que no conoce el código.
3. Commit + push.
4. La página en GitHub Pages se actualiza sola, no hace falta regenerar nada.

## Setup inicial de GitHub Pages

1. Subir `index.html` y `backlog.csv` a la raíz del repo (o a una carpeta `/docs`, tu elección).
2. Settings → Pages → Source: rama `main`, carpeta raíz (o `/docs` si los pusiste ahí).
3. El link queda algo como `https://agevaled.github.io/Exostead-Log/`.

## Notas

- Repo pensado como público (necesario para Pages gratis) — no meter nada del código o docs internos de Exostead acá.
- Nunca hay estado "en progreso" a propósito: algo pasa de `backlog` a `done` recién cuando está terminado al 100%.
