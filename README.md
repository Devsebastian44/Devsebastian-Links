# 🔗 DevLinks

![Astro](https://img.shields.io/badge/Astro-SSG-BC52EE?style=flat&logo=astro&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-Strict-3178C6?style=flat&logo=typescript&logoColor=white)
![CSS](https://img.shields.io/badge/Estilos-CSS%20Custom-1572B6?style=flat&logo=css3&logoColor=white)
![Netlify](https://img.shields.io/badge/Deploy-Netlify-00C7B7?style=flat&logo=netlify&logoColor=white)
![Prettier](https://img.shields.io/badge/Formatter-Prettier-F7B93E?style=flat&logo=prettier&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green?style=flat&logo=opensourceinitiative&logoColor=white)

> 🌐 **Live:** [devlinks44.netlify.app](https://devlinks44.netlify.app)

---

## 🧠 Overview

**DevLinks** es una página personal de agregación de enlaces estilo **Linktree**,
construida con **Astro** en modo de generación estática pura (SSG). Su propósito
es centralizar en un único punto de acceso todos los perfiles profesionales,
proyectos destacados, redes sociales y recursos del desarrollador, ofreciendo
una alternativa rápida, personalizable y autohosteada a plataformas como Linktree
o Beacons.

Al estar generada completamente en tiempo de compilación como HTML, CSS y
JavaScript mínimo sin dependencias de servidor ni base de datos, la página
resultante es extremadamente ligera, de carga casi instantánea y compatible
con cualquier plataforma de hosting estático. El proyecto hace uso de
**TypeScript en modo strict** vía la configuración `astro/tsconfigs/strict`
y está formateado con **Prettier** con el plugin oficial `prettier-plugin-astro`,
garantizando consistencia de código en archivos `.astro`, `.ts` y `.js`.

El diseño visual está implementado con **CSS personalizado** (representa el
23.9% del código base), prescindiendo de frameworks de utilidades, lo que
permite un control granular sobre cada elemento de la interfaz sin dependencias
de terceros adicionales en producción.

---

## ⚙️ Features

- **Página de enlaces centralizada** tipo Linktree con tarjetas o botones
  visuales que redirigen a todos los perfiles y proyectos del desarrollador
  desde una única URL compartible.
- **Generación estática pura con Astro SSG** — sin JavaScript en cliente por
  defecto, sin llamadas a APIs externas, sin base de datos. El sitio completo
  se compila a archivos estáticos listos para desplegar en cualquier CDN.
- **Diseño visual personalizado con CSS nativo** — estética y layout
  completamente artesanal sin depender de Tailwind ni otro framework de
  estilos, con control total sobre tipografía, colores, animaciones y layout.
- **TypeScript strict mode** mediante la extensión `astro/tsconfigs/strict`,
  asegurando el máximo nivel de seguridad de tipos en todos los componentes
  Astro y archivos de configuración.
- **Prettier con soporte nativo para Astro** vía `prettier-plugin-astro` con
  parser dedicado para archivos `.astro`, garantizando formateo consistente
  en todo el proyecto.
- **Logo del proyecto** incluido (`Logo.png`) como identidad visual propia
  de la página de enlaces.
- **Variables de entorno plantilladas** en `.env.example` para configuración
  limpia y reproducible del entorno local.
- **Configuración de editor estandarizada** con `.editorconfig` para mantener
  consistencia entre distintos editores y sistemas operativos.
- **Arquitectura DevSecOps dual** — desarrollo completo en GitLab (fuente de
  verdad) con publicación sanitizada automatizada hacia GitHub vía
  `publish_public.ps1`.
- **Despliegue en Netlify** con generación y distribución del sitio estático
  directamente desde el repositorio, con CDN global y HTTPS automático.

---

## 🛠️ Tech Stack

| Categoría | Tecnología | Detalle |
|---|---|---|
| Framework | Astro (SSG) | Generación estática pura, zero-JS por defecto |
| Lenguaje | TypeScript | Strict mode via `astro/tsconfigs/strict` |
| Estilos | CSS Personalizado | Sin framework de utilidades, diseño artesanal |
| Formateo | Prettier + `prettier-plugin-astro` | `printWidth: 100`, `singleQuote`, `semi` |
| Despliegue | Netlify | Hosting estático con CDN global |
| Node versioning | `.nvmrc` | Versión de Node fijada para el entorno |
| Publicación | PowerShell (`publish_public.ps1`) | Sanitización y push a GitHub |
| Licencia | MIT | Libre uso personal y educativo |

---

## 📦 Installation

### Prerrequisitos

- **Node.js** (versión especificada en `.nvmrc`)
- **npm** actualizado

### 1. Clonar el repositorio

```bash
# Repositorio completo de laboratorio (fuente de verdad, GitLab)
git clone https://gitlab.com/group-programming-lab/DevLinks.git

# Portafolio público sanitizado (GitHub)
git clone https://github.com/devsebastian44/DevLinks.git

cd DevLinks
```

### 2. Usar la versión correcta de Node

```bash
nvm use
```

### 3. Instalar dependencias

```bash
npm install
```

### 4. Configurar el entorno (si aplica)

```bash
cp .env.example .env
# Editar .env con los valores necesarios
```

---

## ▶️ Usage

### Servidor de desarrollo

```bash
npm run dev
```

Abre [http://localhost:4321](http://localhost:4321) en tu navegador.

> Astro corre en el puerto `4321` por defecto.

### Build de producción

```bash
npm run build
```

Los archivos estáticos se generan en el directorio `dist/`, listos para
subir a cualquier plataforma de hosting (Netlify, Vercel, GitHub Pages,
Cloudflare Pages, etc.).

### Previsualizar el build localmente

```bash
npm run preview
```

### Formatear el código

```bash
# Verificar formato de todos los archivos (.astro, .ts, .js, .css)
npx prettier --check .

# Aplicar formato automáticamente
npx prettier --write .
```

### Publicar a GitHub (DevSecOps)

```powershell
# Desde PowerShell, en el entorno de laboratorio GitLab
.\scripts\publish_public.ps1
```

---

## 📁 Project Structure

```
DevLinks/
│
├── src/                        # Código fuente principal de la aplicación
│   ├── pages/
│   │   └── index.astro         # Página principal — listado de todos los enlaces
│   ├── components/             # Componentes Astro reutilizables
│   │   ├── LinkCard.astro      # Tarjeta/botón individual para cada enlace
│   │   ├── Avatar.astro        # Foto o avatar del perfil
│   │   └── SocialIcon.astro    # Iconos de redes sociales
│   ├── layouts/
│   │   └── Layout.astro        # Layout base con metadata SEO y estilos globales
│   └── styles/                 # Estilos CSS personalizados
│       └── global.css          # Variables CSS, reset, tipografía y layout base
│
├── public/                     # Assets estáticos servidos directamente
│   ├── favicon.svg             # Ícono del sitio
│   └── ...                     # Imágenes, fuentes u otros assets públicos
│
├── Logo.png                    # Logo del proyecto DevLinks (raíz del repo)
│
├── .vscode/                    # Configuración recomendada de VS Code
├── .editorconfig               # Estándar de formato entre editores
├── .env.example                # Plantilla de variables de entorno
├── .gitignore                  # Exclusiones de Git
├── .nvmrc                      # Versión de Node.js fijada
├── .prettierrc                 # Config Prettier con prettier-plugin-astro
├── astro.config.mjs            # Configuración mínima de Astro (SSG puro)
├── tsconfig.json               # TypeScript strict via astro/tsconfigs/strict
├── package.json                # Dependencias y scripts del proyecto
├── LICENSE                     # Licencia MIT
└── README.md                   # Documentación principal
```

> **Nota:** Las carpetas `scripts/`, `tests/` y el archivo `.gitlab-ci.yml`
> existen únicamente en el repositorio privado de GitLab y son eliminadas
> automáticamente por `publish_public.ps1` antes de cada publicación en GitHub.

---

## 🎨 Personalización

Para adaptar DevLinks a tu propio perfil, edita los datos directamente en
`src/pages/index.astro` y los componentes correspondientes:

**Datos de perfil:**

```astro
---
const profile = {
  name: 'Tu Nombre',
  role: 'Tu Rol Profesional',
  avatar: '/tu-avatar.jpg',
  bio: 'Descripción breve de tu perfil',
};
---
```

**Agregar o modificar enlaces:**

```astro
const links = [
  { label: 'GitHub',    url: 'https://github.com/tuusuario',    icon: 'github'   },
  { label: 'LinkedIn',  url: 'https://linkedin.com/in/tuperfil', icon: 'linkedin' },
  { label: 'Portfolio', url: 'https://tuweb.com',               icon: 'globe'    },
  { label: 'Blog',      url: 'https://tublog.com',              icon: 'rss'      },
];
```

**Paleta de colores** — edita las variables CSS en `src/styles/global.css`:

```css
:root {
  --color-bg: #0f0f0f;
  --color-surface: #1a1a1a;
  --color-accent: #bc52ee;
  --color-text: #f0f0f0;
  --color-muted: #888888;
}
```

---

## 🔐 Security

### Variables de entorno

El archivo `.env.example` documenta cualquier variable de entorno requerida
sin exponer valores reales. El `.gitignore` excluye `.env` y `.env.*` del
repositorio, previniendo filtraciones accidentales de configuración local.

### Sin dependencias de servidor en producción

Al ser un sitio 100% estático, DevLinks no expone endpoints, bases de datos
ni lógica de servidor que puedan ser atacados. La superficie de ataque se
reduce al mínimo posible para una aplicación web.

### Consistencia de editor

El `.editorconfig` normaliza codificación de caracteres, saltos de línea y
tabulaciones entre distintos editores y sistemas operativos, previniendo
diffs innecesarios por diferencias de entorno.

---

## 🌐 Repository Architecture

Este proyecto sigue una arquitectura distribuida de doble repositorio,
separando el entorno de desarrollo completo del portafolio público:

**GitHub** expone el código fuente del sitio estático, la configuración del
proyecto y la documentación como portafolio público limpio y compartible.

**GitLab** es la fuente de verdad y laboratorio de desarrollo: contiene los
scripts de automatización DevSecOps (`scripts/`), los tests de validación
(`tests/`), el pipeline de CI/CD (`.gitlab-ci.yml`) y toda la infraestructura
interna que no forma parte del portafolio público. El flujo de publicación
es orquestado por `scripts/publish_public.ps1`, que sanitiza el repositorio
y fuerza el push hacia GitHub de forma controlada y auditable.

### 🔗 Full Source Code

👉 Código completo disponible en GitLab:
[https://gitlab.com/group-programming-lab/DevLinks](https://gitlab.com/group-programming-lab/DevLinks)

---

## 🚀 Roadmap

Mejoras sugeridas a partir de la arquitectura y stack detectados en el código:

- **Modo oscuro / claro** con toggle persistido en `localStorage` y detección
  automática de `prefers-color-scheme` del sistema operativo.
- **Animaciones de entrada** con CSS `@keyframes` o las transiciones de View
  Transitions API de Astro para una experiencia más fluida al cargar la página.
- **Sección de proyectos destacados** con tarjetas que incluyan descripción,
  tecnologías usadas y enlace al repositorio, diferenciada visualmente del
  listado de redes sociales.
- **Contador de visitas** integrado con un servicio externo sin necesidad de
  backend propio (Umami, Plausible, o simple badge de shields.io).
- **Optimización de imágenes** con el componente `<Image />` nativo de Astro
  para el avatar y otros assets, generando formatos modernos (WebP, AVIF)
  automáticamente en el build.
- **Open Graph y Twitter Cards** configurados en el `<Layout>` con metadata
  dinámica para mejorar el preview al compartir la URL en redes sociales.
- **Sitemap.xml automático** con `@astrojs/sitemap` para indexación en
  buscadores.
- **Tests de accesibilidad** con `axe-core` integrado en el pipeline de
  GitLab CI/CD para garantizar cumplimiento de estándares WCAG.
- **Modo multi-perfil** con rutas dinámicas Astro (`/[usuario].astro`)
  que permitan gestionar múltiples páginas de enlaces desde un único
  repositorio usando archivos de datos JSON o YAML por perfil.

---

## 📄 License

Este proyecto está distribuido bajo la licencia **MIT**.

Puedes usar, copiar, modificar, fusionar, publicar y distribuir el
software libremente para uso personal y educativo, siempre incluyendo
el aviso de copyright original.

Copyright © 2025 **Sebastián Zhunaula** (devsebastian44)

---

## 👨‍💻 Author

<table>
  <tr>
    <td align="center">
      <b>Sebastián Zhunaula</b><br/>
      <sub>Full-Stack Developer · Frontend Specialist · UI Designer</sub><br/><br/>
      <a href="https://github.com/devsebastian44">
        <img src="https://img.shields.io/badge/GitHub-devsebastian44-black?style=flat&logo=github" />
      </a>
      <br/>
      <a href="https://gitlab.com/group-programming-lab">
        <img src="https://img.shields.io/badge/GitLab-group--programming--lab-FC6D26?style=flat&logo=gitlab" />
      </a>
      <br/>
      <a href="https://devlinks44.netlify.app">
        <img src="https://img.shields.io/badge/DevLinks-devlinks44.netlify.app-00C7B7?style=flat&logo=netlify" />
      </a>
    </td>
  </tr>
</table>

> Este proyecto forma parte de un portafolio de desarrollo web frontend,
> demostrando el uso de Astro como generador de sitios estáticos con
> TypeScript strict, CSS artesanal, formateo profesional con Prettier y
> despliegue continuo en Netlify, todo bajo una estrategia DevSecOps de
> doble repositorio.