# Mi Bolsillo COP - Compilación Automática de APK en GitHub Actions (Versión 100% Offline)

Este paquete contiene tu aplicación (`www/index.html`) adaptada para **Capacitor** junto con el flujo automático de **GitHub Actions** para generar el instalador `.apk` directamente desde tu celular sin necesidad de PC.

> **Mejora Offline:** Se eliminaron todas las dependencias remotas (Tailwind CSS, fuentes de Google Fonts y llamadas automáticas a Firebase). Ahora la app viene con todos los recursos empaquetados localmente, garantizando que cargue al instante y funcione sin internet ni datos móviles.

## Estructura de archivos:
- `package.json`
- `capacitor.config.json`
- `.github/workflows/build-apk.yml`
- `www/`
  - `index.html` (código de la app adaptado para uso local offline)
  - `tailwind.js` (motor Tailwind CSS descargado localmente)
  - `fonts/`
    - `inter.css` (estilos de fuentes locales)
    - `inter-latin.woff2` (fuente Inter normal/negrita)
    - `inter-latin-ext.woff2` (fuente Inter caracteres extendidos)

## Pasos para compilar tu APK:

1. **Subir los cambios a tu repositorio en GitHub:**
   - Sube todos los archivos respetando la estructura (`package.json`, `capacitor.config.json`, la carpeta `.github/` y toda la carpeta `www/`).
   - Haz commit de los cambios en la rama `main` o `master`.

2. **Descargar tu APK compilado:**
   - Ve a la pestaña **Actions** dentro de tu repositorio en GitHub.
   - Verás ejecutándose el workflow **Compilar APK Android (Capacitor)** (~3 minutos).
   - Cuando aparezca el check verde, entra a la ejecución y baja hasta la sección **Artifacts**.
   - Toca **`MiBolsilloCOP-Android-APK`** para descargar el instalador `.apk` listo para tu celular.
