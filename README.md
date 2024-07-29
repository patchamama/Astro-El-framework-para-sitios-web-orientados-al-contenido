## dev/Talles: Astro: El framework para sitios web orientados al contenido

_https://cursos.devtalles.com/courses/take/Astro_

## Secciones

### Sección 1: Introducción

- [Instalaciones necesarias](https://gist.github.com/Klerith/b2ccb9d49385d766138e737f840650fc)

Hoja de atajos de Astro: Hoja de Atajos - Astro: https://github.com/Klerith/mas-talento/blob/main/astro/astro-cheat-sheet.pdf | [Aquí local](/blob/main/docs/astro-cheat-sheet.pdf)

### Sección 2: Introducción a Astro

```
# Crear proyecto con Astro
npm create astro@latest

# Instalar dependencias
npm install

# Ejecutar proyecto con Astro y abrir página demo en navegador
npm run dev
open http://localhost:4321/

# Crear el sitio para producción y abrir en navegador
npm run build
open dist/index.html
# o `http-server dist` o puede ser también `cd dist & http-server -o`
# también puede ser `npm run build & npm run preview`

```

Para crear una ruta (path) es suficiente con crear un archivo en la carpeta `src/pages`, por ejemplo `src/pages/about.astro` y automáticamente el contenido de este archivo se mostrará en la url: `http://localhost:4321/about`

En la carpeta `public` se guardan contenidos como imágenes, fonts e icons, que no se van a optimizar por parte de Astro pero al crear el build (`npm run build`) este contenido se pasará a la carpeta de producción (archivos estáticos finalmente en la carpeta `dist`) lista para hacer un _deployment_ en versel, github pages,...

Al generarse un código final con el `npm run build` o comprobándolo con `npm run build & npm run preview` por defecto no se genera código _javascript_.

### Documentación

- https://docs.astro.build/en/basics/project-structure/
- https://docs.astro.build/en/reference/cli-reference/#astro-preferences
