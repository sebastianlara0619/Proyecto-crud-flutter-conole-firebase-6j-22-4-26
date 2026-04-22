¡Excelente elección! Integrar Firebase con Flutter es un combo muy potente. Para que todo funcione sobre ruedas, el **Firebase CLI** (Command Line Interface) es tu mejor amigo, ya que automatiza gran parte de la configuración.

Aquí tienes la guía paso a paso para dejar tu entorno listo.

---

## 1. Verificación de Node.js y npm

Antes de instalar nada, debemos ver si ya tienes las herramientas en tu sistema.

* **¿Qué es npm?** Es el gestor de paquetes que viene con **Node.js**. Lo usaremos para descargar e instalar las herramientas de Firebase.
* **Versión recomendada:** Se sugiere utilizar la versión **LTS** (Long Term Support) de Node.js para evitar errores de compatibilidad.

### Comandos de verificación:
Abre tu terminal (PowerShell en Windows, Terminal en macOS/Linux) y escribe:

1.  `node -v` (Muestra la versión de Node.js)
2.  `npm -v` (Muestra la versión de npm)

> **Nota:** Si recibes un error tipo "comando no encontrado", significa que debemos instalarlo desde cero.

---

## 2. Instalación de Node.js y npm (Paso a paso)

Si no los tienes, sigue estos pasos:

1.  **Descarga:** Ve al sitio oficial [nodejs.org](https://nodejs.org/).
2.  **Selección:** Descarga la versión que dice **LTS** (actualmente suele ser la v20 o v22).
3.  **Instalación:**
    * **Windows/macOS:** Ejecuta el instalador `.msi` o `.pkg`. Dale a "Next" a todo. 
    * **IMPORTANTE:** Asegúrate de que la casilla **"Add to PATH"** esté marcada (esto permite que los comandos funcionen en cualquier carpeta).
4.  **Reinicio:** Una vez finalizada la instalación, **cierra y vuelve a abrir tu terminal** para que reconozca los cambios.

---

## 3. Instalación Global de Firebase CLI

Una vez que `npm` funciona, instalaremos las herramientas de Firebase de forma **global**. Esto significa que podrás usarlas en cualquier proyecto de tu computadora sin tener que reinstalarlas.

### Comando de instalación:
Ejecuta el siguiente comando en tu terminal:

```bash
npm install -g firebase-tools
```

* `-g`: Indica que la instalación es **global**.
* `firebase-tools`: Es el nombre del paquete que contiene el CLI.

---

## 4. Comandos esenciales de Firebase

Ahora que tienes la herramienta, veamos cómo usarla para conectar tu cuenta y tu proyecto.

### A. Cómo acceder con tu Cuenta de Google
Para que la consola sepa quién eres, debes iniciar sesión:

```bash
firebase login
```
* **Qué sucede:** Se abrirá una ventana en tu navegador. Elige tu cuenta de Google, acepta los permisos y ¡listo! La terminal te dirá "Success! Logged in as [tu_correo]".

### B. Cómo inicializar un proyecto en Firebase
Navega en la terminal hasta la carpeta raíz de tu proyecto de Flutter y ejecuta:

```bash
firebase init
```

**Este comando es un asistente interactivo. Pasos comunes:**
1.  **Selección de funciones:** Usa las flechas y la barra espaciadora para elegir qué necesitas (ej. *Firestore, Hosting, Storage*).
2.  **Proyecto:** Elige "Use an existing project" (si ya lo creaste en la web de Firebase) o "Create a new project".
3.  **Configuraciones:** Te pedirá nombres de archivos (puedes dejar los predeterminados presionando Enter).

---

## Tip Pro para Flutter: `flutterfire_cli`

Aunque el Firebase CLI es la base, para Flutter existe una herramienta específica llamada **FlutterFire CLI** que configura automáticamente tus archivos `google-services.json` y `GoogleService-Info.plist`.

Una vez instalado el Firebase CLI, te recomiendo ejecutar:
```bash
dart pub global activate flutterfire_cli
```
Luego, simplemente corres `flutterfire configure` y él hará todo el trabajo sucio por ti en Android e iOS.

¿Ya tienes creado el proyecto en la consola web de Firebase o te gustaría que te ayude con ese paso primero?
