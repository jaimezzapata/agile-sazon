# Módulo: Autenticación 🔐

Bienvenido a la documentación del módulo de **Autenticación** del proyecto **Agile Sazón**. Este módulo es el punto de entrada y control de seguridad de la plataforma, encargado de la gestión de accesos, roles, perfiles y registro de usuarios.

---

## 📋 Documentación Requerida

Siguiendo las directrices del [README general](../../README.MD), este módulo cuenta con los siguientes componentes de documentación técnica y de gestión:

| Documento | Descripción | Estado / Enlace |
| :--- | :--- | :--- |
| **Modelo Relacional** | Diagrama Entidad-Relación (Mermaid), diccionario de datos y DDL para Autenticación, Roles y Perfil. | ✅ *Completado* · [docs/modelo_relacional.md](./docs/modelo_relacional.md) |
| **Backlog** | Historias de usuario, requerimientos funcionales y no funcionales, criterios de aceptación y priorización (Sprint Backlog). | ⏳ *En proceso de carga* · `[docs/backlog.md](./docs/backlog.md)` |
| **Informe Técnico** | Descripción del módulo, objetivos, alcance, decisiones arquitectónicas, estado actual y conclusiones. | ⏳ *En proceso de carga* · `[docs/informe.md](./docs/informe.md)` |
| **Wireframes & Prototipos** | Bocetos UI/UX, flujos de navegación y pantallas de acceso diseñadas en Figma. | ⏳ *En proceso de carga* · `[docs/wireframes/](./docs/wireframes/)` |

---

## 👨‍💻 Integrantes del Equipo

### Jaime Zapata Valencia — Líder de Módulo & Desarrollador Full Stack
*Único responsable del diseño, documentación y desarrollo del módulo de autenticación.*

* **Experiencia:**
  * Desarrollador Full Stack con amplia experiencia en el diseño y creación de interfaces de usuario interactivas y aplicaciones web de alto rendimiento.
  * Experiencia consolidada en liderazgo de equipos de desarrollo, arquitectura de software y gestión técnica.
  * Trayectoria en formación técnica y profesional en áreas de ingeniería de software y tecnologías web.

* **Capacidades y Fortalezas:**
  * **Liderazgo y Habilidades Blandas:** Liderazgo técnico de equipos, mentoría, metodologías ágiles (Scrum/Kanban), resolución de problemas complejos y visión estratégica de producto.
  * **Stacks de Desarrollo Full Stack:** Dominio completo de stacks modernos:
    * **MERN** (MongoDB, Express.js, React, Node.js)
    * **PERN** (PostgreSQL, Express.js, React, Node.js)
    * **MEVN** (MongoDB, Express.js, Vue.js, Node.js)
    * **MEAN** (MongoDB, Express.js, Angular, Node.js)
    * **Java Enterprise:** Spring Boot, Spring Security, APIs RESTful.
  * **Bases de Datos:** Diseño, modelado y administración en MySQL, PostgreSQL y Oracle.
  * **Diseño UI/UX y Prototipado:** Figma, Adobe Illustrator, Adobe Photoshop para la construcción de sistemas de diseño y flujos de usuario intuitivos.

* **Contacto / Redes:**
  * **GitHub:** [@jaimezzapata](https://github.com/jaimezzapata)
  * **Correo electrónico:** [zapataval2304@gmail.com](mailto:zapataval2304@gmail.com)

---

## 🛠️ Arquitectura y Stack Tecnológico

El desarrollo de este módulo se plantea en dos fases estratégicas de evolución:

```text
┌────────────────────────────────────────┐       ┌────────────────────────────────────────┐
│         FASE 1: MVP / Prototipo        │  ───► │        FASE 2: Migración Futura        │
│  HTML5 + CSS3 + Vanilla JS + Arrays    │       │     React + Java Spring Boot + SQL     │
└────────────────────────────────────────┘       └────────────────────────────────────────┘
```

### 1. Fase Inicial (Prototipo Funcional / MVP)
* **Frontend:** HTML5 semántico y CSS3 puro con diseño responsivo y accesible.
* **Lógica de Autenticación:** JavaScript Vanilla modular.
* **Persistencia de Datos:** Arreglos locales en memoria y `localStorage` para emular el registro, validación de credenciales, sesiones activas y control de acceso por roles sin dependencias externas inmediatas.

### 2. Fase de Migración (Escalabilidad y Producción)
* **Frontend:** Migración a componentes reactivos con **React** y consumo de servicios API REST.
* **Backend:** Implementación de servicios con **Java** y **Spring Boot** (Spring Security con tokens JWT).
* **Base de Datos:** Persistencia robusta en bases de datos relacionales (**PostgreSQL / MySQL**).

---

## 🌿 Flujo de Trabajo con Git (GitFlow)

En cumplimiento de la metodología establecida en el repositorio central:

1. **Fork del Repositorio:** El trabajo del módulo se ejecuta sobre el fork personal en [github.com/jaimezzapata/agile-sazon](https://github.com/jaimezzapata).
2. **Ramas de Trabajo:** Todo desarrollo de características se desglosa desde `develop` en ramas bajo la convención:
   * `feature/autenticacion-registro`
   * `feature/autenticacion-login`
   * `feature/autenticacion-roles-permisos`
   * `feature/autenticacion-documentacion`
3. **Integración:** Las funcionalidades terminadas y probadas se sincronizan hacia la rama `develop` del proyecto central mediante Pull Requests con previa revisión.
