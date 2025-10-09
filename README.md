## Capítulo VI: Product Implementation, Validation & Deployment

### 6.1. Software Configuration Management

#### 6.1.1. Software Development Environment Configuration

**Gestión de Proyectos:**

- Discord: Se implementó como plataforma principal para la comunicación sincrónica del equipo de desarrollo, facilitando canales especializados para discusiones técnicas, reuniones virtuales y comunicación de avances del proyecto en tiempo real.
- WhatsApp: Se empleó como canal complementario de comunicación para mantener conectividad continua entre los integrantes del equipo, particularmente para coordinaciones urgentes y notificaciones rápidas.
- GitFlow: Se adoptó como metodología de gestión de ramas en el control de versiones, proporcionando una estructura organizada para el manejo de features, releases y hotfixes, lo cual optimizó la colaboración en equipo y garantizó la integridad del código mediante flujos de trabajo estandarizados.
- Trello: Se utilizó como sistema de gestión visual de tareas, permitiendo identificar y categorizar actividades pendientes, completadas y programadas para entregas futuras, facilitando el seguimiento del progreso del proyecto mediante tableros Kanban.

**Gestión de Requisitos:**

- Miro: Se empleó para la creación colaborativa de mapas mentales, diagramas de afinidad y canvas de modelo de negocio, facilitando la visualización y organización estructurada de requisitos funcionales y no funcionales, características del producto y objetivos estratégicos del proyecto.
- Lucidchart: Se utilizó como herramienta para la elaboración de diagramas de clases.
- Vertabelo: Se utilizó como herramienta para la elaboración de los diagramas de base de datos.

**Diseño de Experiencia e Interfaz de Usuario:**

- Figma: Se implementó como plataforma principal para el diseño de interfaz de usuario (UI) y experiencia de usuario (UX) del sistema SmartParking, permitiendo la creación colaborativa de prototipos interactivos, wireframes, mockups de alta fidelidad y sistemas de diseño que orientaron el desarrollo del producto final.
- UXPressia: Se empleó como herramienta especializada para la elaboración de artefactos de investigación de usuarios, incluyendo customer journey maps, user personas y empathy maps, permitiendo visualizar y analizar profundamente la experiencia del usuario para fundamentar decisiones de diseño centradas en el usuario.

**Desarrollo de Software:**

- Visual Studio Code: Se utilizó como editor principal para la documentación técnica del proyecto, elaboración del informe y desarrollo de componentes web, aprovechando su extensibilidad mediante plugins y soporte multi-lenguaje.

**Frameworks y Lenguajes de Programación:**

- React: Framework basado en JavaScript utilizado para el desarrollo de la Landing Page, aprovechando su arquitectura basada en componentes reutilizables y virtual DOM para optimizar el rendimiento.
- Java: Lenguaje de programación orientado a objetos utilizado para el desarrollo del backend del sistema, seleccionado por sus características de portabilidad multiplataforma, robustez en manejo de excepciones y ecosistema maduro de frameworks empresariales.
- Next.js: Framework basado en React empleado para la construcción de la aplicación web principal y landing page, proporcionando renderizado del lado del servidor (SSR), generación de sitios estáticos (SSG), enrutamiento automático y optimización de rendimiento, lo que mejora tanto la experiencia del usuario como el posicionamiento SEO.
- React Native: Framework multiplataforma desarrollado por Meta, utilizado para la construcción de aplicaciones móviles nativas para Android e iOS, permitiendo compartir gran parte del código entre plataformas mientras se mantiene el rendimiento y la apariencia nativa, optimizando así el tiempo de desarrollo y mantenimiento.

**Documentación de Software:**

- GitHub: Se implementó como plataforma centralizada para el control de versiones del código fuente, gestión de issues, pull requests y documentación técnica del proyecto mediante archivos README.md que detallan arquitectura, instalación, configuración y guías de contribución.
- Structurizr: Se empleó para la elaboración de diagramas C4 (Context, Container, Component, Code) del sistema, utilizando su DSL (Domain-Specific Language) basado en sintaxis declarativa para generar documentación arquitectónica visual que representa la estructura estática del sistema en diferentes niveles de abstención.

#### 6.1.2. Source Code Management

La administración y estructuración de las modificaciones del código se implementaron mediante una organización corporativa en la plataforma GitHub, estableciendo repositorios diferenciados por componente del sistema:

**Organización:** https://github.com/Lorem-Ipsum-UPC  
**Repositorio Landing Page:** https://github.com/Lorem-Ipsum-UPC/Landing-Page  
**Repositorio Aplicación Web Frontend:** https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend
**Repositorio Aplicación Móvil Frontend:** En desarrollo  
**Repositorio Backend:** En desarrollo

**Estructura de Ramificación**  
Cada repositorio implementa una estrategia de ramificación basada en GitFlow:

- main: Rama de producción que almacena exclusivamente versiones estables y validadas del sistema, listas para despliegue en entornos productivos.
- develop: Rama de integración continua donde se consolidan las características en desarrollo antes de su promoción a producción.
- feature: Ramas dedicadas al desarrollo de funcionalidades específicas solicitadas por los usuarios, tanto para la landing page como para la aplicación web.

**Nomenclatura de Ramas:** Se adopta la convención `[rama]/[descripción-funcionalidad]`

**Convenciones de Commits**  
Los mensajes de commit siguen el estándar "Conventional Commits" versión 1.0.0, implementando la estructura: `<type>[scope opcional]: <description>`

**Componentes del mensaje:**

- type: Categoría del cambio realizado (feat, fix, docs, etc.)
- scope: Contexto o módulo afectado por el cambio
- description: Resumen conciso de las modificaciones implementadas

**Tipología de Commits**  
La convención garantiza que cada mensaje refleje con precisión la naturaleza del cambio:

- feat: Implementación de nueva funcionalidad
- fix: Corrección de defectos o errores
- docs: Modificaciones en documentación
- style: Ajustes de formato que no alteran la lógica (espaciado, puntuación, etc.)
- refactor: Reestructuración de código sin modificar funcionalidad ni corregir errores
- chore: Tareas de mantenimiento rutinarias (actualización de dependencias, configuración de archivos .gitignore)
- test: Adición o corrección de pruebas unitarias o de integración
- build: Cambios que afectan el proceso de compilación o construcción del proyecto
- revert: Reversión de un commit anterior, especificando el hash del commit revertido

Esta metodología asegura trazabilidad completa del historial de cambios y facilita la generación automática de changelogs.

#### 6.1.3. Source Code Style Guide & Conventions

**General**  
Para todos los lenguajes, se aplicarán las siguientes directrices de nomenclatura:

- **Convención en inglés**: Todos los nombres de variables, funciones, métodos, clases y archivos se nombrarán en inglés.
- **Convención de nombres**:
  - **camelCase**: Para nombres de variables, funciones y métodos.
  - **PascalCase**: Para nombres de clases y componentes.
  - **snake_case**: Para nombres de archivos.

**Java:** [https://google.github.io/styleguide/javaguide.html](https://google.github.io/styleguide/javaguide.html)

**Convenciones de Java:**

- Los nombres de clases y tipos deben ser sustantivos en mayúscula inicial.
- Los nombres de los métodos deben ser minúsculas.
- El nombre de las variables debe ser en minúsculas y usar camelCase.
- Para las sentencias `if`, `else`, `for`, `do` y `while` se deben usar `{ }`.
- Los nombres de variables que son constantes deben ir en mayúsculas.

**JavaScript:** [https://google.github.io/styleguide/jsguide.html](https://google.github.io/styleguide/jsguide.html)

**Convenciones de JavaScript:**

- Usar camelCase para variables y funciones.
- Usar PascalCase para clases y constructores.
- Usar MAYÚSCULAS_CON_GUIONES_BAJOS para constantes.
- Usar `let` y `const` para declarar variables (evitar `var`).
- Declarar las variables al inicio de su ámbito.
- Incluir punto y coma al final de cada instrucción.
- Usar `//` para comentarios de una línea y `/* */` para bloques de comentarios.
- Escribir comentarios descriptivos en componentes, servicios y secciones complejas.
- Aplicar principios de programación reactiva y patrones de diseño adecuados.

**React:** [https://react.dev/learn/writing-markup-with-jsx](https://react.dev/learn/writing-markup-with-jsx)

**Convenciones de React:**

- **Nombres de componentes**: Usar PascalCase para componentes, por ejemplo, `UserProfile`.
- **Nombres de archivos**: Los archivos de componentes deben nombrarse en PascalCase con extensión `.jsx` o `.tsx`, por ejemplo, `UserProfile.jsx`.
- **Nombres de props**: Declarar props usando camelCase en JavaScript.
- **Prefijos en componentes**: Los componentes de uso único deben llevar el prefijo `The`, por ejemplo, `TheHeader`. Los componentes base reutilizables deben llevar el prefijo `Base`, como `BaseButton`.
- **Keys en listas**: Siempre proporcionar una `key` única al renderizar listas mediante `.map()`.
- **Hooks**: Declarar hooks al inicio del componente funcional y seguir las reglas de hooks de React.
- **Funciones de estado**: Utilizar `useState` y `useEffect` apropiadamente, evitando efectos secundarios innecesarios.

**Next.js:** [https://nextjs.org/docs/app/building-your-application/routing](https://nextjs.org/docs/app/building-your-application/routing)

**Convenciones de Next.js:**

- **Estructura de carpetas**: Utilizar el App Router (carpeta `app/`) para enrutamiento basado en archivos.
- **Nombres de archivos especiales**: Respetar convenciones como `page.tsx`, `layout.tsx`, `loading.tsx`, `error.tsx`.
- **Server Components por defecto**: Los componentes son Server Components a menos que se especifique `'use client'`.
- **Client Components**: Incluir directiva `'use client'` en la primera línea para componentes que requieren interactividad del cliente.
- **Metadata**: Exportar objeto `metadata` o función `generateMetadata` para SEO.
- **API Routes**: Crear API routes en `app/api/` usando convenciones de nombres de archivo.
- **Optimización de imágenes**: Utilizar el componente `<Image>` de Next.js para optimización automática.

**React Native:** [https://reactnative.dev/docs/style](https://reactnative.dev/docs/style)

**Convenciones de React Native:**

- **Nombres de componentes**: Usar PascalCase para componentes nativos, por ejemplo, `UserProfile`.
- **Nombres de archivos**: Los archivos deben nombrarse en PascalCase con extensión `.jsx` o `.tsx`, por ejemplo, `UserProfile.tsx`.
- **Estilos**: Crear objetos de estilo usando `StyleSheet.create()` para optimización de rendimiento.
- **Nombres de estilos**: Utilizar camelCase para propiedades de estilo, por ejemplo, `container`, `buttonText`.
- **Evitar estilos inline**: Preferir `StyleSheet` sobre estilos inline para mejor rendimiento.
- **Componentes platform-specific**: Usar extensiones `.ios.tsx` y `.android.tsx` para código específico de plataforma.
- **Hooks nativos**: Utilizar hooks como `useWindowDimensions`, `useColorScheme` para responsividad.
- **Comentarios de documentación**: Usar `//` para comentarios de línea única y `/* */` para bloques multilínea.
- **Componentes funcionales**: Priorizar componentes funcionales con hooks sobre componentes de clase.

#### 6.1.4. Software Deployment Configuration

Para configurar la landing page previo al despliegue del proyecto, primero tenemos que hacer lo siguiente en el proyecto:

Una vez que se tiene listo el proyecto en React, se ejecuta el comando **npm run build** en la terminal, lo que hace este comando es preparar el proyecto para produccion, asi creando una carpeta llamada **build**, que produce archivos estaticos listo para servir, empaqueta codigo, elimina codigo muerto, entre otras funciones.

<img src="assets/chapter-6/step1-before.png" alt="npm run build">

<img src="assets/chapter-6/step2-preview.png" alt="d">

Luego entro a la plataforma que usare para desplegar mi Landing Page que en este caso será **Netlify**. Entro a la pagina e inicio sesion con Github para que automaticamente se importen los repositorios que tengo, incluido el de la Landing Page que voy a desplegar

<img src="assets/chapter-6/step3-preview.png" alt="">

Una vez en el dashboard de Netlify, se hace click en **Add New Project** para importar el repositorio, luego se hace click en **Import an existing project**, tomando en cuenta que el repositorio ya esta listo habian realizado los pasos previos.

<img src="assets/chapter-6/step5-preview.png" alt="">

Aca se elige la herramienta desde donde importaras el proyecto, que en nuestro caso es **Github**

<img src="assets/chapter-6/step6-preview.png" alt="">

### 6.2. Landing Page, Services & Applications Implementation

#### 6.2.1. Sprint 1

##### 6.2.1.1. Sprint Planning 1

| Sprint #                           | Sprint 1                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sprint Planning Background**     |
| **Date**                           | 03 / 10 / 2025                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Time**                           | 15 : 00 horas                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Location**                       | Discord                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Prepared By**                    | Lorem Ipsum                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Attendees**                      | Calisaya Sánchez, Juan Jesús <br> David Polanco, Alessandro Alonso <br> Espinoza Delgado, Bárbara Antonella <br> Serrano Ircañaupa, Nelson Elias <br> Sotil Vasquez, Tyrone Raí                                                                                                                                                                                                                                               |
| **Sprint-0 Review Summary**        | Previamente al inicio del Sprint 1, el equipo acordó frameworks para cada aplicación, funcionalidades a realizar, guias de estilo y asignación de tareas.                                                                                                                                                                                                                                                                     |
| **Sprint-0 Retrospective Summary** | Como puntos de mejora se reconoce la necesidad de que todo el equipo tenga en claro las restricciones y limites del product backlog para evitar el desarrollo de funcionalidades extras no acordadas.                                                                                                                                                                                                                         |
| **Sprint-1 Goal**                  | La meta de este primer Sprint es desarrollar una landing page completa y una primera versión de la aplicación web para para dueños de estacionamientos. Esto permitirá que los visitantes comprendan el producto y que los dueños tengan un MVP. Se confirmará cuando la landing page esté desplegada sin errores, funcione en todos los dispositivos y los dueños puedan registrarse, crear y visualizar su estacionamiento. |
| **Sprint-1 Velocity**              | 42 hours                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Sprint-1 Story Points**          | 44                                                                                                                                                                                                                                                                                                                                                                                                                            |

##### 6.2.1.2. Aspect Leaders and Collaborators

Con el fin de garantizar una comunicación efectiva y una ejecución eficiente de las tareas, se desarrolló la **matriz LACX (Leadership and Collaboration Matrix)**, la cual permite identificar qué integrante del equipo lidera cada componente del proyecto y quiénes colaboran en su desarrollo.

En esta primera iteración se abordaron los siguientes aspectos principales:

- **Aspect Name 1:** Landing Page
- **Aspect Name 2:** Web App Frontend (Dueños)
- **Aspect Name 3:** RESTful API - Backend Básico
- **Aspect Name 4:** Infraestructura y Despliegue
- **Aspect Name 5:** Documentación

| Team Member                             | GitHub User | Aspect Name 1 | Aspect Name 2 | Aspect Name 3 | Aspect Name 4 | Aspect Name 5 |
| --------------------------------------- | :---------: | :-----------: | :-----------: | :-----------: | :-----------: | :-----------: |
| **Calisaya Sánchez, Juan Jesús**        | JuanCali999 |       C       |       C       |       C       |       C       |       C       |
| **David Polanco, Alessandro Alonso**    | Alesso2805  |       L       |       L       |       C       |       C       |       C       |
| **Espinoza Delgado, Bárbara Antonella** |  MesSobble  |       C       |       C       |       C       |       C       |       L       |
| **Serrano Ircañaupa, Nelson Elias**     |  NelsonUPC  |       C       |       C       |       L       |       C       |       C       |
| **Sotil Vasquez, Tyrone Raí**           |  Tyrone-J   |       C       |       C       |       C       |       L       |       C       |

##### 6.2.1.3. Sprint Backlog 1

Durante este sprint, se trabajó en desarrollar las user stories referentes a la landing page, funcionalidades basicas del frontend y parte del backend.

La gestión del sprint se llevó a cabo utilizando la herramienta Trello, donde se registraron todas las tareas, su estado y responsables.

<img src="assets/chapter-6/TrelloSprint1.png" alt="Trello Sprint1">

Trello: [Link de Trello](https://trello.com/b/7BD2h15m/sprint-1)

| **User Story Id** | **User Story Title**                      | **Task Id** | **Task Title**                                  | **Task Description**                                              | **Estimation (Hours)** | **Assigned To**  | **Status** |
| ----------------- | ----------------------------------------- | ----------- | ----------------------------------------------- | ----------------------------------------------------------------- | ---------------------- | ---------------- | ---------- |
| US01              | Sección hero con propuesta de valor IoT   | T01         | Diseño de sección hero                          | Crear estructura y contenido visual para comunicar el valor IoT   | 1                      | Alessandro David | Done       |
| US02              | Barra de navegación intuitiva             | T02         | Implementar navbar responsive                   | Diseñar y desarrollar barra de navegación clara y adaptable       | 1                      | Alessandro David | Done       |
| US03              | Acceso directo a registro desde landing   | T03         | Crear botones de registro                       | Implementar CTA visibles para registro de Conductor o Propietario | 1                      | Alessandro David | Done       |
| US04              | Registro diferenciado por tipo de usuario | T04         | Desarrollar formulario de registro              | Crear registro con selección de rol y validaciones                | 3                      | Juan Calisaya    | Done       |
| US05              | Inicio de sesión unificado                | T05         | Implementar login con JWT                       | Desarrollar inicio de sesión con redirección según rol            | 3                      | Juan Calisaya    | Done       |
| US07              | Perfil de propietario                     | T06         | Diseñar vista de perfil de propietario          | Implementar gestión de información comercial y contacto           | 3                      | Alessandro David | Done       |
| US18              | Registro de estacionamiento               | T07         | Crear formulario de registro de estacionamiento | Permitir al propietario registrar su local en la plataforma       | 5                      | Juan Calisaya    | Done       |
| US19              | Configuración simple de espacios          | T08         | Implementar editor de espacios                  | Definir cantidad, horarios y tarifas de estacionamiento           | 5                      | Alessandro David | Done       |
| US20              | Visualizar reservas de mi estacionamiento | T09         | Crear panel de reservas del propietario         | Mostrar reservas activas y programadas con detalles               | 5                      | Alessandro David | Done       |
| US32              | Panel web para propietarios               | T10         | Crear panel del propietario                     | Mostrar Panel web para gestión de estacionamientos                | 7                      | Alessandro David | Done       |
| TS01              | API de autenticación                      | T11         | Crear endpoints de autenticación                | Desarrollar endpoints para login, registro y refresh token        | 3                      | Nelson Serrano   | Done       |
| TS02              | API CRUD de estacionamientos              | T12         | Desarrollar API CRUD estacionamientos           | Crear endpoints para CRUD de estacionamientos y espacios          | 5                      | Nelson Serrano   | Done       |

##### 6.2.1.4. Development Evidence for Sprint Review

En esta sección, se presentan los commits realizados en el repositorio de la landing page y en el repositorio del frontend de la web en GitHub. Estos commits reflejan el progreso y las mejoras implementadas durante el Sprint 1, proporcionando una visión detallada de las actividades de desarrollo y las contribuciones del equipo.

**Repositorio de Landing Page:**  
[https://github.com/Lorem-Ipsum-UPC/Landing-Page](https://github.com/Lorem-Ipsum-UPC/Landing-Page)

---

| **Repository**                                                  | **Branch** | **Commit Id**                              | **Commit Message**                                                                                                                                                                                                                                                                                                                                                               | **Commit Message Body** | **Committed on (Date)** |
| --------------------------------------------------------------- | ---------- | ------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------- | ----------------------- |
| [Landing Page](https://github.com/Lorem-Ipsum-UPC/Landing-Page) | `main`     | `b21417e331bcb86c0b996f2253d4f449bf31ea47` | [Initialize project using Create React App](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/b21417e331bcb86c0b996f2253d4f449bf31ea47 "Initialize project using Create React App")                                                                                                                                                                                         | -                       | 3 de Octubre, 2025      |
|                                                                 |            | `ec59e43dbb0866509dac12ef6b85db1f2d51e876` | [feat: add ParkeoYaLanding component with complete landing page structure and features](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/79697a3d8b01fa93b027797ca628257e3be4c7b9 "feat: add ParkeoYaLanding component with complete landing page structure and features")                                                                                                 | -                       | 3 de Octubre, 2025      |
|                                                                 |            | `ec59e43dbb0866509dac12ef6b85db1f2d51e876` | [style: update case study grid and card styles for improved responsiveness and layout](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/ec59e43dbb0866509dac12ef6b85db1f2d51e876 "style: update case study grid and card styles for improved responsiveness and layout")                                                                                                   | -                       | 3 Octubre, 2025         |
|                                                                 |            | `cf4d7ee04ecd284bc3b1ba29387076d7c3ed3441` | [feat: enhance pricing grid responsiveness and add data attribute for selected plan](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/cf4d7ee04ecd284bc3b1ba29387076d7c3ed3441 "feat: enhance pricing grid responsiveness and add data attribute for selected plan")                                                                                                       | -                       | 3 Octubre, 2025         |
|                                                                 |            | `dfc137bf19cb363e703d9bc652a377d87e5a2d2a` | [fix: remove unnecessary peer dependencies from package-lock.json](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/dfc137bf19cb363e703d9bc652a377d87e5a2d2a "fix: remove unnecessary peer dependencies from package-lock.json")                                                                                                                                           | -                       | 4 Octubre, 2025         |
|                                                                 |            | `9b70a89bca51df1b1efc55cf3d15b3a8ff33da3b` | [feat(i18n): integrate internationalization with i18next and add language selector](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/9b70a89bca51df1b1efc55cf3d15b3a8ff33da3b "feat(i18n): integrate internationalization with i18next and add language selector")                                                                                                         | -                       | 4 Octubre, 2025         |
|                                                                 |            | `c43a55726b967e9fc99fea859a98873059d1f92a` | [fix: update package-lock.json to remove unused dependencies and update versions](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/c43a55726b967e9fc99fea859a98873059d1f92a "fix: update package-lock.json to remove unused dependencies and update versions")                                                                                                             | -                       | 4 Octubre, 2025         |
|                                                                 |            | `29ad504394dd512dcd02516ddbac3aa3f360f5c5` | [feat: add TypeScript as a dev dependency and update its version](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/29ad504394dd512dcd02516ddbac3aa3f360f5c5 "feat: add TypeScript as a dev dependency and update its version")                                                                                                                                             | -                       | 4 Octubre, 2025         |
|                                                                 |            | `db39fdf22bacd6b3b0f33ebb377df341f6d11a32` | [fix: downgrade i18next and react-i18next to compatible versions](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/db39fdf22bacd6b3b0f33ebb377df341f6d11a32 "fix: downgrade i18next and react-i18next to compatible versions")                                                                                                                                             | -                       | 4 Octubre, 2025         |
|                                                                 |            | `acfb88e881081f11dd05d8085e350e9baafdad56` | [fix: update react-i18next to version 12.3.1 and adjust CSS media queries for better responsiveness](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/acfb88e881081f11dd05d8085e350e9baafdad56 "fix: update react-i18next to version 12.3.1 and adjust CSS media queries for better responsiveness")                                                                       | -                       | 4 Octubre, 2025         |
|                                                                 |            | `d91e64df56d9f483502ff0ce00c4fd4f0af5716b` | [fix: remove language flags from LanguageSelector component](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/d91e64df56d9f483502ff0ce00c4fd4f0af5716b "fix: remove language flags from LanguageSelector component")                                                                                                                                                       | -                       | 4 Octubre, 2025         |
|                                                                 |            | `64532b5dbea3b2b7859ebc5464589cc0ad2b5902` | [fix: update media query breakpoints for navigation and mobile menu styles; remove unused badge elements from hero and section headers](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/64532b5dbea3b2b7859ebc5464589cc0ad2b5902 "fix: update media query breakpoints for navigation and mobile menu styles; remove unused badge elements from hero and section headers") | -                       | 4 Octubre, 2025         |
|                                                                 |            | `4860bd3bba8ca78dfc65f31d68ce8cb469bd7954` | [fix: adjust alignment in contact methods and remove unused badge element from contact section](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/4860bd3bba8ca78dfc65f31d68ce8cb469bd7954 "fix: adjust alignment in contact methods and remove unused badge element from contact section")                                                                                 | -                       | 5 Octubre, 2025         |
|                                                                 |            | `b276c50f2effb2b7b1b41b8782a65f194fb3ecf4` | [fix: enhance contact form validation and improve user experience with dynamic error messages](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/b276c50f2effb2b7b1b41b8782a65f194fb3ecf4 "fix: enhance contact form validation and improve user experience with dynamic error messages")                                                                                   | -                       | 5 Octubre, 2025         |
|                                                                 |            | `f492967a9d662b59daa1435dfe5aaaad562a6e5c` | [fix: center align contact method elements and improve text styling for better readability](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/f492967a9d662b59daa1435dfe5aaaad562a6e5c "fix: center align contact method elements and improve text styling for better readability")                                                                                         | -                       | 5 Octubre, 2025         |
|                                                                 |            | `90942e52e0be554eabeb3649fdf15c828776d499` | [fix: replace buttons with links for login and registration; improve accessibility and styling](https://github.com/Lorem-Ipsum-UPC/Landing-Page/commit/90942e52e0be554eabeb3649fdf15c828776d499 "fix: replace buttons with links for login and registration; improve accessibility and styling")                                                                                 | -                       | 8 Octubre, 2025         |

**Repositorio de Frontend Web:**

[https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend](https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend)

---

| **Repository**                                                       | **Branch** | **Commit Id**                              | **Commit Message**                                                                                                                                                                                                                                                                                        | **Commit Message Body** | **Committed on (Date)** |
| -------------------------------------------------------------------- | ---------- | ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------- | ----------------------- |
| [Frontend Web](https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend) | `main`     | `5b3acff2c96caeb64fc02a974ff9ca0f087c1905` | [first commit](https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend/commit/5b3acff2c96caeb64fc02a974ff9ca0f087c1905 "first commit")                                                                                                                                                                       | -                       | 6 de Octubre, 2025      |
|                                                                      |            | `bba12d51e01ac295285ec8f47facb4b18749f56d` | [fix(deps): Fix dependencies to run the project](https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend/commit/bba12d51e01ac295285ec8f47facb4b18749f56d "fix(deps): Fix dependencies to run the project")                                                                                                   | -                       | 6 de Octubre, 2025      |
|                                                                      |            | `cbabe01e040cf8c5be567e9c01f43e13b594d0bd` | [feat: implement space management page with real-time IoT sensor monitoring and status filtering](https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend/commit/cbabe01e040cf8c5be567e9c01f43e13b594d0bd "feat: implement space management page with real-time IoT sensor monitoring and status filtering") | -                       | 6 Octubre, 2025         |
|                                                                      |            | `57d72a141cde1263a98b0bace80014ca498ecd93` | [Merge branch 'main' of https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend](https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend/commit/57d72a141cde1263a98b0bace80014ca498ecd93 "Merge branch 'main' of https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend")                                         | -                       | 6 Octubre, 2025         |
|                                                                      |            | `6f678c13a163f3d126d8c983e1c20126e9b39199` | [fix: resolve version conflict for react-is in package-lock.json](https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend/commit/6f678c13a163f3d126d8c983e1c20126e9b39199 "fix: resolve version conflict for react-is in package-lock.json")                                                                 | -                       | 6 Octubre, 2025         |
|                                                                      |            | `166dfb6bdf8711b01d698063f736e24765f51243` | [refactor: rename pages and update navigation links for consistency](https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend/commit/166dfb6bdf8711b01d698063f736e24765f51243 "refactor: rename pages and update navigation links for consistency")                                                           | -                       | 6 Octubre, 2025         |
|                                                                      |            | `54023ffeb3c53ec4f71b1cfc7a2e5199e03c161e` | [feat: add onboarding steps for capacity, schedule, basic info, pricing, and location pages](https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend/commit/54023ffeb3c53ec4f71b1cfc7a2e5199e03c161e "feat: add onboarding steps for capacity, schedule, basic info, pricing, and location pages")           | -                       | 6 Octubre, 2025         |
|                                                                      |            | `f35263b605c3a2b02399b4762a928c5a7ae6f6bf` | [feat: update UI colors and styles across various components for consistency](https://github.com/Lorem-Ipsum-UPC/parkeoya-frontend/commit/f35263b605c3a2b02399b4762a928c5a7ae6f6bf "feat: update UI colors and styles across various components for consistency")                                         | -                       | 7 Octubre, 2025         |

---

##### 6.2.1.5. Testing Suite Evidence for Sprint Review

En esta sección se explica y presenta el conjunto de Unit Tests, Integration Tests y Acceptance Tests automatizados, para Web Services relacionados con los User Stories especificados en el Sprint. 

#### Repositorio de Testing

**Repositorio:** [[https://github.com/Lorem-Ipsum-UPC/parkeoya-testing](https://github.com/Lorem-Ipsum-UPC/parkeoya-testing)](https://github.com/Lorem-Ipsum-UPC/ParkeoYa-AcceptanceTests)

Este repositorio contiene la suite completa de pruebas para ParkeoYa, incluyendo:
- **Unit Tests**: Pruebas unitarias para componentes de autenticación, gestión de estacionamientos y frontend
- **Integration Tests**: Pruebas de integración API y frontend-backend
- **Acceptance Tests (BDD)**: Pruebas con enfoque BDD utilizando Gherkin para User Stories US04 y US18
- **Configuración CI/CD**: Pipeline automatizado de testing con Jest y Cucumber

#### Testing Evidence Commits

| **Repository** | **Branch** | **Commit Id** | **Commit Message** | **Commit Message Body** | **Committed on (Date)** |
|----------------|------------|---------------|-------------------|-------------------------|------------------------|
| parkeoya-testing | main | b8e02eb | testing suite evidence for sprint review documentation | Comprehensive documentation for testing suite evidence including unit tests, integration tests, and acceptance tests with BDD approach for Sprint 1 review process. | 08/10/2025 |
| parkeoya-testing | main | 926c61 | feat: acceptance tests sprint1 | Implementation of acceptance tests for Sprint 1 including BDD scenarios with Gherkin feature files for user registration (US04) and parking registration (US18) user stories. | 08/10/2025 |
| parkeoya-testing | main | 2283e79 | feat: integration tests sprint1 | Development of integration tests for Sprint 1 covering API endpoints, database connectivity, and frontend-backend communication validation. | 08/10/2025 |
| parkeoya-testing | main | 29c1d46 | feat: unit tests sprint1 | Creation of comprehensive unit tests for Sprint 1 including authentication services, parking management components, and frontend form validation. | 08/10/2025 |
| parkeoya-testing | main | 394af22 | feat: config archives and package json | Configuration setup for testing environment including Jest configuration, Cucumber setup, package.json dependencies, and CI/CD pipeline integration. | 08/10/2025 |


#### Responsive Testing Evidence

Adicionalmente, se realizaron pruebas manuales de compatibilidad y responsividad en la Landing Page para garantizar el funcionamiento óptimo en diferentes dispositivos y navegadores:

**Landing Page en computadoras de escritorio**
<img width="1510" height="618" alt="image" src="https://github.com/user-attachments/assets/86a526d2-9322-499a-a6a0-6b3527065552" />

**Landing Page en teléfonos**
<img width="320" height="800" alt="image" src="https://github.com/user-attachments/assets/2519a090-a05f-447a-bf7d-f6c19ab1cefe" />

**Landing Page en tablets**
<img width="885" height="885" alt="image" src="https://github.com/user-attachments/assets/306f9516-09fb-4349-9cb2-253339991e1f" />

##### 6.2.1.6. Execution Evidence for Sprint Review

En este sprint logramos, como primera fase de nuestro producto final, desarrollar nuestra landing page usando React y la capa frontend de nuestra web en NextJS. También se implementó un diseño responsive para dispositivos Android e iOS, y el respectivo despliegue de ambos productos se realizó en Netlify.

### Landing Page

<img src="assets/chapter-6/landingpage.png" alt="Landing Page">

### Frontend Web

<img src="assets/chapter-6/login.png" alt="Login">
<img src="assets/chapter-6/register.png" alt="Register">
<img src="assets/chapter-6/first-step.png" alt="First Step">
<img src="assets/chapter-6/second-step.png" alt="Second Step">
<img src="assets/chapter-6/third-step.png" alt="Third Step">
<img src="assets/chapter-6/fourth-step.png" alt="Fourth Step">
<img src="assets/chapter-6/fifth-step.png" alt="Fifth Step">
<img src="assets/chapter-6/dashboard.png" alt="IoT Spaces">
<img src="assets/chapter-6/iot-spaces.png" alt="Commits Front Web">
<img src="assets/chapter-6/reservations.png" alt="Reservations">
<img src="assets/chapter-6/finances.png" alt="Finances">
<img src="assets/chapter-6/reviews.png" alt="Reviews">
<img src="assets/chapter-6/config.png" alt="Configuration">

##### 6.2.1.7. Services Documentation Evidence for Sprint Review

En el alcance del Sprint 1 se logró desarrollar la landing page y el frontend web, por lo que no se evidencia el empleo de web services.

##### 6.2.1.8. Software Deployment Evidence for Sprint Review

Se adjuntan links y procedimiento del despliegue (realizado en Netfliy y Vercel) tanto del Landing page como de la capa Frontend de la App Web:

#### Landing Page

https://parkeoya-lorem-ipsum.netlify.app/

Para configurar el despliegue del la Landing Page, seguimos los pasos detallados a continuación utilizando Netlify como plataforma:

Primero iniciamos sesion con Github para que se muestren todos los repositorios disponibles para importar y desplegar y seleccionamos la Organización y luego el repositorio a desplegar

<img src="assets/chapter-6/deploy1.png" alt="Imagen deploy paso 1">

Procedemos a desplegar el repositorio de nuestra Landing page

<img src="assets/chapter-6/deploy3.png" alt="Imagen deploy paso 3">

Y listo! Nos mandara a una seccion de Despliegues donde podremos ver el log del despliegue en tiempo real para ver si hay algun error durante el despliegue (pueden haber errores por dependencias que sean muy actuales y se tiene que hacer un downgrade de las mismas para que el despliegue sea compatible y efectivo).

<img src="assets/chapter-6/deploy4.png" alt="Imagen deploy paso 4">

A continuación podemos ver todas las instancias de despliegues que existen debido a los cambios que hemos ido realizando en el repositorio de Landing Page, por ello es que por cada cambio que se realiza, automaticamente Netlify despliega de nuevo el repositorio con los mas recientes cambios

<img src="assets/chapter-6/deploy5.png" alt="Imagen deploy paso 5">

Una vez que entremos a la opción de la instancia de nuestro despliegue que diga "Publicado" o "Published", podremos ver el boton de "Open production deploy" que es el link ya oficial de nuestro despliegue y abajo se puede mostrar un resumen del despliegue

<img src="assets/chapter-6/deploy6.png" alt="Imagen deploy paso 6">

Y abajo de ese resumend del despliegue, podremos ver el log del despliegue y verificar que todo haya ido de acorde, si hubo un problema deberia corregirse e intentar desplegar de nuevo hasta que este sea efectivo sin error de compatibilidad.

<img src="assets/chapter-6/deploy7.png" alt="Imagen deploy paso 7">

#### Frontend Web

https://parkeoya.vercel.app/register

Para configurar el despliegue del web aplication, seguimos los pasos detallados a continuación utilizando Vercel y con CI como plataforma:

Primero se accedemos a vercel.com y agregamos un nuevo proyecto:

<img src="assets/chapter-6/deploy-web-1.png" alt="Imagen deploy web paso 1">

Luego agregamos la organización de GitHub:

<img src="assets/chapter-6/deploy-web-2.png" alt="Imagen deploy paso 2">

Y buscamos el repositorio del frontend web:

<img src="assets/chapter-6/deploy-web-3.png" alt="Imagen deploy paso 3">

Luego verificamos que importe la rama correcta del repositorio de GitHub y el nombre del proyecto. Por ultimo le damos a Deploy.

<img src="assets/chapter-6/deploy-web-4.png" alt="Imagen deploy paso 4">

Listo! El deploy fue un exito [ParkeoYa](https://parkeoya.vercel.app/login)

<img src="assets/chapter-6/deploy-web-5.png" alt="Imagen deploy paso 5">


##### 6.2.1.9. Team Collaboration Insights during Sprint

**Distribución de aportes en el informe:**

URL del repositorio para el Project Report en la organización de GitHub del equipo: [https://github.com/Lorem-Ipsum-UPC/reporte](https://github.com/Lorem-Ipsum-UPC/reporte)

**¿Cómo se han desarrollado las actividades de elaboración del informe?**

Para el desarrollo del informe y aplicaciones en este sprint se distribuyó los capítulos de esta manera:

| Integrante     | Aporte en el informe                                                                                                                                                                                                                                                                   |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tyrone**     | Mobile Wireframes and Mockups, Design App Prototyping.|
| **Barbara**    | Sprint planning 1, Style Guidelines, Web and Landing Page Wireframes and Mockups, Design App Prototyping, Source Code Management, User Flows, Wireflows, Sprint Backlog 1  |
| **Alessandro** | Sprint 1, Source Code Management, Software Deployment Configuration, Development Evidence for Sprint Review, Execution Evidence for Sprint Review, Documentation Evidence for Sprint Review, Software Deployment Evidence for Sprint Review, Team Collaboration Insights during Sprint, Landing Page and App Web Development, |
| **Nelson**     | Sprint 1, testing suite evidence for sprint review |
| **Juan**       | Sprint 1, Software Deployment Evidence for Sprint Review (frontend web), Web Aplication Wireframes, Mockups and video prototyping web |

**Evidencia del commit:**

- **Commits Landing Page**
  
<img src="assets/chapter-6/CommitsLandingPage.png" alt="CommitsLandingPage">

- **Commits Web Frontend**

<img src="assets/chapter-6/CommitsFrontendWeb.png" alt="CommitsFrontendWeb">

- **Commits Informe**
<img src="assets/chapter-6/evidence1.png" alt="Evidencia 1">

<img src="assets/chapter-6/evidence2.png" alt="Evidencia 2">

# Conclusiones y recomendaciones

### Conclusiones

### TB1

Para esta primera entrega se logró sentar las bases del proyecto, logrando que todos los integrantes del equipo comprendieran el tema y la estructura que se realizará durante todo el ciclo, incluyendo la definición de los usuarios objetivo, epicas, historias de usuario, bounded contexts, diagramas C4, diagramas de clases y diagramas de base de datos.

### TP

Para esta segunda entrega se logro realizar una Landing Page consistente de acuerdo a la propuesta de solucion brindada, dando a visualizar la mision y visión de la startup asi como lo que estamos ofreciendo. Se incluye a su vez la capa frontend de la aplicación web que en si, tiene data hardcodeada, sin embargo, lo que se quiere demostrara es el avance consistente de la plataforma como tal, las secciones que vamos a presentar en el entregable final. Todo este avance viene acompañado de sus respectivos despliegues hechos en Netlify (Landing Page) y Vercel (Frontend Web). En este avance en equipo se pudo tambien declarar los pasos a seguir para desplegar una aplicacion web asi dandonos la oportunidad de poder diversificar nuestra web gratuitamente con estas plataformas de despliegue gratuito.

### Recomendaciones

⦁ **Ampliación de funcionalidades:**
Se sugiere continuar con el desarrollo de características que aporten mayor valor tanto a los usuarios como a los administradores. Entre ellas, destacan la integración de métodos de pago automatizados, notificaciones en tiempo real sobre disponibilidad y opciones de personalización. Asimismo, la incorporación de sensores IoT para detectar en tiempo real la ocupación de los estacionamientos fortalecerá la precisión del sistema y la experiencia del usuario.

⦁ **Crecimiento geográfico y sectorial:**
Luego del éxito inicial, ParkeoYa debería considerar su expansión hacia nuevas ciudades con alta demanda de estacionamiento, así como explorar oportunidades en sectores específicos como aeropuertos, centros comerciales y eventos masivos, donde la gestión eficiente de espacios es crucial.

⦁ **Estrategia de marketing y sensibilización:**
Es fundamental diseñar campañas de marketing digital dirigidas tanto a conductores como a administradores de estacionamientos. El uso de testimonios y casos de éxito que evidencien mejoras en tiempos de búsqueda puede incrementar la adopción. Asimismo, se recomienda educar a los usuarios sobre los beneficios que la plataforma aporta a la sostenibilidad urbana.

⦁ **Monitoreo y mejora continua:**
La implementación de un sistema de análisis constante de datos de uso y ocupación permitirá anticipar tendencias, ajustar estrategias y corregir deficiencias. Este enfoque garantizará una experiencia de usuario cada vez más optimizada y adaptable a nuevas necesidades.

⦁ **Compromiso con la sostenibilidad:**
ParkeoYa debería reforzar su rol en la movilidad sostenible, impulsando iniciativas que reduzcan la huella de carbono y colaborando con proyectos de ciudades inteligentes. Esto no solo fortalecerá su posicionamiento como plataforma tecnológica, sino también como un aliado clave en la construcción de entornos urbanos más responsables y sostenibles.

<div style="page-break-after: always;"></div>
