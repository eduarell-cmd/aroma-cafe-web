# AGENTS.md

Sitio web estático de **Aroma Café** (HTML5 + CSS3 puro). Sin dependencias, sin build, sin tests, sin lint. Todo el contenido está en español (`lang="es"`) y debe mantenerse así.

## Estructura y rutas (fácil de romper)

- `index.html` está en la raíz; las demás páginas viven en `pages/` (`menu.html`, `contact.html`, `login.html`).
- Por eso `pages/*.html` referencian recursos con `../`: `../css/styles.css`, `../index.html`.
- Al crear una página en `pages/`, usa siempre rutas relativas `../`, nunca absolutas.
- Al añadir una página en la raíz, usa rutas sin `../`.

## Navegación duplicada

- El `<header>` con la nav y el `<footer>` están copiados literalmente en las 4 páginas. No hay includes ni plantillas.
- Al añadir/renombrar un enlace del menú, actualízalo en **las 4 páginas** (header y footer).
- La página actual se marca con `class="nav-link active"`; los `id` de los enlaces (`#nav-home`, `#nav-menu`, `#nav-contact`, `#nav-login`) son hooks estables, consérvalos.

## CSS

- Una sola hoja compartida: `css/styles.css`, enlazada como `css/styles.css` desde la raíz y `../css/styles.css` desde `pages/`.
- Diseño con design tokens en `:root` (colores `--color-*`, fuentes, radios, sombras). Reutiliza esas variables; no hardcodees colores nuevos.
- Responsive por media query en `max-width: 768px` (breakpoint único).
- La única dependencia externa es Google Fonts vía `@import` al inicio del CSS.

## Verificación

No hay comandos de test/build/lint. Para probar cambios, sirve el sitio localmente:

```bash
python -m http.server 8000
```

Luego abre `http://localhost:8000`. Abrir `index.html` con doble clic también funciona.

## Git

- Rama por defecto: `main`. El repo es de práctica colaborativa: el flujo esperado es rama temática (`feature/...`) + Pull Request contra `main` (ver `README.md`).
- Antes de pushear, haz `git pull` para evitar pisar cambios de otros.
