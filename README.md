# Lectura a primera vista (piano)

App web de una sola página (`index.html`) para practicar lectura a primera vista con un teclado MIDI, al estilo Flowkey.

## Funciones
- Carga de canciones en **MusicXML** (`.musicxml`, `.xml`, `.mxl`) y MIDI (`.mid`).
- Conexión con teclado MIDI (Web MIDI: Chrome o Edge).
- Práctica con tempo o esperando tus notas, mano derecha / izquierda / ambas.
- Metrónomo, cuenta atrás, tempo ajustable, reproducción de la canción.
- Arrastrar la partitura para elegir dónde empezar.
- Ajustes: teclado MIDI, volumen, tamaño de la partitura, tema, fuente Bravura.

## Fuente Bravura
La partitura usa la fuente SMuFL **Bravura** (licencia SIL OFL, se puede redistribuir).
Descarga `Bravura.otf` desde https://github.com/steinbergmedia/bravura y colócala **junto a `index.html`**
(o cárgala desde ⚙ Ajustes, queda guardada en el navegador).

## Instalar en Android (PWA)
1. Publica el repositorio con GitHub Pages (ver abajo).
2. Abre la URL `https://TU_USUARIO.github.io/lectura-piano/` en **Chrome para Android**.
3. Menú ⋮ → **Instalar aplicación** (o «Añadir a la pantalla de inicio»).
4. Conecta el teclado por **USB (adaptador OTG)** antes de abrir la app y acepta el permiso MIDI.
Tras la primera carga funciona sin conexión. Si cambias la app, sube la versión de caché (`V` en `sw.js`).

## Uso en local
Abre `index.html` en Chrome o Edge. Para servirla con un servidor local:

    python3 -m http.server 8000

y entra en http://localhost:8000

## Publicar en GitHub Pages
1. Sube el repositorio a GitHub (ver más abajo).
2. En el repositorio: **Settings → Pages → Source: GitHub Actions**.
3. Cada `git push` a `main` publica la web (HTTPS, necesario para Web MIDI).

## Subir a GitHub
    ./iniciar-git.sh
    git remote add origin https://github.com/TU_USUARIO/lectura-piano.git
    git push -u origin main
