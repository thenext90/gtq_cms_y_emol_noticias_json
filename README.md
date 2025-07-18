# Global Technology Quality - Website con Carousel de Noticias

Este proyecto es un sitio web profesional para Global TechnologyyQuality, una empresa de consultoría ISO, construido con Astro y Tailwind CSS. Incluye secciones para servicios, noticias y un **nuevo carousel interactivo de noticias destacadas**.

## 🆕 Nuevas Características - Carousel de Noticias

### Componentes Agregados:
1. **`/src/components/NewsCard.astro`** - Tarjeta individual de noticia
2. **`/src/components/NewsCarousel.astro`** - Carousel principal de noticias
3. **`/src/data/news-carousel.json`** - Datos de las noticias destacadas

### Características del Carousel:
- ✅ **Autoplay automático mejorado** (cada 5 segundos)
- ✅ **Navegación con flechas**
- ✅ **Indicadores de puntos (dots)**
- ✅ **Barra de progreso animada** - nueva característica
- ✅ **Diseño completamente responsive**
  - Móvil: 1 noticia por vista
  - Tablet: 2 noticias por vista  
  - Desktop: 3 noticias por vista
- ✅ **Soporte para navegación con teclado** (flechas ←→)
- ✅ **Gestos táctiles (swipe)** para móviles - nueva característica
- ✅ **Pausa automática al hacer hover**
- ✅ **Efectos de transición suaves**
- ✅ **Animaciones de aparición escalonadas**
- ✅ **Optimizado para rendimiento**

### Datos de Noticias Incluidos:
- 10 noticias destacadas sobre ISO y gestión empresarial
- Categorías codificadas por colores: ISO 9001, 14001, 27001, 45001, etc.
- Fechas reales y formateadas en español
- Imágenes profesionales de Unsplash
- Resúmenes informativos

## 📁 Estructura del Proyecto

```
src/
├── components/
│   ├── NewsCard.astro              # ← NUEVO: Tarjeta de noticia
│   ├── NewsCarousel.astro          # ← NUEVO: Carousel de noticias
│   └── CourseCard.astro            # ← PREVIO: Componente de curso (no usado)
├── data/
│   ├── news-carousel.json          # ← NUEVO: Datos de noticias destacadas
│   ├── courses.json                # ← PREVIO: Datos de cursos (no usado)
│   ├── emol_emprendedores_full.json
│   └── cms_consultores_news.json
└── pages/
    └── index.astro                 # ← MODIFICADO: Incluye carousel de noticias
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

### Modificar Noticias:
Edita el archivo `/src/data/news-carousel.json`:

```json
{
  "id": 1,
  "titulo": "Título de la noticia",
  "imagen": "URL_de_imagen",
  "fecha": "2025-07-17",
  "categoria": "ISO 9001",
  "resumen": "Resumen descriptivo de la noticia..."
}
```

### Categorías Disponibles con Colores:
- **ISO 9001:** Azul
- **ISO 14001:** Verde  
- **ISO 27001:** Púrpura
- **ISO 45001:** Rojo
- **ISO 31000:** Amarillo
- **ISO 22301:** Índigo
- **ISO 37001:** Rosa
- **ISO 19600:** Gris
- **ISO 26000:** Verde azulado
- **Innovación:** Naranja

### Ajustar Configuración:
En `/src/components/NewsCarousel.astro`, puedes modificar:

- **Velocidad del autoplay:** Línea 20 - `autoplayDuration = 5000` (milisegundos)
- **Noticias por vista:** Líneas 25-33 - Ajustar breakpoints
- **Velocidad de transición:** CSS - `duration-500`

## 🌐 Secciones del Sitio

1. **Hero** - Mensaje principal
2. **Nosotros** - Visión, misión y valores
3. **Servicios** - Certificaciones ISO disponibles
4. **Noticias Destacadas** - ← **NUEVO: Carousel interactivo de noticias**
5. **Contacto** - Formulario y información
6. **Noticias Emol** - Feed de noticias filtradas
7. **Noticias CMS** - Contenido de CMS Consultores

## 📱 Responsive Design

El carousel está completamente optimizado para todos los dispositivos:

- **Móvil (< 768px):** 1 noticia, controles adaptados, soporte para swipe
- **Tablet (768px - 1024px):** 2 noticias
- **Desktop (> 1024px):** 3 noticias, experiencia completa

## 🛠️ Tecnologías Utilizadas

- **Astro 4.0** - Framework principal
- **Tailwind CSS 3.0** - Estilos y diseño
- **TypeScript** - Tipado estático
- **JavaScript nativo** - Funcionalidad del carousel (sin dependencias externas)

## ✨ Características Avanzadas

### 🎯 Autoplay Inteligente:
- Se pausa automáticamente al hacer hover
- Se reinicia al quitar el cursor
- Barra de progreso visual
- Funciona con gestos táctiles

### 📱 Experiencia Móvil:
- Soporte completo para gestos swipe
- Controles optimizados para pantallas pequeñas
- Animaciones suaves y responsivas

### ♿ Accesibilidad:
- Navegación completa con teclado
- Etiquetas ARIA apropiadas
- Contraste de colores optimizado
- Focus indicators visibles

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
- **Animaciones CSS nativas** para mejor rendimiento

## 🎯 Próximas Mejoras Sugeridas

- [ ] Lazy loading para imágenes del carousel
- [ ] Preloader para imágenes
- [ ] Integración con CMS para noticias dinámicas
- [ ] Filtros por categoría de noticia
- [ ] Modal de lectura completa
- [ ] Compartir en redes sociales
- [ ] Sistema de favoritos
- [ ] Búsqueda de noticias
