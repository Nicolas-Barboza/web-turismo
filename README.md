# 🌍 Travel - Sitio Web de Turismo

## 📌 Descripción del Proyecto

Sitio web de turismo desarrollado como Trabajo Práctico para la materia de **Programción y Servicio Web con HTML5 y CSS3**. El proyecto implementa técnicas avanzadas de CSS sin utilizar JavaScript para la lógica de UI, cumpliendo con la especificación **"CSS-Only"**.

**URL de la demo:** [https://github.com/Nicolas-Barboza/web-turismo.git](https://github.com/Nicolas-Barboza/web-turismo.git)

---

## 🎯 Objetivos Cumplidos

| Objetivo | Estado |
|----------|--------|
| Estructura semántica HTML5 | ✅ |
| Diseño responsivo (Flexbox + Grid) | ✅ |
| Animaciones y efectos CSS avanzados | ✅ |
| CSS-Only (sin JS para UI) | ✅ |
| Accesibilidad WCAG AA/AAA | ✅ |
| Modo oscuro con toggle | ✅ |

---

## 🛠️ Tecnologías Utilizadas

| Tecnología | Uso |
|------------|-----|
| **HTML5** | Estructura semántica (`header`, `nav`, `main`, `section`, `article`, `footer`) |
| **CSS3** | Grid, Flexbox, Custom Properties, Animaciones, Transiciones |
| **Google Fonts** | Tipografías 'Inter' (400, 500, 600) y 'Playfair Display' (400, 600, 700) |
| **Unsplash** | Imágenes de placeholder para destinos |
| **OpenStreetMap** | Mapa embebido en footer |

---

## 📁 Estructura del Proyecto

```
proyecto-turismo-css/
├── index.html                    # Página principal
├── destinos.html                 # Galería masonry + filtros
├── agencias.html                 # Tarjetas flip 3D
├── contacto.html                 # Formulario validado + modal
├── precios.html                  # Tabla comparativa + tooltips
├── blog.html                     # Newspaper grid + avatares CSS
├── assets/
│   ├── css/
│   │   ├── base/
│   │   │   ├── reset.css         # Reset moderno
│   │   │   ├── variables.css     # Custom Properties
│   │   │   └── tipografia.css    # Estilos tipográficos
│   │   ├── layout/
│   │   │   ├── header.css        # Header fijo + mega-menú
│   │   │   ├── footer.css        # Footer con newsletter
│   │   │   └── grid.css          # Sistema de grid + masonry
│   │   ├── components/
│   │   │   ├── botones.css       # Botones + spinner
│   │   │   ├── cards.css         # Tarjetas base + masonry
│   │   │   └── modal.css         # Modal con :target
│   │   ├── pages/
│   │   │   ├── home.css          # Hero + contador + carrusel
│   │   │   ├── destinos.css      # Filtros + tabla
│   │   │   ├── agencias.css      # Flip 3D + rating
│   │   │   ├── contacto.css      # Validación formulario
│   │   │   ├── precios.css       # Tooltips + responsive
│   │   │   └── blog.css          # Newspaper + scroll reveal
│   │   ├── themes/
│   │   │   └── dark-mode.css     # Modo oscuro
│   │   └── main.css              # Importa todos los módulos
│   ├── js/
│   │   └── script.js             # Solo toggle dark mode (3 líneas)
│   └── video/
│       └── hero-background.mp4   # Video de fondo Hero
└── README.md                     # Este archivo
```

---

## 🔧 Decisiones de Diseño

### 1. Arquitectura CSS Modular (BEM + Capas)

**Decisión:** Separar el CSS en capas (`base/`, `layout/`, `components/`, `pages/`, `themes/`).

**Justificación:**
- **Mantenibilidad:** Cada archivo tiene una responsabilidad única.
- **Escalabilidad:** Nuevas páginas o componentes se integran sin conflictos.
- **Reutilización:** Componentes como `.btn` o `.card` se usan en múltiples páginas.

### 2. CSS-Only: Técnicas Avanzadas sin JavaScript

| Funcionalidad | Técnica CSS |
|---------------|-------------|
| Mega-menú | `:hover` + `:focus-within` |
| Filtros | `:checked` + `~` (hermanos generales) |
| Contador animado | `@property` + `counter()` |
| Carrusel | `scroll-snap-type` |
| Efecto Flip 3D | `perspective` + `backface-visibility` |
| Rating estrellas | `linear-gradient` + `background-clip: text` |
| Validación formulario | `:valid` / `:invalid` |
| Modal | `:target` |
| Tooltips | `attr(data-tip)` + pseudo-elementos |
| Avatares | `::before` / `::after` |
| Scroll Reveal | `animation-timeline: view()` |
| Menú móvil | Checkbox hack (`:checked`) |

### 3. Paleta de Colores (Tonos Tierra)

| Variable | Valor | Uso |
|----------|-------|-----|
| `--color-primary` | `#0A6847` | Verde naturaleza (botones, enlaces) |
| `--color-secondary` | `#D4A373` | Terracota (acentos) |
| `--color-accent` | `#FFD700` | Dorado (destacados) |
| `--color-bg` | `#F5F5F0` | Fondo principal |
| `--color-text` | `#1A1A1A` | Texto principal |

### 4. Tipografía

- **'Inter'** (400, 500, 600): Textos y UI.
- **'Playfair Display'** (400, 600, 700): Títulos elegantes.

### 5. Accesibilidad (WCAG AA/AAA)

| Elemento | Implementación |
|----------|----------------|
| Skip link | `Saltar al contenido principal` |
| ARIA labels | `aria-label`, `aria-expanded`, `aria-current` |
| Focus visible | `:focus-visible` con `outline: 3px solid` |
| Contraste | Verificado > 4.5:1 |

---

## 📄 Descripción de Páginas

### 🏠 Home (`index.html`)
- **Hero:** Video de fondo con overlay gradiente y texto animado.
- **Destinos destacados:** 4 cards con enlace a filtros específicos.
- **Contador animado:** 500+ destinos, 15K+ viajeros, 120+ agencias.
- **Carrusel testimonios:** `scroll-snap` con 4 testimonios y avatares CSS.

### 🗺️ Destinos (`destinos.html`)
- **Filtros CSS-only:** 6 categorías (Todos, Cultural, Naturaleza, Sol y Playa, Gastronómico, Religioso).
- **Masonry Grid:** `grid-auto-rows: 8px` + clases `.h-1` a `.h-4` para alturas variadas.
- **Tabla de precios:** 8 destinos con tooltips informativos.

### 🏢 Agencias (`agencias.html`)
- **Flip 3D:** 4 tarjetas con `perspective: 1000px`.
- **Rating estrellas:** `linear-gradient` + `background-clip: text`.
- **Frente:** Logo, nombre, ubicación, rating.
- **Dorso:** Descripción, especialidades, botón "Contactar".

### 📞 Contacto (`contacto.html`)
- **Validación en tiempo real:** `:valid` (borde verde) / `:invalid` (borde rojo).
- **Mensajes de error:** Pseudo-elemento `::before` con `attr(data-error)`.
- **Spinner CSS:** `@keyframes spin` en botón de envío.
- **Modal confirmación:** `:target` con overlay blur.

### 💰 Precios (`precios.html`)
- **Tabla comparativa:** 8 destinos con columnas: Destino, Precio Base, Todo Incluido, Descuento, Temporada.
- **Tooltips:** 3 tooltips con `attr(data-tip)`.
- **Efecto hover:** `transform: scale(1.01)` + cambio de fondo.

### 📰 Blog (`blog.html`)
- **Newspaper Grid:** 4 columnas, artículo destacado 2x2.
- **Filtros:** 5 categorías (Todos, Cultural, Naturaleza, Gastronómico, Aventura).
- **Avatares CSS:** 4 variantes con pseudo-elementos.
- **Scroll Reveal:** `animation-timeline: view()` con fallback.

---

## 🚀 Instalación y Ejecución

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/Nicolas-Barboza/web-turismo.git
   ```

2. **Abrir en el navegador:**
   - Navegar a la carpeta del proyecto.
   - Abrir `index.html` directamente.

3. **O usar Live Server (VS Code):**
   - Instalar extensión "Live Server".
   - Click derecho en `index.html` → "Open with Live Server".

---

## 👨‍💻 Autor

**Nombre:** Gonzalo Nicolás Barboza
**Materia:** Programación y Servicio Web
**Año:** 2026

---

## 📄 Licencia

Este proyecto es de uso educativo para el Trabajo Práctico.
