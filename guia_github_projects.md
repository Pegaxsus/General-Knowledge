# GitHub Projects: guía de referencia

## 1. ¿Qué son los Projects de GitHub?

**GitHub Projects** es una herramienta de planificación y seguimiento del trabajo que permite organizar tareas relacionadas con uno o varios repositorios de GitHub.

La distinción fundamental es:

- **Repository:** almacena y versiona el código y otros archivos.
- **Issues:** registra tareas, incidencias, mejoras y solicitudes.
- **Pull Requests (PR):** propone, revisa e integra cambios en el código.
- **Project:** organiza y supervisa el trabajo mediante vistas, estados, prioridades y otros campos.

## 2. Repository frente a Project

| Característica | Repository | Project |
|---|---|---|
| Función principal | Almacenar y versionar código y archivos | Planificar y gestionar tareas |
| Contenido | Código, ramas, commits, documentación | Issues, Pull Requests y borradores de tareas |
| Organización | Carpetas, archivos y ramas | Tablas, tableros Kanban y cronogramas |
| Alcance | Un repositorio concreto | Puede incluir elementos de varios repositorios |
| Seguimiento | Historial de cambios | Estados, responsables, prioridades y fechas |

## 3. Formas de visualizar un Project

GitHub Projects admite distintas vistas de los mismos elementos:

- **Board (Kanban):** organiza el trabajo en columnas como `Todo`, `In Progress` y `Done`.
- **Table:** presenta tareas en filas con campos como estado, prioridad, responsable o fecha.
- **Roadmap:** presenta elementos en una línea temporal, útil para hitos y planificación.

También se pueden configurar **campos personalizados**, filtros, agrupaciones y determinadas automatizaciones para mantener actualizado el seguimiento.

## 4. Ejemplo práctico: desarrollo de una web

Supongamos que tienes el repositorio `MimoMakers-Web` y creas un Project llamado `MimoMakers - Development`.

| Todo | In Progress | Done |
|---|---|---|
| Integrar formulario de contacto | Diseñar catálogo | Configurar repositorio |
| Optimizar SEO | Crear fichas de producto | Crear página principal |

Cada tarea puede asociarse a una **Issue** del repositorio. Cuando se desarrolla una funcionalidad, se puede vincular su **Pull Request** con la Issue correspondiente para mantener la trazabilidad entre planificación y código.

### Flujo habitual

1. Registrar una necesidad en una **Issue**.
2. Incorporar la Issue al **Project** y asignarle estado, prioridad y responsable.
3. Moverla a `In Progress` cuando comience el trabajo.
4. Desarrollar los cambios en una rama y abrir un **Pull Request**.
5. Revisar e integrar el PR.
6. Cerrar la Issue y actualizar el Project a `Done` (manualmente o mediante automatizaciones configuradas).

## 5. ¿A quién pertenecen los Projects?

Los **GitHub Projects modernos** pertenecen a una **cuenta de usuario o a una organización**, no directamente a un repositorio.

Esto permite, por ejemplo, crear un único Project `MimoMakers` y utilizarlo para coordinar tareas de los repositorios:

```text
Cuenta u organización GitHub
├── Project: MimoMakers
│   ├── Issue del repositorio MimoMakers-Web
│   ├── Issue del repositorio MimoMakers-Backend
│   └── PR del repositorio MimoMakers-Web
└── Repositorios
    ├── MimoMakers-Web
    ├── MimoMakers-Backend
    └── MimoMakers-Docs
```

El Project centraliza la planificación, mientras que cada Issue o Pull Request sigue perteneciendo a su repositorio de origen.

## 6. ¿Cuándo conviene utilizar Projects?

| Situación | Enfoque recomendado |
|---|---|
| Repositorio pequeño con pocas tareas | Issues sin necesidad de crear un Project |
| Desarrollo con varias funcionalidades pendientes | Project con tablero Kanban |
| Trabajo con fechas e hitos | Project con vista Roadmap |
| Varios repositorios relacionados | Un Project que agrupe Issues y PR de distintos repositorios |
| Necesidad de seguimiento detallado | Project con campos personalizados y automatizaciones |

## 7. Resumen rápido

> **Repository = dónde está el código.**  
> **Issues = qué tareas o problemas hay.**  
> **Pull Requests = qué cambios se proponen o integran.**  
> **Projects = cómo se planifica y supervisa el conjunto del trabajo.**

### Referencia oficial

- [GitHub Docs — About Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)
- [GitHub Docs — Planning and tracking with Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects)
