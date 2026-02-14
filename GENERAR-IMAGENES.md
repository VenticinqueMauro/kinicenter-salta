# Guía para Generar Imágenes Optimizadas - KineCenter Salta

## 📁 Imágenes Necesarias para SEO Óptimo

### 1. Logo (Alta Prioridad)
Ubicación: `/images/`

**Archivos a generar desde el PDF del logo:**

#### Logo Principal
- `kinecentersalta-logo.svg` - **Prioridad MÁXIMA**
  - Formato vectorial escalable
  - Peso: <10KB
  - Uso: Navegación, footer, compartir en redes

- `kinecentersalta-logo.png` - Transparente
  - Tamaño: 512x512px
  - Peso: <50KB
  - Uso: Favicon, redes sociales

- `kinecentersalta-logo-horizontal.png`
  - Tamaño: 800x200px
  - Peso: <40KB
  - Uso: Email signatures, documentos

---

### 2. Open Graph Images (Redes Sociales)
Ubicación: `/images/`

**CRÍTICO para compartir en Facebook, WhatsApp, LinkedIn**

- `og-image.jpg`
  - Tamaño: **1200x630px** (proporción exacta para Facebook)
  - Peso: <200KB
  - Formato: JPG (mejor compresión para fotos)
  - Contenido sugerido:
    * Logo KineCenter
    * Texto: "Centro de Kinesiología y Estética - Salta"
    * Fondo gradiente cian/morado
    * Imagen del centro o equipos

- `og-image-square.jpg`
  - Tamaño: **1080x1080px**
  - Peso: <150KB
  - Uso: Instagram, WhatsApp Business

---

### 3. Favicons
Ubicación: `/` (raíz del sitio)

**Generador recomendado**: https://realfavicongenerator.net/

Desde el logo PNG, generar:

- `favicon.ico` (16x16, 32x32, 48x48 en un archivo)
- `favicon-16x16.png`
- `favicon-32x32.png`
- `apple-touch-icon.png` (180x180px)
- `android-chrome-192x192.png`
- `android-chrome-512x512.png`

---

### 4. PWA Icons (Progressive Web App)
Ubicación: `/images/`

**Para manifest.json:**

- `icon-72x72.png`
- `icon-96x96.png`
- `icon-128x128.png`
- `icon-144x144.png`
- `icon-152x152.png`
- `icon-192x192.png`
- `icon-384x384.png`
- `icon-512x512.png`

**Tip**: Usar herramienta automática:
- https://app-manifest.firebaseapp.com/
- https://www.pwabuilder.com/

---

### 5. Imágenes del Centro y Equipos
Ubicación: `/images/gallery/`

**Fotos profesionales recomendadas:**

#### Instalaciones (6-10 fotos)
- `centro-exterior.webp` (1200x800px, <150KB)
- `recepcion.webp`
- `sala-espera.webp`
- `consultorio-1.webp`
- `consultorio-2.webp`
- `area-estetica.webp`

#### Equipos/Tecnología (10-15 fotos)
- `equipo-hifu-25d.webp`
- `equipo-criolipolisis.webp`
- `equipo-tecarterapia.webp`
- `equipo-ondas-choque.webp`
- `equipo-radiofrecuencia.webp`
- `equipo-cavitacion.webp`
- etc.

#### Profesional
- `lic-gonzalez-farias.webp` (800x800px, <100KB)
  - Foto profesional de la Lic. González Farías
  - Fondo neutro
  - Buena iluminación

#### Tratamientos en acción
- `tratamiento-hifu-proceso.webp`
- `sesion-tecarterapia.webp`
- `consulta-profesional.webp`

**IMPORTANTE**:
- Todas en formato **WebP** (mejor compresión)
- Alt text descriptivo en cada imagen
- Nombres de archivo con keywords

---

## 🛠️ Herramientas para Convertir PDF a Imágenes

### Opción 1: Online (Rápido)
**CloudConvert** - https://cloudconvert.com/pdf-to-svg
- PDF → SVG (logo vectorial)
- PDF → PNG (alta resolución)

### Opción 2: Software Gratuito
**Adobe Acrobat Reader** (gratuito)
- Abrir PDF
- Herramientas → Exportar PDF → Imagen → PNG
- Configurar DPI: 300 para alta calidad

**GIMP** (gratuito, código abierto)
- Importar PDF
- Exportar como PNG con transparencia
- Redimensionar según necesidad

**Inkscape** (gratuito, vectorial)
- Abrir PDF
- Guardar como SVG optimizado
- Exportar PNG de diferentes tamaños

### Opción 3: Photoshop / Illustrator (Profesional)
- Illustrator: PDF → SVG nativo
- Photoshop: PDF → PNG/WebP optimizado

---

## 🎨 Crear Open Graph Image (og-image.jpg)

### Template sugerido:

**Tamaño del canvas**: 1200x630px

**Elementos**:
1. **Fondo**: Gradiente cian (#1CC8EE) a morado (#9D7FE8)
2. **Logo**: Centrado arriba (300x300px)
3. **Texto Principal**: "KineCenter Salta"
   - Fuente: Cormorant Garamond Bold
   - Tamaño: 72px
   - Color: Blanco
4. **Subtítulo**: "Centro de Kinesiología y Estética"
   - Fuente: Inter Regular
   - Tamaño: 32px
   - Color: Blanco 80%
5. **Badge**: "Tecnología HIFU | Criolipólisis | Rehabilitación"
   - Fondo: Blanco semi-transparente
   - Texto pequeño

**Herramientas para crear**:
- Canva (plantilla personalizada): https://www.canva.com/
- Figma (diseño profesional): https://www.figma.com/
- Photoshop

**Template Canva directo**:
- Buscar: "Facebook Post" (1200x630px)
- Personalizar con colores y textos

---

## 🖼️ Optimización de Imágenes

### Compresión sin pérdida de calidad:

**Herramientas online**:
- **TinyPNG**: https://tinypng.com/ (PNG/JPG)
- **Squoosh**: https://squoosh.app/ (WebP/AVIF)
- **Compressor.io**: https://compressor.io/

**Software offline**:
- **ImageOptim** (Mac)
- **FileOptimizer** (Windows)
- **XnConvert** (Windows/Mac/Linux)

### Conversión a WebP:

**Online**:
- https://convertio.co/es/jpg-webp/

**Línea de comandos** (avanzado):
```bash
# Instalar cwebp (Google)
# Windows: Descargar de developers.google.com/speed/webp/download

# Convertir JPG a WebP
cwebp -q 80 input.jpg -o output.webp

# Convertir PNG a WebP con transparencia
cwebp -q 80 -lossless input.png -o output.webp
```

---

## 📋 Checklist de Imágenes

### Básico (Implementar YA):
- [ ] Logo en formato SVG
- [ ] Logo PNG (512x512px)
- [ ] Favicon.ico
- [ ] favicon-32x32.png
- [ ] favicon-16x16.png
- [ ] apple-touch-icon.png (180x180px)
- [ ] og-image.jpg (1200x630px)

### Intermedio (Semana 1-2):
- [ ] Todos los PWA icons (manifest.json)
- [ ] Foto profesional Lic. González Farías
- [ ] 3-5 fotos del centro
- [ ] 5-8 fotos de equipos principales

### Avanzado (Mes 1):
- [ ] Galería completa de equipos
- [ ] Fotos de tratamientos en proceso
- [ ] Casos antes/después (con autorización)
- [ ] Videos cortos de procedimientos
- [ ] Infografías de procesos

---

## 📐 Dimensiones de Referencia

### Redes Sociales:
- **Facebook Post**: 1200x630px
- **Instagram Post**: 1080x1080px
- **Instagram Story**: 1080x1920px
- **Twitter Card**: 1200x628px
- **LinkedIn Post**: 1200x627px
- **WhatsApp Status**: 1080x1920px

### Web:
- **Hero Image**: 1920x1080px
- **Blog Featured**: 1200x675px
- **Gallery Thumbnail**: 400x400px
- **Team Photo**: 800x800px

---

## 🎯 Nombres de Archivo SEO-Friendly

### ❌ MAL:
- `IMG_1234.jpg`
- `foto1.png`
- `DSC_5678.webp`

### ✅ BIEN:
- `kinecentersalta-logo-principal.svg`
- `centro-kinesiologia-salta-exterior.webp`
- `equipo-hifu-25d-max-kinecentersalta.webp`
- `tratamiento-criolipolisis-salta-proceso.webp`
- `lic-flavia-gonzalez-farias-kinesiologia.webp`

**Reglas**:
- Solo minúsculas
- Separar con guiones `-`
- Incluir keyword relevante
- Máximo 5-6 palabras
- Sin caracteres especiales (ñ, acentos)

---

## 🔄 Estructura de Carpetas Recomendada

```
/images/
├── logo/
│   ├── kinecentersalta-logo.svg
│   ├── kinecentersalta-logo.png
│   ├── kinecentersalta-logo-horizontal.png
│   └── kinecentersalta-logo-vertical.png
│
├── social/
│   ├── og-image.jpg
│   ├── og-image-square.jpg
│   └── twitter-card.jpg
│
├── icons/
│   ├── icon-72x72.png
│   ├── icon-96x96.png
│   ├── ... (todos los PWA icons)
│   └── icon-512x512.png
│
├── gallery/
│   ├── centro/
│   │   ├── centro-exterior.webp
│   │   ├── recepcion.webp
│   │   └── consultorio.webp
│   │
│   ├── equipos/
│   │   ├── equipo-hifu-25d.webp
│   │   ├── equipo-criolipolisis.webp
│   │   └── equipo-tecarterapia.webp
│   │
│   └── team/
│       └── lic-gonzalez-farias.webp
│
└── blog/
    ├── hifu-salta-antes-despues.webp
    ├── criolipolisis-proceso.webp
    └── tecarterapia-tratamiento.webp
```

---

## 📝 Plantilla de Alt Text

**Formato**:
```
[Descripción específica] + [Ubicación/Contexto] + [Marca]
```

**Ejemplos**:

```html
<!-- Logo -->
<img src="kinecentersalta-logo.svg"
     alt="Logo de KineCenter Salta - Centro de Kinesiología y Estética">

<!-- Equipo -->
<img src="equipo-hifu-25d.webp"
     alt="Equipo HIFU 25D Max para lifting facial no invasivo en KineCenter Salta">

<!-- Instalaciones -->
<img src="centro-exterior.webp"
     alt="Fachada del centro KineCenter ubicado en Alsina 1238, Salta Capital">

<!-- Profesional -->
<img src="lic-gonzalez-farias.webp"
     alt="Lic. Flavia Daniela González Farías - Kinesióloga Dermatofuncional MP 1049">

<!-- Tratamiento -->
<img src="tratamiento-criolipolisis-abdomen.webp"
     alt="Sesión de criolipólisis para reducción de grasa abdominal en KineCenter Salta">
```

---

## ✅ Validación Final

Antes de publicar, verificar:

### Peso de archivos:
- [ ] SVG: <20KB
- [ ] PNG logos: <50KB
- [ ] Favicons: <10KB cada uno
- [ ] OG images: <200KB
- [ ] Fotos WebP: <150KB

### Dimensiones correctas:
- [ ] OG image: exactamente 1200x630px
- [ ] Favicons: tamaños estándar
- [ ] PWA icons: según manifest.json

### Formatos:
- [ ] Logo: SVG disponible
- [ ] Fotos: WebP (con fallback JPG)
- [ ] Favicons: ICO + PNG

### Metadata:
- [ ] Todos los alt texts completados
- [ ] Nombres de archivo descriptivos
- [ ] Sin espacios ni caracteres especiales

---

## 🎨 Recursos Gratuitos

### Bancos de imágenes (si necesitas complementar):
- **Unsplash**: https://unsplash.com/ (médicas, spa, salud)
- **Pexels**: https://www.pexels.com/
- **Pixabay**: https://pixabay.com/

Buscar:
- "medical equipment"
- "physiotherapy"
- "spa treatment"
- "modern clinic"

**Nota**: Priorizar fotos propias para autenticidad y SEO.

---

**¡Manos a la obra!** 🎨✨
