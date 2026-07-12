# 🚀 Guía Rápida: Desplegar tu Blog en Vercel

**Tiempo total**: ~5 minutos

## Paso 1: Crear cuenta en GitHub (si no la tienes)

1. Ve a https://github.com/signup
2. Completa el registro con:
   - Email
   - Contraseña
   - Username
3. Confirma tu email

## Paso 2: Subir el proyecto a GitHub

### Opción A: Usar Git desde terminal (Recomendado si conoces terminal)

```bash
# En la carpeta gaming-blog
git init
git add .
git commit -m "Primer commit: Blog de gaming"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/gaming-blog.git
git push -u origin main
```

### Opción B: GitHub Desktop (Más fácil visualmente)

1. Descarga GitHub Desktop: https://desktop.github.com
2. Abre y inicia sesión con tu cuenta GitHub
3. Click en "Create a New Repository"
4. Nombre: `gaming-blog`
5. Local path: Donde descargaste los archivos
6. Click "Create Repository"
7. Click "Publish repository"

## Paso 3: Crear cuenta en Vercel

1. Ve a https://vercel.com/signup
2. Click en "Continue with GitHub"
3. Autoriza a Vercel acceder a tu GitHub
4. Completa perfil

## Paso 4: Desplegar en Vercel

1. En Vercel dashboard, click "Add New Project"
2. Click "Import Git Repository"
3. Busca y selecciona `gaming-blog`
4. Click "Import"

### Configuración Importante:

En la sección "Build and Output Settings":

```
Framework Preset: Create React App
Build Command: cd frontend && npm install && npm run build
Output Directory: frontend/build
Install Command: cd frontend && npm install
```

5. Click "Deploy"

**¡Listo! Vercel te dará una URL como:**
```
https://gaming-blog-abc123.vercel.app
```

## Paso 5: Tu dominio personalizado (Opcional)

Después del primer deploy:

1. En Vercel, entra a tu proyecto
2. Ve a Settings → Domains
3. Agrega tu dominio:
   - Si tienes dominio propio, configura los DNS
   - O compra uno directamente en Vercel

## 🔄 Actualizar el blog después

Si haces cambios en tu código:

```bash
git add .
git commit -m "Descripción del cambio"
git push
```

Vercel detectará automáticamente el cambio y redesplegará. ¡Sin hacer nada más!

## 🆘 Errores Comunes

### ❌ "Build failed"
**Solución**: Verifica que la carpeta `frontend/` tenga `package.json`

### ❌ "Module not found react"
**Solución**: Asegúrate de que instalaste dependencias en frontend

### ❌ "Cannot find src/index.jsx"
**Solución**: Verifica la estructura de carpetas

## ✅ Verificar que todo funcionó

1. Abre tu URL de Vercel
2. Deberías ver:
   - Encabezado azul con título del blog
   - 4 posts de ejemplo
   - Buscador y filtrador funcionales
   - Puedas hacer click en posts

## 🎉 ¡Felicidades!

Tu blog de regulación de gaming está vivo en internet. Ahora puedes:

✅ Compartir la URL con colegas y clientes  
✅ Agregar más posts editando `posts.js`  
✅ Personalizar colores en `App.css`  
✅ Los comentarios se guardan automáticamente  

---

**¿Necesitas ayuda?** 
- Contacta al equipo de Vercel: vercel.com/support
- Documentación React: react.dev
