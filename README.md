# 🦄 Pegasus IT — Landing Page PWA

Landing page profesional para consultora IT, construida con HTML/CSS/JS vanilla + PWA completa.

## 📁 Estructura de archivos

```
pegasus/
├── index.html          → HTML semántico con todas las secciones
├── styles.css          → CSS modular con variables, animaciones y responsive
├── script.js           → JS vanilla modular (i18n, canvas, form, PWA, etc.)
├── manifest.json       → Manifiesto PWA completo
├── service-worker.js   → SW con cache-first + network-first strategies
├── offline.html        → Página de fallback offline
├── icons/
│   ├── favicon.svg     → Favicon vectorial
│   ├── icon-32.png
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── icon-128.png
│   ├── icon-144.png
│   ├── icon-152.png
│   ├── icon-192.png    → Ícono principal PWA
│   ├── icon-384.png
│   └── icon-512.png    → Ícono splash screen
└── screenshots/        → (agregar capturas desktop + mobile)
```

## 🚀 Instrucciones de uso

### Desarrollo local
```bash
# Con Python (sin dependencias)
python3 -m http.server 8080

# Con Node.js
npx serve .

# Con VS Code: instalar "Live Server" y abrir index.html
```

Luego abrí http://localhost:8080

> ⚠️ El service worker requiere HTTPS en producción o `localhost` en desarrollo.

### Producción (Netlify / Vercel)
1. Subí la carpeta completa al repositorio
2. Conectá con Netlify/Vercel
3. Build command: (ninguno)
4. Publish directory: `.`

### Integración de formulario real
En `script.js`, función `initContactForm()`, reemplazá la línea de simulación:
```js
// SIMULADO:
await new Promise(r => setTimeout(r, 1600));

// REAL (ejemplo con Formspree):
const response = await fetch('https://formspree.io/f/TU_ID', {
  method: 'POST',
  body: formData,
  headers: { 'Accept': 'application/json' }
});
if (!response.ok) throw new Error('Error de envío');
```

**Servicios recomendados:** Formspree, EmailJS, Resend, o tu propio endpoint.

## ✨ Funcionalidades

| Feature | Estado |
|---|---|
| Diseño responsive mobile-first | ✅ |
| Animaciones CSS + Intersection Observer | ✅ |
| Canvas con partículas (Hero) | ✅ |
| Multi-idioma ES/EN | ✅ |
| PWA instalable | ✅ |
| Service Worker con cache offline | ✅ |
| Formulario con validación JS | ✅ |
| WhatsApp + Email integrado | ✅ |
| Navegación suave | ✅ |
| Contador animado | ✅ |
| SEO + Open Graph | ✅ |
| Accesibilidad (a11y) | ✅ |

## 🛠 Personalización

### Colores (en `styles.css`)
```css
:root {
  --clr-primary:  #6C63FF;  /* Violet principal */
  --clr-accent:   #00D4FF;  /* Cyan acento */
  --clr-bg:       #07070e;  /* Fondo oscuro */
}
```

### Agregar idioma
En `script.js`, agregá un nuevo objeto en `translations`:
```js
const translations = {
  es: { ... },
  en: { ... },
  pt: { /* nuevo idioma */ }
}
```

### Screenshots PWA (recomendado)
Agregá capturas en `/screenshots/`:
- `desktop.png` (1280×720)
- `mobile.png` (390×844)

## 📞 Contacto configurado

- Email: dandrada23@gmail.com
- WhatsApp: +54 11 5061 0043

---
*Desarrollado para Pegasus IT — 2025*
# pegasus
