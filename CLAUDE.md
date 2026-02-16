# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Proyecto

- **Nombre**: KineCenter Salta
- **Tipo**: Landing institucional estática (HTML/CSS/JS)
- **Descripción**: Sitio web optimizado para SEO de centro de kinesiología y estética en Salta, Argentina
- **Deploy**: Vercel
- **URL**: https://kinicenter-salta.vercel.app/

## Stack Tecnológico

- **Frontend**: HTML5 semántico + CSS3 + JavaScript vanilla
- **Styling**: CSS puro (sin frameworks)
- **SEO**: Schema.org markup, Open Graph, Twitter Cards
- **Deploy**: Vercel con configuración en `vercel.json`
- **Package Manager**: npm (solo para tooling de Claude Code)

## Estructura del Proyecto

```
/
├── index.html          # Landing principal con SEO completo
├── style.css           # Estilos responsive (mobile-first)
├── script.js           # Interacciones (menú, animaciones)
├── sitemap.xml         # Mapa del sitio para Google
├── robots.txt          # Directivas para crawlers
├── manifest.json       # PWA configuration
├── vercel.json         # Headers de seguridad y cache
├── .gitignore          # Excluye docs y archivos temporales
└── assets/
    └── images/         # Imágenes del sitio (logos, favicons)
```

## Archivos de Documentación (ignorados en deploy)

Estos archivos están en `.gitignore` y NO se despliegan:
- `SEO-GUIA.md` - Guía de implementación SEO
- `CONTENIDO-BLOG-SEO.md` - Ideas de contenido
- `GENERAR-IMAGENES.md` - Instrucciones para assets
- `TRACKING-CODES.html` - Códigos de Analytics/GTM
- `CHECKLIST-IMPLEMENTACION.md` - Lista de tareas

## Convenciones de Código

### HTML
- Semántico HTML5: usar `<section>`, `<article>`, `<nav>`, `<header>`, `<footer>`
- Un solo `<h1>` por página con keyword principal
- Jerarquía correcta de headings (H1 → H2 → H3)
- ARIA labels para accesibilidad
- Schema.org structured data en JSON-LD

### CSS
- Mobile-first approach (media queries desde `min-width`)
- Variables CSS para colores y espaciado
- BEM naming para clases complejas
- No usar `!important` salvo casos justificados
- Orden de propiedades: layout → sizing → spacing → typography → visual

### JavaScript
- Vanilla JS (sin frameworks)
- Event listeners delegados cuando sea posible
- Evitar manipulación directa del DOM en loops
- Usar `const` y `let`, nunca `var`
- Comentarios solo cuando la lógica no sea obvia

## Paleta de Colores

- **Primario (Cian)**: `#06b6d4` (cyan-500)
- **Secundario (Morado)**: `#8b5cf6` (violet-500)
- **Texto**: `#1e293b` (slate-800)
- **Fondo**: `#f8fafc` (slate-50)
- **Acento**: Gradiente cian → morado

## Información del Negocio

- **Nombre**: KineCenter Salta
- **Dirección**: Alsina 1238, Salta Capital, Salta, Argentina
- **Coordenadas**: -24.7859, -65.4117
- **Teléfono**: 387 5224444
- **WhatsApp**: +54 9 387 5224444
- **Profesional**: Lic. Flavia Daniela González Farías (MP 1049)

## Keywords Principales

- kinesiología salta
- estética salta
- HIFU salta
- criolipólisis salta
- rehabilitación neurológica salta
- tecarterapia salta
- ondas de choque salta
- fisioterapia salta

## Reglas Críticas

1. NUNCA modificar las coordenadas GPS o dirección sin confirmación del cliente
2. MANTENER la estructura de Schema.org intacta (crítico para SEO local)
3. NO cambiar los colores principales sin justificación (branding)
4. PRESERVAR el formato de URLs canónicas y Open Graph
5. TODO cambio en meta tags debe mantener longitud óptima:
   - Title: 50-60 caracteres
   - Description: 150-160 caracteres
6. NO eliminar clases CSS que puedan estar referenciadas en JS
7. VERIFICAR responsive en cambios de CSS (mobile, tablet, desktop)

## Deployment

### Vercel Configuration
- Deploy automático desde `main` branch
- Headers de seguridad configurados en `vercel.json`
- Cache de 1 año para assets estáticos
- Redirect www → non-www

### Pre-Deploy Checklist
1. Verificar que todos los enlaces internos funcionen
2. Validar HTML en https://validator.w3.org/
3. Validar Schema.org en https://search.google.com/test/rich-results
4. Probar responsive en varios tamaños
5. Verificar velocidad en PageSpeed Insights

## Comandos Comunes

```bash
# Desarrollo local
# Abrir index.html en navegador con Live Server (VS Code) o similar

# Deploy a Vercel (automático via git)
git add .
git commit -m "descripción"
git push origin main

# Validar HTML (requiere Node.js)
npx html-validator-cli index.html

# Comprobar links rotos
npx broken-link-checker https://kinicenter-salta.vercel.app/
```

## Patrones de Implementación

### Agregar Nueva Sección
1. Crear `<section>` con id único y clase descriptiva
2. Agregar heading (H2 o H3 según jerarquía)
3. Incluir keyword relevante en el heading
4. Agregar link en navegación si es necesaria
5. Asegurar responsive en mobile

### Optimizar Imagen Nueva
1. Formato: WebP para fotografías, SVG para logos
2. Tamaño máximo: 1920px de ancho
3. Compresión: 80-85% de calidad
4. Naming: descriptivo (ej: `tratamiento-hifu-salta.webp`)
5. Alt text: descriptivo con keyword cuando sea relevante

### Agregar Tracking Code
1. NO agregar directamente a `index.html`
2. Ver `TRACKING-CODES.html` para ejemplos
3. Insertar antes de `</head>` para scripts de tracking
4. Usar async/defer en scripts externos

## SEO Checklist

### On-Page
- [x] Title tag optimizado con keyword
- [x] Meta description única por página
- [x] H1 único con keyword principal
- [x] Schema.org LocalBusiness + MedicalBusiness
- [x] Open Graph tags completos
- [x] Canonical URL configurado
- [x] Geo-tags de ubicación

### Technical
- [x] Sitemap.xml accesible
- [x] Robots.txt configurado
- [x] SSL/HTTPS habilitado
- [x] Mobile responsive
- [x] Velocidad de carga optimizada
- [x] Images con lazy loading preparado

### Local SEO
- [ ] Google My Business verificado (acción del cliente)
- [ ] Reseñas de Google activas (acción del cliente)
- [ ] NAP (Name, Address, Phone) consistente

## Testing

### Manual Testing Checklist
- Navegación mobile funcionando correctamente
- WhatsApp float button redirige correctamente
- Smooth scroll en links internos
- Forms (si se agregan) validan correctamente
- No hay errores en consola del browser

### Herramientas de Testing
- [Google PageSpeed Insights](https://pagespeed.web.dev/)
- [Mobile-Friendly Test](https://search.google.com/test/mobile-friendly)
- [Rich Results Test](https://search.google.com/test/rich-results)
- [W3C HTML Validator](https://validator.w3.org/)
- [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)

## Workflow de Cambios

### Para cambios pequeños (typos, ajustes CSS):
1. Editar archivo directamente
2. Probar en browser local
3. Commit con mensaje descriptivo
4. Push (deploy automático)

### Para cambios significativos (nueva sección, refactor):
1. Usar `/rpi:research` para analizar viabilidad
2. Usar `/rpi:plan` para descomponer en micro-tareas
3. Usar `/rpi:implement` para ejecutar con commits atómicos
4. Planes se guardan en `rpi/{feature-slug}/`

## Commits

Seguir formato convencional:

```
{type}(scope): descripción imperativa

Cuerpo opcional con contexto
```

### Types permitidos:
- `feat`: Nueva funcionalidad o sección
- `fix`: Corrección de bug o error
- `style`: Cambios de CSS/diseño
- `content`: Cambios de texto/contenido
- `seo`: Optimizaciones de SEO
- `perf`: Mejoras de performance
- `docs`: Cambios en documentación
- `chore`: Tareas de mantenimiento

### Ejemplos:
```
feat(services): add new treatment section for laser therapy
fix(mobile): correct menu overlay z-index on iOS
style(hero): adjust gradient opacity for better readability
content(about): update professional credentials
seo(meta): optimize description length for Google preview
```

---

## Memoria

### Última Sesión
- **Fecha**: 2026-02-16
- **Estado**: Sitio desplegado en Vercel
- **Feature en progreso**: ninguna
- **Próximo paso**: Monitorear métricas SEO tras configuración de Google My Business

### Decisiones Técnicas Recientes
- Migración de URLs absolutas a relativas para desarrollo local
- Configuración de Vercel con headers de seguridad y cache agresivo
- URLs actualizadas al dominio definitivo de Vercel

### Problemas Conocidos
- Imágenes de assets/images/ pendientes de generar (logos, og-image, favicons)
- Google Analytics y GTM pendientes de configuración por el cliente
- Google My Business pendiente de creación por el cliente
