# UCN Bilingüismo — Web Object

Objeto web (HTML) bilingüe para que los estudiantes de idiomas de la
**Fundación Universitaria Católica del Norte (UCN)** accedan a dos políticas
institucionales relevantes para el bilingüismo, visualizadas como **flipbook**
(animación de paso de páginas).

A bilingual HTML web object for UCN language students to access two
institutional policies relevant to bilingualism, shown as a **flipbook**
(page-flip animation).

## Contenido / Contents

| Documento · Document | Páginas · Pages | Descripción · Description |
| --- | --- | --- |
| Acuerdo 05 de 2025 (Lengua Extranjera) | 6 | Modifica el Acuerdo N.º 12 de 2024 y reglamenta la Lengua Extranjera para los programas académicos. |
| Acuerdo 15 de 2025 (Calendario Académico 2026) | 14 | Establece el calendario académico 2026: pregrado, posgrado y Centro de Idiomas. |

## Estructura / Structure

```
webobject/
├── index.html                    # Objeto web principal (bilingüe ES/EN + flipbook)
├── assets/
│   ├── logo.svg                  # Logotipo oficial UCN
│   ├── background.mp4            # Video de fondo
│   └── pages/
│       ├── manifest.js           # Índice de libros (window.BOOKS)
│       ├── doc1/page-01.png …    # Páginas renderizadas del Acuerdo 05
│       └── doc2/page-01.png …    # Páginas renderizadas del Acuerdo 15
└── docs/
    ├── acuerdo-05-2025-lengua-extranjera.pdf
    └── acuerdo-15-2025-calendario-academico-2026.pdf
```

## Uso / Usage

- Abre `index.html` en un navegador, o publícalo en GitHub Pages.
- El botón **ES / EN** cambia el idioma del objeto web.
- Pulsa **Abrir flipbook** en cada tarjeta para ver el documento con animación
  de paso de páginas. Usa las flechas laterales, las teclas ← →, o arrastra
  para navegar; **Esc** cierra el visor. También puedes abrir el PDF original.

> Open `index.html` in a browser or publish it on GitHub Pages. The **ES / EN**
> button switches the language. Click **Open flipbook** on each card to read the
> document with a page-flip animation (use the side arrows or ← → keys, and Esc
> to close). The original PDF is also available.

## Notas técnicas / Technical notes

- Todo es autocontenido (sin CDN): las páginas de los PDF se renderizaron
  previamente a PNG y la animación es CSS 3D puro. Funciona abierto desde disco
  (`file://`) o servido por cualquier host estático.
- Para regenerar las imágenes, renderiza los PDF con PyMuPDF (fitz) y actualiza
  `assets/pages/manifest.js`.
