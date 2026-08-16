# Práctica de Autómatas, Gramáticas y Lenguajes — UNED

App web autónoma para practicar las 534 preguntas de los exámenes de Junio (2022, 2023, 2024) de la asignatura *Autómatas, Gramáticas y Lenguajes* del 1.º curso del Grado en Ingeniería Informática / Ingeniería TI de la UNED.

## Contenido del paquete

```
.
├── index.html              # La app de práctica (autocontenida, sin dependencias externas)
├── examen_original.pdf     # PDF original con todas las preguntas y soluciones razonadas
└── README.md               # Este archivo
```

## Funcionalidad de la app

- 534 preguntas con sus 4 opciones (a/b/c/d) tal cual aparecen en el PDF original (con sus diagramas de autómatas, gramáticas, MTs, etc).
- Al responder, se ilumina la opción correcta en verde y la fallada en rojo, y aparece la **solución razonada** del PDF.
- **Filtros**: todas / sin responder / acertadas / falladas — útil para repasar errores.
- **Navegación**: anterior, siguiente, aleatoria.
- **Estadísticas** persistentes con barra de progreso.
- **Atajos de teclado**: `A`-`D` o `1`-`4` para responder, `←` `→` `Espacio` para navegar, `R` para aleatoria.
- **Progreso guardado** en el `localStorage` del navegador. Botón "Reiniciar" para empezar de cero.

---

## Uso en local (Windows / macOS / Linux)

### Opción 1: doble click

1. Descomprime el zip en cualquier carpeta.
2. Haz **doble click** sobre `index.html` — se abrirá en tu navegador por defecto.
3. ¡Listo! Funciona sin internet, sin instalación, sin servidor.

> **Recomendado**: Chrome, Firefox o Edge actualizados. El archivo HTML pesa ~27 MB porque embebe todas las imágenes de las preguntas, así que la primera carga puede tardar 2-3 segundos.

### Opción 2: navegador específico

Si quieres abrirlo con un navegador concreto:

- **Windows**: click derecho sobre `index.html` → *Abrir con* → elige Chrome/Firefox/Edge.
- **macOS**: click derecho → *Abrir con* → navegador.

---

## Publicar en GitHub Pages (acceso desde cualquier dispositivo)

Si quieres que la app esté accesible desde tu móvil, tablet u otro PC mediante una URL pública, puedes alojarla gratis en GitHub Pages.

### Paso a paso

#### 1. Crear cuenta en GitHub

Si no tienes ya: ve a [github.com](https://github.com) y regístrate.

#### 2. Crear un nuevo repositorio

1. Click en el botón verde **"New"** (o ve a https://github.com/new).
2. **Repository name**: por ejemplo, `practica-automatas`.
3. **Visibility**: marca **Public** (necesario para GitHub Pages gratis).
4. **NO** marques "Add a README file" (ya tienes uno).
5. Click en **"Create repository"**.

#### 3. Subir los archivos

Tienes dos formas:

**A) Mediante la web de GitHub (recomendado, más fácil):**

1. En la página del repositorio recién creado, verás un enlace que pone *"uploading an existing file"*. Click ahí.
2. Arrastra los 3 archivos del paquete (`index.html`, `examen_original.pdf`, `README.md`) a la zona de subida.
3. Espera a que se suban (`index.html` tarda un poco por el tamaño).
4. Abajo, en *"Commit changes"*, escribe un mensaje como `Subida inicial` y haz click en **"Commit changes"**.

**B) Mediante línea de comandos (si tienes Git instalado):**

```bash
cd carpeta-donde-descomprimiste-el-zip
git init
git add index.html examen_original.pdf README.md
git commit -m "Subida inicial"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/practica-automatas.git
git push -u origin main
```

#### 4. Activar GitHub Pages

1. En tu repositorio, ve a **Settings** (pestaña arriba a la derecha).
2. En el menú lateral izquierdo, busca **Pages**.
3. En la sección **Source**, despliega el selector y elige **Deploy from a branch**.
4. En **Branch**, elige `main` y deja la carpeta en `/ (root)`.
5. Click en **Save**.
6. Espera 1-2 minutos. Vuelve a recargar la página de Pages — verás una URL parecida a:
   ```
   https://TU_USUARIO.github.io/practica-automatas/
   ```
7. Abre esa URL en cualquier navegador. ¡Ya tienes tu app online!

### Notas sobre GitHub Pages

- La URL es **pública**: cualquiera con el enlace puede acceder. Si te preocupa, deja el repo privado y usa otra solución (Netlify, Vercel) — pero recuerda que las preguntas y soluciones son material académico ya distribuido por la UNED.
- El progreso se guarda **localmente en cada navegador**: si entras desde el móvil y luego desde el PC, son progresos separados.
- GitHub Pages tiene un límite de **1 GB por repo** y **100 GB de tráfico al mes** en cuentas gratuitas — más que suficiente para uso personal.

---

## Solución de problemas

| Problema | Solución |
|----------|----------|
| El archivo HTML no abre / aparece como texto | Asegúrate de que el archivo se llama `index.html` (no `index.html.txt`). En Windows, activa *Ver extensiones de archivo* en el Explorador. |
| Las imágenes no se ven | Algún navegador muy antiguo no soporta `data:` URIs grandes. Usa Chrome/Firefox/Edge actualizados. |
| Quiero empezar de cero | Click en el botón **Reiniciar** (esquina superior derecha de los controles). |
| Subo el HTML a GitHub y tarda mucho | Es normal: 27 MB es bastante. Espera a que termine la subida antes de cerrar la pestaña. |
| GitHub Pages muestra error 404 | Espera 5 minutos tras activar Pages. Si persiste, comprueba que el archivo se llama exactamente `index.html` (minúsculas). |

---

## Créditos

- Preguntas y soluciones: equipo docente de la UNED (Elena Gaudioso Vázquez y Félix Hernández del Olmo).
- App: construida sobre los enunciados del PDF *Soluciones a los exámenes de Junio 2022* (con material adicional de 2023 y 2024).
