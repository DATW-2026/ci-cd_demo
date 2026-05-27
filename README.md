# Demo de CI/CD

Proyecto de práctica para el curso **DATW2026**, orientado a montar una base para trabajar CI/CD con buenas prácticas de calidad de código.

## Estado actual del proyecto

- Proyecto Node.js inicializado.
- Configuración de ESLint creada con formato moderno (`eslint.config.js`).
- Lint preparado para múltiples tipos de archivo:
    - JavaScript/TypeScript
    - JSON
    - Markdown
    - CSS
- Script de lint disponible en `package.json`.
- Carpeta `src/` creada, actualmente vacía.

## Estructura

```text
.
├─ src/
├─ eslint.config.js
├─ package.json
├─ package-lock.json
└─ README.md
```

## Scripts disponibles

- `npm run lint`: ejecuta ESLint sobre todo el proyecto.

## Dependencias de desarrollo instaladas

- `eslint`
- `@eslint/js`
- `typescript-eslint`
- `globals`
- `@eslint/json`
- `@eslint/markdown`
- `@eslint/css`

## Cómo usarlo ahora mismo

1. Instalar dependencias:

    ```bash
    npm install
    ```

2. Ejecutar análisis estático:

    ```bash
    npm run lint
    ```
