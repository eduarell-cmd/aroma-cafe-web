# ☕ Aroma Café Web

Sitio web estático para la cafetería ficticia **Aroma Café**, diseñado para la práctica colaborativa de **Git y GitHub en equipo**.

Construido puramente con **HTML5 semántico** y **CSS3 moderno**, sin dependencias ni frameworks externos, garantizando una estructura limpia, comprensible y adaptable a cualquier dispositivo móvil o de escritorio.

---

## 📁 Estructura del Proyecto

```text
aroma-cafe-web/
├── index.html          # Página principal / Bienvenida
├── pages/
│   ├── menu.html       # Catálogo con 4 productos y precios
│   ├── contact.html    # Ubicación, horarios y formulario de contacto
│   └── login.html      # Pantalla de acceso de usuarios (visual)
├── css/
│   └── styles.css      # Hoja de estilos compartida (diseño responsive)
└── README.md           # Documentación y guía del proyecto
```

---

## 🌟 Páginas y Contenido

1. **Inicio (`index.html`)**:
   - Logotipo y barra de navegación superior.
   - Hero section de bienvenida con botones de llamada a la acción (*Call to Action*).
   - Bloques destacados de propuesta de valor (Tueste artesanal, Horneado diario, Espacio cálido).
   - Pie de página completo con enlaces y horario.

2. **Menú (`pages/menu.html`)**:
   - 4 productos destacados con etiqueta de categoría, descripción detallada y precios:
     - *Café Espresso Intenso*
     - *Cappuccino Tradicional*
     - *Latte Vainilla & Caramelo*
     - *Croissant Artesanal de Almendras*

3. **Contacto (`pages/contact.html`)**:
   - Tarjeta con dirección física, horarios de apertura, teléfono y correo electrónico.
   - Formulario de contacto visual con campos para nombre, correo, asunto y mensaje.

4. **Iniciar Sesión (`pages/login.html`)**:
   - Formulario limpio y centrado para inicio de sesión con campos para correo electrónico, contraseña, opción "Recordarme" y enlaces secundarios.

---

## 🚀 ¿Cómo visualizar el proyecto?

No requiere instalación de paquetes (`npm`, `yarn`, etc.):

1. **Directamente en el navegador**: Haz doble clic en `index.html` o ábrelo con tu navegador preferido (Chrome, Edge, Firefox, Safari).
2. **Con Live Server (VS Code / extensiones)**: Haz clic derecho en `index.html` y selecciona **"Open with Live Server"** para recarga automática al editar.
3. **Con Python (opcional)**:
   ```bash
   python -m http.server 8000
   ```
   Luego visita `http://localhost:8000` en tu navegador.

---

## 👥 Guía sugerida para practicar Git y GitHub en Equipo

Este repositorio es ideal para simular un flujo de trabajo profesional entre compañeros de equipo:

### 1. Inicialización del Repositorio (Líder / Integrante 1)
```bash
git init
git add .
git commit -m "feat: estructura inicial del proyecto Aroma Cafe"
git branch -M main
git remote add origin https://github.com/<tu-usuario>/aroma-cafe-web.git
git push -u origin main
```

### 2. Flujo de Trabajo en Equipo (Ramas y Pull Requests)
Cada miembro del equipo puede clonar el repositorio y trabajar en una funcionalidad aislada mediante ramas temáticas:

- **Clonar el proyecto**:
  ```bash
  git clone https://github.com/<tu-usuario>/aroma-cafe-web.git
  cd aroma-cafe-web
  ```

- **Crear una rama para tu tarea**:
  ```bash
  # Ejemplo: Miembro 1 mejora el menú
  git checkout -b feature/nuevos-productos-menu

  # Ejemplo: Miembro 2 agrega estilos o modo oscuro
  git checkout -b feature/estilos-modo-oscuro

  # Ejemplo: Miembro 3 agrega mapa interactivo en contacto
  git checkout -b feature/mapa-contacto
  ```

- **Guardar cambios y subir la rama a GitHub**:
  ```bash
  git add .
  git commit -m "feat(menu): agregar sección de postres de temporada"
  git push origin feature/nuevos-productos-menu
  ```

- **Abrir un Pull Request (PR)** en GitHub:
  - Comparar tu rama contra `main`.
  - Asignar a tus compañeros como *Reviewers* (revisores de código).
  - Practicar comentarios constructivos y aprobación de cambios (*Approve*).
  - Hacer *Merge* a `main` cuando esté listo.

---

## 📜 Licencia

Proyecto con fines puramente educativos y de práctica. Libre para modificar, expandir y usar en talleres de Git y desarrollo web.
