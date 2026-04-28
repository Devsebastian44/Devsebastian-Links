# 🔗 DevLinks

![Astro](https://img.shields.io/badge/Astro-SSG-BC52EE?style=flat&logo=astro&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-Strict-3178C6?style=flat&logo=typescript&logoColor=white)
![CSS](https://img.shields.io/badge/Estilos-CSS%20Custom-1572B6?style=flat&logo=css3&logoColor=white)
![Netlify](https://img.shields.io/badge/Deploy-Netlify-00C7B7?style=flat&logo=netlify&logoColor=white)
![Prettier](https://img.shields.io/badge/Formatter-Prettier-F7B93E?style=flat&logo=prettier&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI%2FCD-2088FF?style=flat&logo=github-actions&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat&logo=opensourceinitiative&logoColor=white)
![CI](https://github.com/devsebastian44/DevLinks/actions/workflows/ci.yml/badge.svg)

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
con cualquier plataforma de hosting estático.

---

## ⚙️ Features

- **Página de enlaces centralizada** tipo Linktree.
- **Generación estática pura con Astro SSG** — Zero-JS por defecto.
- **Diseño visual personalizado con CSS nativo** — Sin frameworks de utilidades.
- **TypeScript strict mode** para máxima seguridad de tipos.
- **Prettier con soporte nativo para Astro** para consistencia de código.
- **CI/CD con GitHub Actions** para validación automática de Pull Requests.

---

## 🛠️ Tech Stack

| Categoría | Tecnología        | Detalle                           |
| --------- | ----------------- | --------------------------------- |
| Framework | Astro (SSG)       | Generación estática pura          |
| Lenguaje  | TypeScript        | Strict mode                       |
| Estilos   | CSS Personalizado | Diseño artesanal                  |
| Testing   | Vitest            | Pruebas unitarias y de validación |
| CI/CD     | GitHub Actions    | Automatización de lint y tests    |
| Licencia  | MIT               | Libre uso personal y educativo    |

---

## 📦 Installation & Setup

### Prerrequisitos

- **Node.js** (v22 o superior)
- **npm** actualizado

### 1. Clonar el repositorio

```bash
git clone https://github.com/devsebastian44/DevLinks.git
cd DevLinks
```

### 2. Instalar dependencias

```bash
npm install
```

### 3. Configurar el entorno

```bash
cp .env.example .env
# Editar .env con los valores necesarios (si aplica)
```

---

## ▶️ Usage

### Servidor de desarrollo

```bash
npm run dev
```

Abre [http://localhost:4321](http://localhost:4321) en tu navegador.

### Build de producción

```bash
npm run build
```

### Ejecutar Tests

```bash
npm run test
```

### Verificar Linting

```bash
npm run lint
```

---

## 📁 Project Structure

```
DevLinks/
│
├── .github/workflows/          # Configuración de GitHub Actions
├── src/                        # Código fuente principal
├── public/                     # Assets estáticos
├── tests/                      # Pruebas automatizadas (Vitest)
├── astro.config.mjs            # Configuración de Astro
├── package.json                # Dependencias y scripts
└── README.md                   # Documentación principal
```

---

## 🤝 Contributing

¡Las contribuciones son bienvenidas! Sigue estos pasos para colaborar:

1. Haz un **Fork** del proyecto.
2. Crea una rama para tu mejora (`git checkout -B feature/mejor-increible`).
3. Realiza tus cambios y asegúrate de que pasen los tests (`npm run test`).
4. Haz un **Commit** de tus cambios siguiendo [Conventional Commits](https://www.conventionalcommits.org/).
5. Haz un **Push** a tu rama (`git push origin feature/mejor-increible`).
6. Abre un **Pull Request**.

---

## 🛡️ Security Disclaimer

> [!IMPORTANT]
> This project is for educational and ethical cybersecurity purposes only. The author is not responsible for any misuse of the information or tools contained in this repository.

---

## 📄 License

Este proyecto está distribuido bajo la licencia **MIT**.

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
    </td>
  </tr>
</table>
