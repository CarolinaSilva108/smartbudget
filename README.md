# SmartBudget - Landing Page

> Proyecto del Módulo #3: Desarrollo de la Interfaz de Usuario Web

## 📝 Descripción

SmartBudget es una landing page para una aplicación de gestión de finanzas personales. El proyecto implementa una interfaz web moderna, responsive y escalable utilizando HTML5 semántico, metodologías CSS, SASS y Bootstrap 4.

## 🚀 Características Implementadas

### ✅ Lección 1: Estructura HTML Semántica
- Uso de etiquetas semánticas HTML5: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`
- Jerarquía correcta de headings (h1, h2, h3)
- Comentarios identificando componentes clave

### ✅ Lección 2: Metodología CSS (BEM)
- **Metodología elegida**: BEM (Block Element Modifier)
- **Justificación**: BEM es simple de aprender, fácil de mantener y escalable para proyectos pequeños y medianos
- Nomenclatura coherente en todos los componentes
- Ejemplos: `.navbar`, `.navbar__link`, `.btn--primary`

### ✅ Lección 3: Preprocesador SASS
- Estructura de carpetas **patrón 7-1**:
  ```
  sass/
  ├── abstracts/         (variables, mixins)
  ├── base/              (reset, typography)
  ├── components/        (buttons, cards)
  ├── layout/            (header, footer)
  └── pages/             (home)
  ```
- Variables para colores, tipografía y espaciado
- Mixins para responsive y reutilización de estilos
- Anidamientos y imports modulares

### ✅ Lección 4: Modelo de Cajas y Layout
- Box-sizing aplicado globalmente
- Flexbox para componentes (navbar, hero, stats)
- CSS Grid para secciones (features grid, footer)
- Media queries mobile-first para responsive
- Funciona en mobile, tablet y desktop

### ✅ Lección 5: Bootstrap 4
- **Integrado via CDN** (Bootstrap 4.6.2)
- **Componentes utilizados**:
  - Navbar responsive con collapse para mobile
  - Sistema de Grid (container, row, col)
  - Cards para mostrar características
  - Modales para registro y demo
  - Botones y utilidades de espaciado
- Paleta de colores personalizada que complementa Bootstrap

## 🛠️ Tecnologías Utilizadas

| Tecnología | Versión | Uso |
|------------|---------|-----|
| HTML5 | - | Estructura semántica |
| CSS3 | - | Estilos base |
| SASS | Dart Sass | Preprocesador CSS |
| Bootstrap | 4.6.2 | Framework CSS |
| Font Awesome | 6.4.0 | Iconos |
| Google Fonts | - | Tipografía (Inter, Poppins) |

## 📁 Estructura del Proyecto

```
smartbudget/
├── index.html              # Página principal
├── css/
│   └── main.css           # CSS compilado desde SASS
├── sass/
│   ├── abstracts/
│   │   ├── _variables.scss
│   │   └── _mixins.scss
│   ├── base/
│   │   ├── _reset.scss
│   │   └── _typography.scss
│   ├── components/
│   │   ├── _buttons.scss
│   │   └── _cards.scss
│   ├── layout/
│   │   ├── _header.scss
│   │   └── _footer.scss
│   ├── pages/
│   │   └── _home.scss
│   └── main.scss          # Archivo principal
└── README.md              # Este archivo
```

## 🎨 Decisiones de Diseño

### Paleta de Colores
- **Primario**: Azul (#2563eb) - Transmite confianza y profesionalismo (importante en fintech)
- **Secundario**: Verde (#10b981) - Representa crecimiento y ganancias
- **Acento**: Púrpura (#8b5cf6) - Para CTAs destacados
- **Neutrales**: Escala de grises para textos y fondos

### Tipografía
- **Display**: Poppins (headings) - Moderna y llamativa
- **Body**: Inter (textos) - Excelente legibilidad

### Responsive Design
- **Mobile First**: Diseñado primero para móviles (576px+)
- **Breakpoints**: 576px (sm), 768px (md), 992px (lg), 1200px (xl)

## ⚙️ Instalación y Uso

### Requisitos Previos
- Node.js y npm instalados
- SASS instalado globalmente: `npm install -g sass`

### Pasos para Ejecutar

1. **Clonar el repositorio**
   ```bash
   git clone <url-del-repositorio>
   cd smartbudget
   ```

2. **Compilar SASS**
   ```bash
   sass sass/main.scss css/main.css
   ```

3. **Modo desarrollo (watch)**
   ```bash
   sass --watch sass/main.scss:css/main.css
   ```

4. **Abrir en el navegador**
   - Simplemente abre `index.html` en tu navegador
   - O usa un servidor local: `npx serve .`

## 📱 Compatibilidad

✅ Chrome 90+  
✅ Firefox 88+  
✅ Safari 14+  
✅ Edge 90+  
✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🔄 Proceso de Desarrollo

Este proyecto se desarrolló siguiendo buenas prácticas de Git:
- Rama principal: `main`
- Ramas feature para cada funcionalidad
- Commits descriptivos por cambio

## 🎓 Aprendizajes Clave

1. **HTML Semántico**: Aprendí la importancia de usar etiquetas semánticas para mejor accesibilidad y SEO
2. **Metodología BEM**: Me ayudó a mantener el CSS organizado y predecible
3. **SASS**: Los mixins y variables hacen el código mucho más mantenible
4. **Bootstrap**: Acelera el desarrollo pero requiere entender cuándo usarlo vs CSS custom
5. **Responsive Design**: Mobile-first es más eficiente que desktop-first

## 🚀 Mejoras Futuras

- [ ] Agregar animaciones con JavaScript
- [ ] Implementar dark mode
- [ ] Conectar formularios a backend
- [ ] Agregar más secciones (testimonios, precios)
- [ ] Optimizar imágenes y performance
- [ ] Tests de accesibilidad (WCAG)

## 👤 Autor

Proyecto desarrollado como parte del Módulo #3 de Alkemy - Desarrollo Frontend

---

**Nota**: Este es un proyecto educativo con fines demostrativos del aprendizaje de HTML, CSS, SASS y Bootstrap.
