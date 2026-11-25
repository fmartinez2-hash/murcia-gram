# MurciaGram — El Pinterest de la Región de Murcia

Plataforma web de inspiración visual desarrollada para promocionar el patrimonio histórico, natural y gastronómico de los municipios de la Región de Murcia.

## Características Técnicas
- **Arquitectura Semántica HTML5:** Uso exclusivo de etiquetas semánticas (`<header>`, `<nav>`, `<aside>`, `<main>`, `<article>`, `<figure>`, `<figcaption>`, `<footer>`) sin contenedores genéricos.
- **CSS3 Mobile-First & Range Queries:** Diseño adaptable construido desde móvil (`< 600px`) hacia tableta (`(width >= 600px) and (width <= 800px)`) y escritorio (`width > 800px`) mediante operadores matemáticos modernos y arquitectura híbrida Grid + Flexbox.
- **Microinteracciones UI/UX:** Tarjetas con sombras difuminadas, curvas Bézier personalizadas, overlay interactivo tipo Pinterest, estado permanente mediante selectores CSS (`:checked`) y hoja de estilos dedicada para impresión (`@media print`).
- **Rendimiento y SEO:** Imágenes responsivas mediante `<picture>` (400px móvil / 1000px escritorio), carga diferida (`loading="lazy"`) y metadatos SEO + Open Graph.

## Automatización de Imágenes con ImageMagick
El proyecto incluye una tarea configurada en `.vscode/tasks.json` compatible con Windows, macOS y Linux:
1. Coloca las fotografías originales en `/assets/raw/` (ej. `cartagena.jpg`, `lorca.jpg`).
2. Ejecuta la tarea con `Ctrl + Shift + B` (o `Terminal > Ejecutar tarea > Optimizar Imágenes MurciaGram (ImageMagick)`).
3. El script generará automáticamente las variantes `-mobile.jpg` (400px) y `-desktop.jpg` (1000px) optimizadas en `/assets/img/`.
