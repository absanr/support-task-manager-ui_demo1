# 🎯 Soporti - Sistema Avanzado de Gestión de Tickets

**Sistema profesional de gestión de tickets de soporte técnico** desarrollado con **Spring Boot 3**, **Thymeleaf** y **Lombok**. Incluye tablero **Kanban inmersivo**, gestión completa de inventario y sistema de diseño moderno.

---

## ✨ Características Principales

### 🏗️ **Arquitectura y Backend**
- **Arquitectura MVC limpia y profesional**
- **Spring Boot 3.5.6** con Java 21
- **Controladores RESTful** para gestión de tickets
- **Servicios de negocio** con lógica centralizada
- **Modelos de dominio** con Lombok (POJOs limpios)

### 🎫 **Gestión Avanzada de Tickets**
- **Vista Lista**: Tabla completa con filtros y búsqueda
- **Vista Kanban Inmersiva**: Tablero drag & drop con controles flotantes
- **Estados dinámicos**: 6 estados configurables (Backlog → En Prueba)
- **Prioridades visuales**: Crítica, Alta, Media, Baja (con colores)
- **Asignación de técnicos** y control de equipos
- **Marca de agua personalizada** en modo Kanban

### 📦 **Control de Inventario**
- **Gestión completa de repuestos**
- **Alertas de stock bajo** (≤3 unidades)
- **Códigos únicos** por repuesto
- **Ubicación física** en almacén
- **Vista detalle** con información completa

### 🎨 **Sistema de Diseño Profesional**
- **Paleta de 7 colores funcionales** (Material Design)
- **Modo claro y oscuro** completamente funcional
- **Interfaz responsive** con Bootstrap 5.3.3
- **Sistema de variables CSS** (120+ tokens)
- **Accesibilidad WCAG 2.1** (touch-friendly, contraste AA)
- **Animaciones fluidas** sin distractores

### 🚀 **Experiencia de Usuario**
- **Navbar moderno** con búsqueda central y notificaciones
- **Sidebar colapsible** con localStorage persistence
- **Controles flotantes** en modo Kanban inmersivo
- **Botones de acción** posicionados como app móvil
- **Transiciones suaves** y feedback visual
- **Íconos dinámicos** que cambian según el estado

---

## 🛠️ **Stack Tecnológico**

### **Backend**
- ![Java](https://img.shields.io/badge/Java-21-orange?logo=openjdk) **Java 21** (compatible con Java 17+)
- ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5.6-brightgreen?logo=springboot) **Spring Boot 3.5.6**
- ![Spring Web](https://img.shields.io/badge/Spring%20Web%20MVC-6.1.x-green?logo=spring) **Spring Web MVC**
- ![Thymeleaf](https://img.shields.io/badge/Thymeleaf-3.1.x-blue?logo=thymeleaf) **Thymeleaf** para vistas dinámicas
- ![Lombok](https://img.shields.io/badge/Lombok-1.18.x-red?logo=lombok) **Lombok** para reducir código repetitivo
- ![Maven](https://img.shields.io/badge/Maven-3.9.x-purple?logo=apachemaven) **Maven** como gestor de dependencias

### **Frontend**
- ![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.3-purple?logo=bootstrap) **Bootstrap 5.3.3** para diseño responsive
- ![Font Awesome](https://img.shields.io/badge/Font%20Awesome-6.5.1-blue?logo=fontawesome) **Font Awesome 6.5.1** para iconografía
- ![CSS3](https://img.shields.io/badge/CSS3-Variables%20+%20Grid-blue?logo=css3) **CSS3 moderno** con variables, grid y flexbox
- ![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?logo=javascript) **JavaScript ES6+** para interactividad

---

## 📁 **Estructura del Proyecto**

```
📂 taskmanager/
├── 📂 src/main/java/com/soporti/app/taskmanager/
│   ├── 📂 controller/
│   │   ├── 🏠 ControladorInicio.java       → Dashboard principal
│   │   ├── 🎫 ControladorTicket.java       → Gestión de tickets (Lista + Kanban)
│   │   └── 📦 ControladorInventario.java   → Gestión de inventario
│   ├── 📂 model/
│   │   ├── 📄 Ticket.java                  → Modelo de ticket
│   │   ├── 🔧 Repuesto.java                → Modelo de repuesto
│   │   ├── 📊 EstadoTicket.java            → Estados del workflow
│   │   ├── ⚠️ PrioridadTicket.java         → Niveles de prioridad
│   │   └── 📝 HistorialTicket.java         → Historial de cambios
│   ├── 📂 service/
│   │   ├── 🎫 ServicioTicket.java          → Lógica de negocio tickets
│   │   └── 📦 ServicioRepuesto.java        → Lógica de negocio inventario
│   └── ⚡ TaskmanagerApplication.java      → Clase principal Spring Boot
├── 📂 src/main/resources/
│   ├── 📂 templates/
│   │   ├── 🏗️ layout.html                  → Plantilla base con fragmentos
│   │   ├── 🏠 inicio.html                  → Dashboard con métricas
│   │   ├── 📂 tickets/
│   │   │   ├── 📋 listado.html             → Vista lista con filtros
│   │   │   ├── 🎯 kanban.html              → Vista Kanban inmersiva
│   │   │   └── 🔍 detalle.html             → Detalle completo de ticket
│   │   └── 📂 inventario/
│   │       ├── 📦 listado.html             → Lista de repuestos
│   │       └── 🔍 detalle.html             → Detalle de repuesto
│   ├── 📂 static/
│   │   ├── 📂 css/
│   │   │   ├── 🎨 variables.css            → Sistema de tokens de diseño
│   │   │   ├── 🏗️ layout.css               → Navbar, sidebar, layout
│   │   │   ├── 🧩 componentes.css          → Componentes reutilizables
│   │   │   ├── 📊 dashboard.css            → Estilos del dashboard
│   │   │   ├── 🎫 tickets.css              → Estilos vista lista tickets
│   │   │   ├── 🎯 kanban.css               → Estilos Kanban inmersivo
│   │   │   └── 📦 inventario.css           → Estilos inventario
│   │   └── 📂 js/
│   │       ├── 🌓 theme-manager.js         → Gestor modo claro/oscuro
│   │       └── 📱 sidebar-manager.js       → Gestor sidebar colapsible
│   └── ⚙️ application.properties           → Configuración aplicación
├── 📄 pom.xml                              → Dependencias Maven
├── 📖 README.md                            → Documentación principal
├── 📋 ANALISIS_FUNCIONALIDAD.md           → Análisis técnico detallado
└── 🎨 UI_TOUCH_IMPROVEMENTS.md            → Mejoras de UX implementadas
```

## [PATTERN] Patrón arquitectónico

### Modelo-Vista-Controlador (MVC)

**Model (Modelo)**
- `Ticket`: Representa un ticket de soporte con toda su información
- `Repuesto`: Representa un repuesto del inventario
- `HistorialTicket`: Registro de cambios en los tickets

**View (Vista)**
- Plantillas Thymeleaf en `src/main/resources/templates/`
- Layout reutilizable con fragmentos (navbar, sidebar, footer)
- Vistas dinámicas con `th:each`, `th:text`, `th:if`

**Controller (Controlador)**
- `ControladorInicio`: Gestiona el dashboard principal
- `ControladorTicket`: Gestiona tickets de soporte
- `ControladorInventario`: Gestiona el inventario de repuestos

## [DATA] Gestión de datos

Los datos se gestionan en **memoria** mediante `ArrayList`, sin uso de base de datos:

- **ServicioTicket**: Contiene 12 tickets precargados en memoria
- **ServicioRepuesto**: Contiene 10 repuestos precargados en memoria

Los servicios son **@Service** de Spring e implementan la lógica de negocio.

---

## 🗺️ **Mapa de Rutas**

| Ruta | Descripción | Vista | Características |
|------|-------------|-------|----------------|
| `/` o `/inicio` | 🏠 **Dashboard Principal** | `inicio.html` | Métricas, últimos tickets, navegación rápida |
| `/tickets` | 📋 **Lista de Tickets** | `tickets/listado.html` | Tabla completa, filtros, búsqueda |
| `/tickets/kanban` | 🎯 **Kanban Inmersivo** | `tickets/kanban.html` | Tablero visual, controles flotantes, drag & drop |
| `/tickets/{id}` | 🔍 **Detalle de Ticket** | `tickets/detalle.html` | Información completa, historial, acciones |
| `/inventario` | 📦 **Lista de Inventario** | `inventario/listado.html` | Repuestos, alertas stock, filtros |
| `/inventario/{codigo}` | 🔧 **Detalle de Repuesto** | `inventario/detalle.html` | Especificaciones, ubicación, stock |

---

## 🎯 **Kanban Inmersivo - Características Avanzadas**

### **Experiencia Visual**
- 🎨 **Marca de agua dinámica**: "Tablero Kanban" con opacidad personalizable
- 🎭 **Controles flotantes**: Botones posicionados como app móvil
- 🎪 **6 estados de workflow**: Backlog → Asignado → En Diagnóstico → En Reparación → En Espera → En Prueba
- 🏷️ **Etiquetas de prioridad**: Visual con colores (Crítica-Roja, Alta-Naranja, Media-Azul, Baja-Gris)

### **Interactividad Avanzada**
- 📱 **Sidebar colapsible**: Ícono dinámico (`>>>` cuando oculto, `<<<` cuando visible)
- 🔄 **Persistencia localStorage**: Recuerda el estado del sidebar
- ⚡ **Animaciones fluidas**: Transiciones de 0.3s sin distractores
- 🎛️ **Controles intuitivos**: 
  - Botón sidebar en navbar (esquina superior izquierda)
  - "Vista Lista" (botón secundario, esquina inferior derecha)
  - "Nuevo Ticket" (botón principal azul, esquina inferior derecha)

### **Responsive Design**
- 📱 **Móvil**: Sidebar se convierte en offcanvas automáticamente
- 💻 **Desktop**: Control total de sidebar colapsible
- 🎨 **Botones adaptativos**: Tamaños y posiciones optimizados por dispositivo

## [RUN] Cómo ejecutar

### Requisitos previos
- Java 17 o superior instalado
- Maven 3.8+ (incluido en el proyecto con wrapper)

### Compilar el proyecto
```bash
./mvnw clean compile
```

### Ejecutar la aplicación
```bash
./mvnw spring-boot:run
```

### Acceder a la aplicación
Abrir navegador en: **http://localhost:8080**

## [CONFIG] Configuración

El archivo `application.properties` contiene:

- **Puerto del servidor**: 8080
- **Configuración de Thymeleaf**: Sin caché para desarrollo
- **Codificación UTF-8**: Para caracteres en español
- **Logging**: Nivel INFO para seguimiento

## [MIGRATION] Proceso de migración

### Desde carpeta `old/`

**Origen:**
- Frontend HTML estático con JavaScript
- Datos en archivos JSON
- Sin backend integrado

**Destino:**
- Aplicación Spring Boot con arquitectura MVC
- Vistas dinámicas con Thymeleaf
- Datos simulados en memoria con POJOs
- Backend Java profesional

### Cambios realizados

1. **Modelos de dominio**: Creación de POJOs con Lombok
2. **Servicios de datos**: Servicios Spring con datos en memoria
3. **Controladores MVC**: Controladores con rutas en español
4. **Plantillas Thymeleaf**: Conversión de HTML estático a dinámico
5. **Layout reutilizable**: Fragmentos Thymeleaf para navbar/sidebar/footer
6. **Todo en español**: Código, comentarios, rutas y mensajes

---

## ⚡ **Funcionalidades Implementadas**

### 🏠 **Dashboard Inteligente**
- 📊 **Indicadores clave**: Tickets pendientes, en progreso, cerrados, stock crítico
- 📈 **Métricas visuales**: Cards con iconografía y colores semánticos
- 🕐 **Últimos tickets**: Tabla con los 10 tickets más recientes
- 🚀 **Navegación rápida**: Acceso directo a todas las secciones
- 🎨 **Adaptativo**: Se ajusta automáticamente al modo claro/oscuro

### 🎫 **Gestión Avanzada de Tickets**

#### **Vista Lista Profesional**
- 📋 **Tabla completa**: Todos los tickets con paginación
- 🔍 **Filtros dinámicos**: Por estado, prioridad, técnico asignado
- 🔎 **Búsqueda en tiempo real**: Por código, título, cliente
- 🏷️ **Estados visuales**: 6 estados con colores distintivos
- ⚠️ **Prioridades**: Crítica (roja), Alta (naranja), Media (azul), Baja (gris)

#### **Vista Kanban Inmersiva** ⭐
- 🎯 **Tablero visual**: Arrastrar y soltar entre columnas
- 🎨 **Marca de agua**: "Tablero Kanban" de fondo personalizable
- 📱 **Controles flotantes**: Botones posicionados como app móvil
- 🔄 **Sidebar dinámico**: Ícono cambia según estado (>>> | <<<)
- 💾 **Persistencia**: Estado guardado en localStorage
- ⚡ **Animaciones**: Transiciones fluidas de 0.3s

#### **Detalle Completo**
- 📝 **Información completa**: Todos los campos del ticket
- 👥 **Técnico asignado**: Control de asignación
- 🏢 **Cliente y equipo**: Datos de contacto y hardware
- 📋 **Descripción del problema**: Detalle técnico
- ⏱️ **Historial**: Registro de cambios de estado

### 📦 **Control de Inventario Inteligente**
- 📊 **Lista de repuestos**: Vista tabular con toda la información
- ⚠️ **Alertas automáticas**: Stock bajo (≤3 unidades) resaltado
- 🔧 **Detalle completo**: Especificaciones, ubicación, proveedores
- 📍 **Control de ubicación**: Estantes y posiciones físicas
- 🔎 **Búsqueda avanzada**: Por código, nombre, categoría

---

## 🎨 **Sistema de Diseño Profesional v2.0**

### **Paleta de Colores Funcional**
```css
/* 🔵 Primario - Acciones principales */
--color-primario: #2196f3;     /* Botones principales, enlaces */
--color-primario-600: #1976d2; /* Hover states */
--color-primario-100: #bbdefb; /* Fondos suaves */

/* ✅ Éxito - Confirmaciones */  
--color-exito: #4caf50;        /* Tickets completados, confirmaciones */

/* ⚠️ Advertencia - Alertas */
--color-advertencia: #ffc107;  /* Stock bajo, advertencias */

/* ❌ Error - Crítico */
--color-error: #f44336;        /* Errores, prioridad crítica */

/* ℹ️ Info - Información */
--color-info: #00bcd4;         /* Información neutral */

/* 🌫️ Escala de Grises */
--gris-50 a --gris-900;        /* Textos, fondos, bordes */
```

### **Tipografía Escalada** 
```css
--texto-xs: 0.75rem;    /* 12px - Metadatos */
--texto-sm: 0.875rem;   /* 14px - Texto secundario */
--texto-base: 1rem;     /* 16px - Texto principal */
--texto-lg: 1.125rem;   /* 18px - Subtítulos */
--texto-xl: 1.25rem;    /* 20px - Encabezados pequeños */
--texto-2xl: 1.5rem;    /* 24px - Encabezados medianos */
--texto-3xl: 1.875rem;  /* 30px - Encabezados grandes */
--texto-4xl: 2.25rem;   /* 36px - Títulos principales */
```

### **Sistema de Espaciado**
```css
--espacio-1: 0.25rem;   /* 4px */
--espacio-2: 0.5rem;    /* 8px */
--espacio-4: 1rem;      /* 16px - Base */
--espacio-6: 1.5rem;    /* 24px */
--espacio-8: 2rem;      /* 32px */
--espacio-12: 3rem;     /* 48px */
```

### **Características de Accesibilidad**
- ✅ **Contraste WCAG 2.1 AA**: Todos los elementos cumplen estándares
- ✅ **Touch-friendly**: Áreas táctiles mínimas de 44px
- ✅ **Navegación por teclado**: Focus states visibles
- ✅ **Responsive mobile-first**: Diseño adaptativo completo
- ✅ **Sin animaciones distractoras**: Solo transiciones funcionales

### **Modo Oscuro Inteligente**
- 🌓 **Toggle automático**: Botón en navbar para cambio instantáneo  
- 💾 **Persistencia**: Preferencia guardada en localStorage
- 🎨 **Adaptación completa**: Todos los componentes se adaptan
- 🔄 **Sincronización**: Mantiene consistencia entre pestañas

---

## 📝 **Convenciones de Código**

### **Estilo Java**
- 🇪🇸 **Nombres en español**: Clases, métodos, variables, atributos
- 📚 **JavaDoc completo**: Documentación clara en español
- 🧹 **Código limpio**: Principios SOLID y Clean Code
- 🏷️ **Lombok**: Reducción de boilerplate con anotaciones

### **Estilo Frontend**
- 📱 **Mobile-first**: Responsive design desde móvil hacia desktop
- 🧩 **Componentes reutilizables**: CSS modular y mantenible
- 🎨 **Variables CSS**: Sistema de tokens centralizado
- ⚡ **Performance**: Carga optimizada de recursos
- 🔧 **JavaScript progresivo**: Funcionalidad básica sin JS, mejorada con JS

---

## 🚀 **Cómo Ejecutar el Proyecto**

### **Requisitos Previos**
- ☕ **Java 17+** instalado ([Descargar OpenJDK](https://openjdk.org/))
- 🔧 **Maven 3.8+** (incluido wrapper en el proyecto)
- 🌐 **Navegador moderno** (Chrome 90+, Firefox 88+, Safari 14+)

### **Pasos de Instalación**

1. **Clonar el repositorio**
   ```bash
   git clone <repository-url>
   cd taskmanager
   ```

2. **Compilar el proyecto**
   ```bash
   ./mvnw clean compile
   ```

3. **Ejecutar la aplicación**
   ```bash
   ./mvnw spring-boot:run
   ```

4. **Acceder a la aplicación**
   ```
   🌐 URL: http://localhost:8080
   🏠 Dashboard: http://localhost:8080/inicio
   📋 Tickets: http://localhost:8080/tickets
   🎯 Kanban: http://localhost:8080/tickets/kanban
   📦 Inventario: http://localhost:8080/inventario
   ```

### **Configuración Avanzada**

**Cambiar puerto** (opcional):
```properties
# application.properties
server.port=9090
```

**Activar logs detallados** (desarrollo):
```properties
logging.level.com.soporti=DEBUG
spring.thymeleaf.cache=false
```

---

## 🎯 **Información del Proyecto**

| Campo | Valor |
|-------|-------|
| **Nombre** | Soporti - Sistema Avanzado de Gestión de Tickets |
| **Versión** | 2.0 (Kanban Inmersivo) |
| **Framework** | Spring Boot 3.5.6 |
| **Java Version** | 21 (compatible con 17+) |
| **Arquitectura** | MVC + Sistema de Diseño Moderno |
| **Estado** | ✅ Completo y Funcional |
| **Licencia** | 📚 Proyecto Educativo |
| **Desarrollado por** | Grupo de Desarrollo - Curso Marcos de Desarrollo Web |

---

## 🛣️ **Roadmap - Próximos Pasos**

### **Fase 1: Funcionalidades Core** 
- [ ] 📝 **Formularios CRUD**: Crear/editar/eliminar tickets
- [ ] 🔐 **Sistema de autenticación**: Spring Security + roles
- [ ] 🗄️ **Persistencia**: Migración a Spring Data JPA + H2/PostgreSQL
- [ ] ✅ **Validaciones**: Bean Validation en formularios

### **Fase 2: Características Avanzadas**
- [ ] 🔍 **Búsqueda avanzada**: Elasticsearch/Lucene integration  
- [ ] 📊 **Reportes y dashboards**: Gráficos con Chart.js
- [ ] 📧 **Notificaciones**: Email/SMS cuando cambian estados
- [ ] 🔄 **API REST**: Endpoints para integración externa

### **Fase 3: Optimización y Escalabilidad**
- [ ] 📱 **PWA**: Progressive Web App capabilities
- [ ] 🔄 **Real-time**: WebSockets para actualizaciones en vivo
- [ ] 🧪 **Testing**: Unit tests con JUnit 5 + Mockito
- [ ] 🐳 **Containerización**: Docker + Docker Compose
- [ ] ☁️ **Deploy**: Preparación para cloud (AWS/Azure)

---

## 🆘 **Soporte y Documentación**

### **Documentación Técnica**
- 📋 [`ANALISIS_FUNCIONALIDAD.md`](./ANALISIS_FUNCIONALIDAD.md) - Análisis detallado de funcionalidades
- 🎨 [`UI_TOUCH_IMPROVEMENTS.md`](./UI_TOUCH_IMPROVEMENTS.md) - Mejoras de UX implementadas
- 🧪 [`TESTING_THEME.md`](./TESTING_THEME.md) - Pruebas del sistema de temas
- 🔧 [`THEME_FIXES.md`](./THEME_FIXES.md) - Correcciones de modo oscuro

### **Enlaces Útiles**
- 📖 [Spring Boot Documentation](https://spring.io/projects/spring-boot)
- 🎨 [Thymeleaf Documentation](https://www.thymeleaf.org/)
- 🎯 [Bootstrap 5 Documentation](https://getbootstrap.com/docs/5.3/)
- ⚙️ [Lombok Documentation](https://projectlombok.org/)

### **Resolución de Problemas**
- 📊 **Logs**: Revisar consola para errores detallados
- ⚙️ **Configuración**: Verificar `application.properties`
- 🔄 **Puerto ocupado**: Cambiar puerto en configuración
- 🧹 **Cache**: Limpiar con `./mvnw clean` si hay problemas

---

## 🏆 **Estado del Proyecto**

### **✅ Completado**
- 🏗️ Arquitectura MVC profesional
- 🎫 Gestión completa de tickets (Lista + Kanban)
- 📦 Control de inventario con alertas
- 🎨 Sistema de diseño moderno (7 colores funcionales)
- 🌓 Modo claro/oscuro completamente funcional
- 📱 Diseño responsive mobile-first
- 🎯 Kanban inmersivo con controles flotantes
- 💾 Persistencia de preferencias (localStorage)
- ⚡ Animaciones y transiciones fluidas

### **🚧 En Desarrollo**
- 📝 Formularios de creación/edición
- 🔐 Sistema de autenticación
- 🗄️ Persistencia en base de datos

---

**✨ Proyecto exitosamente migrado y modernizado desde frontend estático a aplicación Spring Boot profesional con experiencia Kanban inmersiva.**

---
*Última actualización: Octubre 2025* 🗓️
