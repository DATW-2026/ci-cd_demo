# Demo de CI/CD

Proyecto de práctica para el curso **DATW2026**, usado como base para trabajar desarrollo frontend, calidad de código, pruebas automatizadas y flujo de CI/CD.

## Estado actual del proyecto

La demo ya no es solo un proyecto Node.js con ESLint. Actualmente contiene una aplicación frontend con **Vite**, **TypeScript** y **Custom Elements** nativos.

Incluye:

- Aplicación web montada desde `src/main.ts`.
- Router básico con History API.
- Páginas principales:
    - Inicio (`/`)
    - Películas (`/films`)
    - Acerca de (`/about`)
- Componentes reutilizables en `src/core/components/`, como `app`, `header`, `menu`, `footer`, `counter`, `register` y `theme`.
- Entidades de dominio en `src/core/entities/`.
- Repositorios para acceso a datos en `src/core/repositories/`.
- Estilos globales en `base.css` e `index.css`.
- Estilos específicos junto a cada componente.
- Tests unitarios con **Vitest**, **Testing Library** y **jsdom**.
- Configuración de cobertura con `@vitest/coverage-v8`.
- Configuración de pruebas end-to-end con **Playwright**.
- Linting con ESLint para JavaScript y TypeScript.

## Estructura principal

```text
.
├─ .github/
├─ public/
│  ├─ favicon.svg
│  └─ icons.svg
├─ src/
│  ├─ about/
│  ├─ films/
│  ├─ home/
│  ├─ core/
│  │  ├─ components/
│  │  ├─ config/
│  │  ├─ data/
│  │  ├─ entities/
│  │  ├─ repositories/
│  │  └─ router/
│  ├─ main.ts
│  └─ setup-test.ts
├─ base.css
├─ index.css
├─ index.html
├─ eslint.config.js
├─ playwright.config.ts
├─ vitest.config.ts
├─ package.json
└─ README.md
```

## Scripts disponibles

- `npm run dev`: arranca el servidor de desarrollo de Vite.
- `npm run build`: ejecuta `tsc` y genera la build de producción.
- `npm run preview`: sirve localmente la build generada.
- `npm run lint`: ejecuta ESLint sobre el proyecto.
- `npm run test`: ejecuta los tests con Vitest.
- `npm run test:c`: ejecuta los tests con cobertura.
- `npm run e2e`: ejecuta las pruebas end-to-end de Playwright en Chromium.

## Cómo trabajar con el proyecto

1. Instalar dependencias:

    ```bash
    npm install
    ```

2. Arrancar el entorno de desarrollo:

    ```bash
    npm run dev
    ```

3. Validar calidad y pruebas:

    ```bash
    npm run lint
    npm run test
    npm run build
    ```

4. Ejecutar pruebas end-to-end cuando corresponda:

    ```bash
    npm run e2e
    ```

## Situación de CI/CD

El proyecto ya cuenta con las piezas locales necesarias para construir una pipeline básica:

- Instalación reproducible mediante `package-lock.json`.
- Análisis estático con ESLint.
- Comprobación de tipos y build con TypeScript y Vite.
- Tests unitarios con Vitest.
- Cobertura de tests.
- Base para pruebas end-to-end con Playwright.

El siguiente paso natural del demo es añadir workflows de CI, por ejemplo con GitHub Actions, para ejecutar `npm ci`, `npm run lint`, `npm run test` y `npm run build` en cada push o pull request.
