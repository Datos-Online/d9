<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/public/logo-readme-light.svg">
    <source media="(prefers-color-scheme: light)" srcset="docs/public/logo-readme.svg">
    <img alt="d9 Logo" src="docs/public/logo-readme.svg" width="200">
  </picture>
</p>

<br />

[English](./readme.md) - [Español](./readme-es.md)

# d9 — Plataforma de Datos Abiertos

**d9** es un fork de código abierto de [Directus 9](https://github.com/directus/directus) (GPLv3), mantenido de forma independiente por [La Webcapsule](https://github.com/LaWebcapsule). Dado que Directus 10+ es ahora un software de código abierto premium, este repositorio tiene como objetivo mantener una versión estándar de código abierto de Directus 9.

> [!NOTE]
> d9 no está afiliado, respaldado o conectado con el equipo central de Directus ni con Monospace Inc.

## ¿Por qué d9?

- **Permanencia de código abierto** — d9 permanece GPLv3, para siempre. Sin puertas premium, sin dependencia del proveedor.
- **Compatibilidad inmediata** — Mismo esquema de base de datos que Directus 9. Migra en minutos, no en días.

## Características

- **API REST & GraphQL** — Añade instantáneamente una API Node.js extremadamente rápida sobre cualquier base de datos SQL.
- **Gestiona SQL puro** — Funciona con bases de datos SQL nuevas o existentes, sin necesidad de migración.
- **Soporte multi-base de datos** — PostgreSQL, MySQL, SQLite, OracleDB, CockroachDB, MariaDB y MS-SQL.
- **Auto-alojado** — Ejecútalo en tu propia infraestructura. Tú eres dueño de tus datos.
- **Totalmente extensible** — Arquitectura modular, fácil de personalizar con extensiones.
- **Estudio de Datos sin código** — Un panel de control Vue.js intuitivo para usuarios no técnicos.

## Inicio rápido

```bash
npm init @wbce-d9/directus-project@latest
```

O con Docker:

```bash
docker run -d -p 8055:8055 ghcr.io/lawebcapsule/directus9:latest
```

## Migrando desde Directus 9

d9 utiliza el mismo esquema de base de datos que Directus 9. No se necesita migración de base de datos.

### 1. Actualiza tus dependencias

```json
// package.json
"directus": "9.x.x"           →  "@wbce-d9/directus9": "10.x.x"
"@directus/some-package"       →  "@wbce-d9/some-package"
```

### 2. Actualiza tus importaciones

```ts
// Before
import { ... } from "directus"
import { ... } from "@directus/some-package"

// After
import { ... } from "@wbce-d9/directus9"
import { ... } from "@wbce-d9/some-package"
```

### 3. Instala y ejecuta

```bash
npm update
npx directus start
```

## SDK de JS

```bash
npm install @wbce-d9/sdk
```

## Extensiones

Todas las extensiones de Directus 9 son compatibles con d9 sin necesidad de configuración adicional.

Para crear una nueva extensión:

```bash
npm init @wbce-d9/directus-extension@latest
```

## Enlaces

- **[Documentación](https://d9.webcapsule.io/getting-started/introduction.html)** — Referencia completa y guías
- **[GitHub](https://github.com/LaWebcapsule/d9)** — Código fuente e incidencias
- **[Contribuir](./contributing.md)** — Cómo contribuir a d9

## Licencia

d9 se publica bajo la licencia [GPLv3](./license).

Este repositorio es un fork de Directus 9, que fue publicado bajo GPLv3 por Monospace Inc. d9 es un proyecto independiente mantenido por La Webcapsule.

## Descargo de responsabilidad sobre activos

Este fork contiene versiones modificadas de los activos de documentación originales de Directus (capturas de pantalla, diagramas y vídeos). Estos activos han sido alterados para reemplazar la marca Directus por la marca d9 y para eliminar cualquier información de identificación de usuarios. En este proyecto no se utilizan marcas registradas, logotipos originales de Directus ni datos personales de los colaboradores de Directus.