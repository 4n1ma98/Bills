# Mi Bolsillo COP - Compilación Automática de APK en GitHub Actions

Este paquete contiene tu aplicación (`www/index.html`) adaptada para **Capacitor** junto con el flujo automático de **GitHub Actions** para generar el instalador `.apk` directamente desde tu celular sin necesidad de PC.

## Pasos desde tu POCO X7 Pro:

1. **Crear repositorio en GitHub:**
   - Entra a [github.com](https://github.com) desde Chrome en tu celular e inicia sesión.
   - Toca el botón **`+`** (arriba a la derecha) -> **New repository**.
   - Ponle nombre (ej. `mi-bolsillo-cop`), déjalo **Privado** o **Público** y toca **Create repository**.

2. **Subir los archivos del ZIP:**
   - Descomprime este archivo `.zip` en tu carpeta `Download` usando el Gestor de Archivos de Xiaomi.
   - En la página de tu repositorio nuevo en GitHub, toca **uploading an existing file** (si no lo ves en móvil, activa *"Sitio de escritorio"* en los 3 puntos de Chrome).
   - Selecciona y sube todos los archivos manteniendo la estructura:
     - `package.json`
     - `capacitor.config.json`
     - `www/index.html`
     - `.github/workflows/build-apk.yml`
   - Toca **Commit changes**.

3. **Descargar tu APK compilado:**
   - Ve a la pestaña **Actions** dentro de tu repositorio en GitHub.
   - Verás ejecutándose el workflow **Compilar APK Android (Capacitor)** (tarda ~3 minutos).
   - Cuando aparezca el check verde, entra a la ejecución y baja hasta **Artifacts**.
   - Toca **`MiBolsilloCOP-Android-APK`** para descargar el `.zip` con tu `app-debug.apk` listo para instalar en Android.

## Nota sobre tus datos actuales
Al instalar el APK por primera vez, la app tendrá su base de datos interna limpia. Antes de migrar:
1. Abre tu versión actual en el navegador y descarga tu respaldo `.json`.
2. Abre la app instalada **Mi Bolsillo COP**, ve a **Gestión de Datos / JSON -> Importar JSON** y carga ese archivo.
3. A partir de ahí, el botón **Compartir** adjuntará el `.json` directamente en WhatsApp, Drive o cualquier app de Android.
