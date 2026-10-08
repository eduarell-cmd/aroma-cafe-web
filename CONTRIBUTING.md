# Guía de contribución — Aroma Café Web

## Flujo de ramas

- `main`: rama estable. Solo recibe merges vía Pull Request (release desde `develop`, hotfixes urgentes).
- `develop`: rama de integración. Toda funcionalidad se integra aquí vía Pull Request.
- `feature/<nombre>`: una rama por integrante/tarea, creada **desde `develop`**.
- `hotfix/<nombre>`: correcciones urgentes, creadas **desde `main`**; se fusionan a `main` **y de vuelta a `develop`**.

## Equipo y ramas asignadas

| Integrante     | Rama                |
| -------------- | ------------------- |
| AngelDittrich | `feature/menu-page`   |
| DamianOlivar     | `feature/login-form`  |
| EduardoArellanes | `feature/contact-page` |

## Commits

Usa mensajes en formato convencional, en español o inglés pero consistentes:

- `feat(pagina): ...` — nueva funcionalidad o contenido
- `fix(...): ...` — corrección de errores
- `docs: ...` / `chore: ...` — documentación o tareas

## Pull Requests

1. Actualiza tu rama con `develop` (`git pull origin develop`) antes de abrir el PR.
2. Abre el PR contra `develop` (o contra `main` si es release/hotfix) con **título y descripción**.
3. Un compañero revisa y aprueba antes del merge.
4. No borres las ramas `feature/*` ni `hotfix/*` después del merge (deben quedar visibles como evidencia).

## Releases

Las versiones se publican fusionando `develop` → `main` con un PR de release, y etiquetando con versionado semántico (`v1.0.0`, `v1.0.1`, ...).
