# 📅 Scheduler

![Scheduler Banner](https://img.shields.io/badge/Scheduler-Open%20Source-blue?style=for-the-badge)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.x-blue.svg?logo=python)](https://www.python.org/)
[![R](https://img.shields.io/badge/R-Programming-276DC3.svg?logo=r)](https://www.r-project.org/)
[![React](https://img.shields.io/badge/React-Frontend-61DAFB.svg?logo=react)](https://reactjs.org/)
[![C#](https://img.shields.io/badge/C%23-.NET-512BD4.svg?logo=csharp)](https://docs.microsoft.com/dotnet/csharp/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626.svg?logo=jupyter)](https://jupyter.org/)

[![GitHub Sponsors](https://img.shields.io/badge/GitHub-Sponsors-pink?style=for-the-badge&logo=githubsponsors)](https://github.com/sponsors/elisaul77)
[![PayPal](https://img.shields.io/badge/PayPal-Donate-blue?style=for-the-badge&logo=paypal)](https://paypal.me/eflorezp)
[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow?style=for-the-badge&logo=buymeacoffee)](https://buymeacoffee.com/elisaul77)

**Scheduler** es una aplicación **Open Source** diseñada para la gestión, automatización y programación de tareas en múltiples lenguajes de programación. Este proyecto proporciona ejemplos, utilidades y herramientas para **Python, R, React, Jupyter Notebooks y C#**.

---

## ✨ Características Principales

- 🐍 **Python**: Scripts de automatización y scheduling con cron jobs
- 📊 **R**: Análisis estadístico y programación de tareas de data science
- ⚛️ **React**: Interfaces frontend para visualización y control de schedulers
- 📓 **Jupyter Notebooks (.ipynb)**: Documentación interactiva y prototipos
- 🔷 **C#**: Integraciones con .NET y Windows Task Scheduler

---

## 📁 Estructura de Carpetas por Lenguaje

```
Scheduler/
│
├── 📂 python/                    # Código Python
│   ├── schedulers/               # Módulos de scheduling
│   ├── utils/                    # Utilidades auxiliares
│   ├── tests/                    # Tests unitarios
│   └── requirements.txt          # Dependencias Python
│
├── 📂 r/                         # Código R
│   ├── scripts/                  # Scripts de análisis
│   ├── schedulers/               # Funciones de programación
│   └── packages.R                # Dependencias R
│
├── 📂 react/                     # Frontend React
│   ├── src/                      # Código fuente
│   │   ├── components/           # Componentes reutilizables
│   │   ├── hooks/                # Custom hooks
│   │   ├── services/             # Servicios API
│   │   └── pages/                # Páginas principales
│   ├── public/                   # Archivos estáticos
│   └── package.json              # Dependencias Node.js
│
├── 📂 notebooks/                 # Jupyter Notebooks
│   ├── tutorials/                # Tutoriales interactivos
│   ├── examples/                 # Ejemplos de uso
│   └── prototypes/               # Prototipos de desarrollo
│
├── 📂 csharp/                    # Código C#
│   ├── Scheduler.Core/           # Biblioteca principal
│   ├── Scheduler.API/            # API REST
│   ├── Scheduler.Tests/          # Tests unitarios
│   └── Scheduler.sln             # Solución Visual Studio
│
├── 📂 docs/                      # Documentación
│   ├── api/                      # Documentación API
│   ├── guides/                   # Guías de usuario
│   └── architecture/             # Documentación de arquitectura
│
├── 📂 docker/                    # Configuración Docker
│   ├── Dockerfile.python         # Imagen Python
│   ├── Dockerfile.react          # Imagen React
│   └── docker-compose.yml        # Orquestación de servicios
│
├── .gitignore                    # Archivos ignorados
├── LICENSE                       # Licencia MIT
└── README.md                     # Este archivo
```

---

## 🏗️ Arquitectura de Implementación

### Diagrama de Arquitectura

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                              SCHEDULER SYSTEM                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐  │
│  │   FRONTEND  │    │   API LAYER │    │   CORE      │    │  STORAGE    │  │
│  │   (React)   │───▶│   (REST)    │───▶│  ENGINE     │───▶│  (Database) │  │
│  └─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘  │
│        │                  │                   │                  │          │
│        ▼                  ▼                   ▼                  ▼          │
│  ┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐  │
│  │  Components │    │  Endpoints  │    │  Schedulers │    │    SQL      │  │
│  │  - Dashboard│    │  - /tasks   │    │  - Python   │    │  - Tasks    │  │
│  │  - TaskList │    │  - /jobs    │    │  - R        │    │  - Jobs     │  │
│  │  - Settings │    │  - /stats   │    │  - C#       │    │  - Logs     │  │
│  └─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘  │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                           INTEGRATIONS                                       │
├───────────────┬──────────────┬──────────────┬──────────────┬────────────────┤
│   CRON JOBS   │   WEBHOOKS   │   QUEUES     │   EXTERNAL   │   NOTEBOOKS    │
│   (Python)    │   (API)      │   (Redis)    │   SERVICES   │   (Jupyter)    │
└───────────────┴──────────────┴──────────────┴──────────────┴────────────────┘
```

### Capas del Sistema

| Capa | Tecnología | Descripción |
|------|------------|-------------|
| **Frontend** | React | Interfaz de usuario para gestión visual de tareas |
| **API** | Python/C# | REST API para comunicación entre servicios |
| **Core** | Multi-lenguaje | Motor de scheduling con soporte para Python, R, C# |
| **Storage** | SQL/NoSQL | Persistencia de tareas, jobs y logs |
| **Integration** | Múltiple | Cron jobs, webhooks, colas de mensajes |

### Flujo de Trabajo

1. **Creación de Tarea**: Usuario define tarea desde UI React o API
2. **Validación**: API valida y procesa la solicitud
3. **Scheduling**: Core Engine programa la tarea según configuración
4. **Ejecución**: Scheduler ejecuta en el runtime apropiado (Python/R/C#)
5. **Logging**: Resultados almacenados y notificaciones enviadas

---

## 🚀 Inicio Rápido

### Requisitos Previos

- Python 3.8+
- Node.js 16+
- .NET 6+ (para módulos C#)
- R 4.0+ (para módulos R)
- Docker (opcional)

### Instalación

```bash
# Clonar repositorio
git clone https://github.com/elisaul77/Scheduler.git
cd Scheduler

# Instalar dependencias Python
pip install -r python/requirements.txt

# Instalar dependencias React
cd react && npm install

# Ejecutar aplicación
npm run dev
```

### Con Docker

```bash
docker-compose up --build
```

---

## 📚 Documentación

| Documento | Descripción |
|-----------|-------------|
| [Guía de Instalación](docs/guides/installation.md) | Instrucciones detalladas de setup |
| [API Reference](docs/api/reference.md) | Documentación de endpoints |
| [Arquitectura](docs/architecture/overview.md) | Detalles técnicos del sistema |
| [Contribución](CONTRIBUTING.md) | Guía para contribuidores |

---

## 👨‍💻 Fundador y Desarrollador

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/elisaul77">
        <img src="https://github.com/elisaul77.png" width="100px;" alt="Eli Saul Florez Perez"/><br />
        <sub><b>Eli Saul Florez Perez</b></sub>
      </a><br />
      <sub>Fundador & Lead Developer</sub>
    </td>
  </tr>
</table>

**Contacto:**
- 📧 Email: elisaul77@gmail.com
- 🐙 GitHub: [@elisaul77](https://github.com/elisaul77)

---

## 💖 Apoya el Proyecto

Si **Scheduler** te resulta útil, considera apoyar su desarrollo:

### 🌟 Donaciones Recurrentes

[![GitHub Sponsors](https://img.shields.io/badge/GitHub-Sponsors-pink?style=for-the-badge&logo=githubsponsors)](https://github.com/sponsors/elisaul77)
[![Patreon](https://img.shields.io/badge/Patreon-Support-orange?style=for-the-badge&logo=patreon)](https://patreon.com/elisaul77)

### 💰 Donaciones Únicas

[![PayPal](https://img.shields.io/badge/PayPal-Donate-blue?style=for-the-badge&logo=paypal)](https://paypal.me/eflorezp)
[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow?style=for-the-badge&logo=buymeacoffee)](https://buymeacoffee.com/elisaul77)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-Support-red?style=for-the-badge&logo=kofi)](https://ko-fi.com/elisaul77)

### 🪙 Criptomonedas

| Moneda | Dirección |
|--------|-----------|
| **Bitcoin (BTC)** | `13AJVNugF4CtwX6q5jmtZvM6Qqsei5ag47` |
| **Ethereum (ETH)** | `0xa577f401ba2caae852704168ca49ec12e09088d7` |
| **BSC (BNB)** | `0xa577f401ba2caae852704168ca49ec12e09088d7` |

### 🤝 Otras Formas de Contribuir

- ⭐ **Dale una estrella** al repositorio
- 🐛 **Reporta bugs** y sugiere mejoras
- 📝 **Contribuye con código** o documentación
- 📢 **Comparte** el proyecto con otros desarrolladores

---

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Para contribuir:

1. Fork el repositorio
2. Crea una rama feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -m 'Add: nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

Por favor lee [CONTRIBUTING.md](CONTRIBUTING.md) para más detalles.

---

## 📋 Roadmap

- [ ] 🐍 Módulos Python base para scheduling
- [ ] 📊 Integración con R para data science tasks
- [ ] ⚛️ Dashboard React completo
- [ ] 🔷 Windows Task Scheduler integration (C#)
- [ ] 📓 Tutoriales en Jupyter Notebooks
- [ ] 🐳 Contenedores Docker optimizados
- [ ] 📡 API REST completa
- [ ] 📈 Sistema de métricas y monitoreo

---

## 📄 Licencia

Este proyecto está licenciado bajo la **Licencia MIT**.

```
MIT License

Copyright (c) 2022 Eli Saul Florez Perez

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Agradecimientos

- A la comunidad **Open Source** por su apoyo continuo
- A todos los **contribuidores** que mejoran el proyecto
- A los **sponsors** que hacen posible el desarrollo

---

<div align="center">
  <sub>Hecho con ❤️ por <a href="https://github.com/elisaul77">Eli Saul Florez Perez</a></sub><br/>
  <sub>© 2022 - Presente | Todos los derechos reservados bajo MIT License</sub>
</div>
