# Justificación Metodológica - SmartBudget

## Metodología CSS Seleccionada: BEM (Block Element Modifier)

### ¿Por qué BEM?

Elegí la metodología BEM para este proyecto por las siguientes razones:

#### 1. **Simplicidad y Curva de Aprendizaje**
BEM tiene una convención de nomenclatura clara y fácil de entender:
- **Block**: Componente independiente (`.navbar`, `.card`, `.btn`)
- **Element**: Parte del bloque (`.navbar__link`, `.card__title`)
- **Modifier**: Variación del bloque o elemento (`.btn--primary`, `.card--hover`)

#### 2. **Escalabilidad**
Al trabajar en un proyecto de landing page que puede crecer, BEM permite:
- Agregar nuevos componentes sin conflictos de nombres
- Entender la estructura solo leyendo las clases
- Facilitar el trabajo en equipo con convenciones claras

#### 3. **Modularidad**
Cada componente es independiente y reutilizable. Por ejemplo:
```css
.btn { /* Estilos base */ }
.btn--primary { /* Variación azul */ }
.btn--secondary { /* Variación verde */ }
```

#### 4. **Comparación con otras metodologías**

| Aspecto | BEM | OOCSS | SMACSS |
|---------|-----|-------|--------|
| Curva de aprendizaje | **Baja** ✅ | Media | Alta |
| Nomenclatura clara | **Sí** ✅ | Parcial | Parcial |
| Para proyectos pequeños | **Ideal** ✅ | Sí | Complejo |
| Uso con SASS | **Excelente** ✅ | Bueno | Bueno |

## Decisiones de Diseño

### Paleta de Colores - Enfoque Fintech

**Primario: Azul (#2563eb)**
- **Justificación**: El azul transmite confianza, seguridad y profesionalismo
- **Uso**: Aplicaciones financieras históricamente usan azul (bancos, PayPal, etc.)

**Secundario: Verde (#10b981)**
- **Justificación**: Representa crecimiento, ganancias y éxito financiero
- **Uso**: Indicadores positivos, botones de acción exitosa

**Acento: Púrpura (#8b5cf6)**
- **Justificación**: Destacar CTAs importantes sin ser agresivo
- **Uso**: Botones principales, gradientes para jerarquía visual

### Tipografía

**Inter (Body Text)**
- Diseñada específicamente para interfaces digitales
- Excelente legibilidad en pantallas pequeñas
- Soporta múltiples pesos (300-800)

**Poppins (Headings)**
- Moderna y geométrica
- Contrasta bien con Inter
- Transmite innovación (importante en fintech)

## Framework CSS: Bootstrap 4

### ¿Por qué Bootstrap 4 y no Bootstrap 5?

El enunciado del proyecto especificó Bootstrap 4, por lo tanto usé la versión 4.6.2 (última versión estable de BS4).

**Ventajas de Bootstrap 4 para este proyecto:**
- Sistema de Grid probado y maduro
- Componentes pre-diseñados (navbar, modales, cards)
- Compatibilidad con navegadores antiguos (si es necesario)
- Documentación extensa

**Componentes utilizados:**
1. **Navbar responsive** - Colapsa en mobile con hamburger menu
2. **Cards** - Para mostrar características del producto
3. **Modales** - Para registro y demo sin cambiar de página
4. **Sistema de Grid** - Layout responsive con `container`, `row`, `col`
5. **Utilidades** - Espaciado, colores, alineación

## Estructura SASS - Patrón 7-1

### ¿Qué es el Patrón 7-1?

Es una arquitectura que organiza SASS en 7 carpetas + 1 archivo principal:

```
sass/
├── abstracts/      # Variables y mixins (sin output CSS)
├── base/           # Estilos base (reset, tipografía)
├── components/     # Componentes pequeños (botones, cards)
├── layout/         # Estructura general (header, footer)
├── pages/          # Estilos específicos por página
├── themes/         # (No usado en este proyecto)
├── vendors/        # (No usado - Bootstrap via CDN)
└── main.scss       # Archivo que importa todo
```

### Beneficios aplicados:

1. **Organización clara**: Cada archivo tiene un propósito específico
2. **Mantenibilidad**: Fácil encontrar y modificar estilos
3. **Reutilización**: Variables y mixins centralizados
4. **Colaboración**: Múltiples personas pueden trabajar sin conflictos

## Layout Responsivo - Mobile First

### Media Queries utilizadas:

```scss
// Mobile: base (sin media query)
// Tablet: 768px+
// Desktop: 992px+
// Desktop grande: 1200px+
```

### Enfoque Mobile First

Escribí los estilos primero para mobile y **agregué** complejidad para pantallas grandes:

```scss
.hero__container {
  grid-template-columns: 1fr;  // Mobile: 1 columna
  
  @media (min-width: 768px) {
    grid-template-columns: 1fr 1fr;  // Desktop: 2 columnas
  }
}
```

**Ventajas:**
- Mejor performance en móviles (mayoría de usuarios)
- Código más limpio (menos sobrescritura)
- Progressive enhancement (funciona sin CSS avanzado)

## Herramientas de Verificación

### Modelo de Cajas

Apliqué `box-sizing: border-box` globalmente:
```css
*, *::before, *::after {
  box-sizing: border-box;
}
```

**Beneficio**: Padding y border no afectan el width/height final

### Validación realizada:

1. ✅ Inspección con DevTools (Chrome)
2. ✅ Prueba en diferentes tamaños de pantalla
3. ✅ Verificación de espaciado y alineación
4. ✅ Comprobación de collapse de navbar en mobile

## Conclusión

Este proyecto demuestra la aplicación práctica de:
- HTML semántico para accesibilidad y SEO
- Metodología BEM para CSS escalable
- SASS con patrón 7-1 para organización
- Bootstrap 4 para accelerar desarrollo
- Diseño responsive mobile-first

Cada decisión técnica se tomó pensando en **mantenibilidad**, **escalabilidad** y **mejores prácticas** del desarrollo frontend moderno.

---

**Fecha**: Febrero 2026  
**Módulo**: #3 - Desarrollo de la Interfaz de Usuario Web  
**Proyecto**: SmartBudget Landing Page
