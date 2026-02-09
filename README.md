# Simulador IS6 — CCU Atracción de Talento

Dashboard interactivo para proyectar la dotación IS6 en cualquier fecha, con filtrado por dotación vigente y actualización de movimientos organizacionales.

---

## Publicar en GitHub Pages (paso a paso)

### 1. Crear cuenta de GitHub (si no tienes)
- Ve a [github.com](https://github.com) y crea una cuenta gratuita

### 2. Instalar Git y Node.js en tu computador
- **Node.js**: Descarga e instala desde [nodejs.org](https://nodejs.org/) (versión LTS)
- **Git**: Descarga e instala desde [git-scm.com](https://git-scm.com/downloads)
- Después de instalar, reinicia tu computador

### 3. Descomprimir el proyecto
- Descomprime el archivo `simulador-is6.zip` en alguna carpeta de tu computador
- Por ejemplo en `C:\Users\TuNombre\simulador-is6`

### 4. Abrir terminal en la carpeta del proyecto
- En Windows: abre la carpeta, haz clic derecho en un espacio vacío y selecciona "Abrir en Terminal" o "Git Bash Here"
- En Mac: abre Terminal y navega con `cd ruta/a/simulador-is6`

### 5. Instalar dependencias
```bash
npm install
```

### 6. (Opcional) Probar localmente antes de publicar
```bash
npm run dev
```
Esto abre el simulador en `http://localhost:5173` para que lo veas antes de publicar.

### 7. Crear repositorio en GitHub
- Ve a [github.com/new](https://github.com/new)
- Nombre del repositorio: `simulador-is6`
- Dejalo como **Public** (necesario para GitHub Pages gratuito)
- NO marques "Add a README" ni nada más
- Click "Create repository"

### 8. Editar configuración con tu usuario
Abre el archivo `package.json` con un editor de texto y cambia esta línea:
```
"homepage": "https://TU_USUARIO.github.io/simulador-is6"
```
Reemplaza `TU_USUARIO` por tu nombre de usuario de GitHub.

También abre `vite.config.js` — si tu repositorio se llama distinto a `simulador-is6`, actualiza la línea `base`.

### 9. Subir el código a GitHub
```bash
git init
git add .
git commit -m "Simulador IS6 v1"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/simulador-is6.git
git push -u origin main
```
(Reemplaza `TU_USUARIO` por tu usuario real)

### 10. Publicar en GitHub Pages
```bash
npm run deploy
```
Este comando construye la app y la publica automáticamente.

### 11. Activar GitHub Pages (solo la primera vez)
- Ve a tu repositorio en GitHub
- Settings → Pages
- En "Source", selecciona la rama `gh-pages`
- Click "Save"
- Espera 1-2 minutos

### 12. Acceder al simulador
Tu simulador estará disponible en:
```
https://TU_USUARIO.github.io/simulador-is6/
```
Comparte este link con quien quieras — funciona desde cualquier navegador.

---

## Actualizar después de cambios

Si en el futuro haces cambios al código, solo necesitas:
```bash
git add .
git commit -m "Descripcion del cambio"
git push
npm run deploy
```

---

## Notas importantes

- **Privacidad**: Los datos están embebidos en el código JavaScript. Aunque no son visibles directamente en la página, alguien con conocimientos técnicos podría extraerlos. Si esto es un problema, considera usar un repositorio privado (requiere GitHub Pro o un dominio alternativo como Netlify con protección).
- **CSV de vigentes**: Los archivos que se suben a la app NO salen del navegador del usuario. Todo se procesa localmente, nada se envía a ningún servidor.
- **Sin servidor**: La app es 100% estática (HTML/JS/CSS), no necesita backend ni base de datos.
