## dev/Talles: Astro: El framework para sitios web orientados al contenido

_https://cursos.devtalles.com/courses/take/Astro_

## Secciones

### Sección 1: Introducción

- [Instalaciones necesarias](https://gist.github.com/Klerith/b2ccb9d49385d766138e737f840650fc)

Hoja de atajos de Astro: Hoja de Atajos - Astro: https://github.com/Klerith/mas-talento/blob/main/astro/astro-cheat-sheet.pdf | [Aquí local](/blob/main/docs/astro-cheat-sheet.pdf)

### Sección 2: Introducción a Astro

[Ver sesión en devTalles](https://cursos.devtalles.com/courses/take/Astro/lessons/55900239-introduccion-a-la-seccion)

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

Al generarse un código final con el `npm run build` o comprobándolo con `npm run build & npm run preview` por defecto _NO_ se genera código _javascript_. Sí agrega alguna section de js vanilla en el archivo .astro, este iría incrustrado en el html final que se genere.

- [Nuestro primer sitio en Astro & Estructura de un proyecto](https://github.com/patchamama/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/commit/a854ac3285c474b7bf0a8346606031f54080da80)
- [Sintaxis y funcionamiento de los archivos .astro](https://github.com/patchamama/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/commit/b138a0910124e63d503c99581f7dfcd4453b70de)
- [Tarea - Actualizar momento actual](https://github.com/patchamama/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/commit/9c83c6a47f2658fc206c38288207d396561ef406)
  _Aquí es importante entender que sí estamos comprobando en modo desarrollo la aplicación `npm run dev` entonces el "momento actual" y "momento actual real" tiene un mismo valor pues se está generando en el momento la fecha dinámicamente con el código js y se está mostrando. Sin embargo, ya en modo producción `npm run build & npm run preview` no es así pues la primera parte del código que determina que se mueste la hora de "momento actual" se genera puro html pegando ahí la hora en texto pero la segunda parte "momento actual real" se genera desde el código js en la sección <script>...</script> que determina que se muestre ese tiempo en el momento de visitarse la página_.
- [Navegación entre páginas](https://github.com/patchamama/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/commit/5fec8c7502aa0b9cfc415ff7c3257161a05c7395)
- [Reutilización de components](https://github.com/patchamama/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/commit/a0ffa81902e479740ede3548e23300f8f7863d3b)
- [Layouts y Props](https://github.com/patchamama/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/commit/31562a243df18de40e59059eef7f3a80c43ab816)
  _Los Layouts son componentes especiales que envuelven (wrapper) elementos <html>, <head> y <body> de una página y que permiten por ello insertar códigos a un template común_.
- [Estilos por componente y globales](https://github.com/patchamama/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/commit/50008333604c4c994fb2c13e8f3e07322a5e5a9a)
- [Página 404](https://github.com/patchamama/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/commit/013c4d661b6365c37d042fd62085fe863498cba6)
- [View Transitions](https://github.com/patchamama/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/commit/729474a780d08b3af64c1fc951d4876741d92acd)
  _Lo que se hace es que se agrega el componente <ViewTransitions /> preferiblemente en el template/layout y esto permite que se cargen muy rápido las páginas como sí fuera un SPA, así sí hay algún enlace como un NavBar que navega a otra página entonces precarga la página antes de ser visitada y al visitar la página usa la opción ViewTransition del navegador con una animación que se puede también animar entre diferentes formas_.
- [Recapitulación](https://github.com/patchamama/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/commit/25e2ff07df5f7598856eeea0af7e2faa21506586)
  _La diferencia de referenciar el archivo de css usando desde Astro `import '../styles/global.css'` y usando directamente en el head la referencia al archivo en la carpeta public `<link rel="stylessheet" href="styles/global.css" />` es que con import se preprocesa por el compilador de Astro el css y se minimiza_.
- [Código fuente](https://github.com/DevTalles-corp/astro-foundation/tree/fin-seccion-02)
- [Ver sitio en producción en github pages](https://patchamama.github.io/devTalles-Astro-El-framework-para-sitios-web-orientados-al-contenido/dist_section2/)

### Documentación

- https://docs.astro.build/en/basics/project-structure/
- https://docs.astro.build/en/reference/cli-reference/#astro-preferences
- https://docs.astro.build/en/basics/layouts/
- https://docs.astro.build/en/guides/styling/
- https://dev.to/stackfindover/35-html-404-page-templates-5bge
- https://docs.astro.build/en/guides/view-transitions/

===

### Sección 3: Rutas dinámicas y paginación estática

### Documentación

===

## Snippers

- component (crea la estructura de un componente)
