## 🛠️ Estructura del Proyecto

    vr-files/
    │
    ├── index.html   ← Interfaz web / listado de archivos
    ├── README.md    ← Tutorial completo del proyecto
    └── files/       ← Activos VR (.glb, texturas, etc.)

---

## ⚙️ Configuración del Proyecto

El archivo `index.html` es el motor de la web.  
En la parte superior del script se define la constante `CONFIG`, donde se puede personalizar:

- Usuario GitHub: `jc-csl`
- Repositorio: `vr-files`
- Carpeta de activos: `files`
- Título de la página: configurable mediante la variable `tituloPagina`

No se necesita compilación ni servidor local.  
Cada cambio subido al repositorio se publica automáticamente mediante GitHub Pages.

---

## 📁 Cómo Subir Archivos al CDN

### Opción A — Subida desde la Web (GitHub)

1. Acceder al repositorio.
2. Entrar en la carpeta `/files`.
3. Pulsar **Add file → Upload files**.
4. Arrastrar los archivos `.glb`.
5. Pulsar **Commit changes**.

---

### Opción B — Subida desde el Ordenador (Git)

1. Clonar el repositorio:

        git clone https://github.com/jc-csl/vr-files.git
        cd vr-files

2. Copiar los modelos a la carpeta:

        vr-files/files

3. Subir los cambios:

        git add .
        git commit -m "Añadir nuevos modelos VR"
        git push origin main

---

## 🔑 Configuración de Acceso SSH (Recomendado)

### 1️⃣ Generar clave SSH

        ssh-keygen -t ed25519 -C "tu-correo@ejemplo.com"

### 2️⃣ Copiar la clave pública

        type %userprofile%\.ssh\id_ed25519.pub

### 3️⃣ Añadir la clave a GitHub

1. Ir a **GitHub → Settings → SSH and GPG keys**
2. Pulsar **New SSH key**
3. Asignar un nombre al equipo
4. Pegar la clave pública y guardar

### 4️⃣ Cambiar el origen del repositorio a SSH

        git remote set-url origin git@github.com:jc-csl/vr-files.git

---

## 🔗 Uso de los Archivos en Proyectos VR

Cada archivo subido a `/files` queda accesible mediante URL directa:

        https://jc-csl.github.io/vr-files/files/nombre-del-modelo.glb

Ejemplo en A-Frame:

        <a-entity 
          gltf-model="https://jc-csl.github.io/vr-files/files/modelo.glb"
          position="0 0 -3">
        </a-entity>

---

## ℹ️ Notas Importantes

- Unidades: tamaños mostrados en MB.
- Copiar enlace: botón integrado en la interfaz web.
- Visibilidad: el repositorio debe ser **Público**.
- Límite recomendado: archivos menores de **100 MB**.

---

## 🚀 Actualizar el README

        git add README.md
        git commit -m "Actualizar tutorial del proyecto"
        git push

---

## 👤 Autor

Repositorio mantenido por **jc-csl**  
Uso como CDN personal de activos VR / 3D.
