# Global Technology Quality - Website con Carousel de Cursos

Este proyecto es un sitio web profesional para Global Technology Quality, una empresa de consultoría ISO, construido con Astro y Tailwind CSS. Incluye secciones para servicios, noticias y un **nuevo carousel interactivo de cursos**.

## 🆕 Nuevas Características - Carousel de Cursos

### Componentes Agregados:
1. **`/src/components/CourseCard.astro`** - Tarjeta individual de curso
2. **`/src/components/CoursesCarousel.astro`** - Carousel principal
3. **`/src/data/courses.json`** - Datos de los cursos

### Características del Carousel:
- ✅ **Autoplay automático** (cada 4 segundos)
- ✅ **Navegación con flechas**
- ✅ **Indicadores de puntos (dots)**
- ✅ **Diseño completamente responsive**
  - Móvil: 1 curso por vista
  - Tablet: 2 cursos por vista  
  - Desktop: 3 cursos por vista
- ✅ **Soporte para navegación con teclado** (flechas ←→)
- ✅ **Pausa automática al hacer hover**
- ✅ **Efectos de transición suaves**
- ✅ **Optimizado para rendimiento**

### Datos de Cursos Incluidos:
- 10 cursos de ejemplo con imágenes de Unsplash
- Categorías: Principiante, Intermedio, Avanzado
- Sistema de ratings con estrellas
- Precios en USD
- Imágenes responsivas

## 📁 Estructura del Proyecto

```
src/
├── components/
│   ├── CourseCard.astro          # ← NUEVO: Tarjeta de curso
│   └── CoursesCarousel.astro     # ← NUEVO: Carousel principal
├── data/
│   ├── courses.json              # ← NUEVO: Datos de cursos
│   ├── emol_emprendedores_full.json
│   └── cms_consultores_news.json
└── pages/
    └── index.astro               # ← MODIFICADO: Incluye carousel
```

## 🚀 Instalación y Uso

1. **Instalar dependencias:**
   ```bash
   npm install
   ```

2. **Ejecutar en desarrollo:**
   ```bash
   npm run dev
   ```

3. **Construir para producción:**
   ```bash
   npm run build
   ```

## 🎨 Personalización del Carousel

### Modificar Cursos:
Edita el archivo `/src/data/courses.json`:

```json
{
  "id": 1,
  "cover": "URL_de_imagen",
  "title": "Título del curso",
  "rating": 5,
  "ratingCount": 25,
  "price": 30,
  "category": "Intermedio"
}
```

### Ajustar Configuración:
En `/src/components/CoursesCarousel.astro`, puedes modificar:

- **Velocidad del autoplay:** Línea 140 - `4000` (milisegundos)
- **Cursos por vista:** Líneas 67-75 - Ajustar breakpoints
- **Velocidad de transición:** Línea 188 - `duration-500`

### Estilos Personalizados:
El carousel usa clases de Tailwind CSS que puedes personalizar:

- **Colores:** `bg-blue-600`, `text-blue-600`, etc.
- **Espaciado:** `py-16`, `px-6`, etc.
- **Sombras:** `shadow-lg`, `hover:shadow-xl`

## 🌐 Secciones del Sitio

1. **Hero** - Mensaje principal
2. **Nosotros** - Visión, misión y valores
3. **Servicios** - Certificaciones ISO disponibles
4. **Cursos** - ← **NUEVO: Carousel interactivo**
5. **Contacto** - Formulario y información
6. **Noticias Emol** - Feed de noticias filtradas
7. **Noticias CMS** - Contenido de CMS Consultores

## 📱 Responsive Design

El carousel está completamente optimizado para todos los dispositivos:

- **Móvil (< 768px):** 1 curso, controles adaptados
- **Tablet (768px - 1024px):** 2 cursos
- **Desktop (> 1024px):** 3 cursos, experiencia completa

## 🛠️ Tecnologías Utilizadas

- **Astro 4.0** - Framework principal
- **Tailwind CSS 3.0** - Estilos y diseño
- **TypeScript** - Tipado estático
- **JavaScript nativo** - Funcionalidad del carousel (sin dependencias externas)

## 🔧 Código Reutilizable

El código del carousel es completamente modular y puede ser:
- Copiado a otros proyectos Astro
- Adaptado para diferentes tipos de contenido
- Personalizado con diferentes estilos
- Extendido con más funcionalidades

## 📈 Rendimiento

- **Sin dependencias externas** para el carousel
- **Imágenes optimizadas** con lazy loading
- **CSS mínimo** usando Tailwind
- **JavaScript eficiente** con event listeners optimizados

## 🎯 Próximas Mejoras Sugeridas

- [ ] Lazy loading para imágenes del carousel
- [ ] Gestos táctiles (swipe) en móviles
- [ ] Preloader para imágenes
- [ ] Integración con CMS para cursos dinámicos
- [ ] Filtros por categoría de curso
- [ ] Modal de detalles de curso
