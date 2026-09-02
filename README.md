# Minimal Testimonial Section

Sección de testimonios responsiva construida con HTML y CSS puro, sin frameworks ni JavaScript. Muestra tres tarjetas con foto, nombre, calificación en estrellas y comentario.

## Estructura del proyecto

```
.
├── index.html
├── styles.css
└── images/
    ├── p1.jpg
    ├── p2.jpg
    └── p3.jpg
```

## Tecnologías

- HTML5
- CSS3 (Flexbox + Media Queries)
- [Font Awesome 6.2.1](https://fontawesome.com/) (vía CDN) para los íconos de estrellas
- [Google Fonts – Montserrat](https://fonts.google.com/specimen/Montserrat) (vía CDN)

## Cómo ejecutarlo

No requiere instalación ni build. Basta con abrir `index.html` en el navegador, o servirlo con cualquier servidor estático:

```bash
npx serve .
```

## Personalización

| Elemento | Dónde se edita |
|---|---|
| Nombre y comentario | `index.html`, dentro de cada `.testimonial` |
| Calificación (estrellas) | Clases `fas fa-star` (llena), `fa-star-half-stroke` (media) y `far fa-star` (vacía) en `.stars` |
| Foto de perfil | Reemplazar los archivos en `images/` manteniendo el mismo nombre, o cambiar el `src` |
| Color de acento | Variable de color `#9970FD` en `.border` y `.stars` dentro de `styles.css` |

## Responsividad

- `> 960px`: 3 columnas
- `≤ 960px`: 1 columna, tarjeta al 80% de ancho
- `≤ 600px`: 1 columna, tarjeta al 100% de ancho

## Problemas conocidos

- **Dependencia de CDN externo**: tanto Font Awesome como Montserrat se cargan desde CDN externos (`use.fontawesome.com` y `fonts.googleapis.com`). Sin conexión a internet, las estrellas no se renderizan y el texto cae al fallback `sans-serif`.

## Licencia

No especificada.
