# 🎰 Blog de Regulación de Gaming en México

Blog profesional sobre regulación de casinos, licencias DGJS, LFPIORPI, impuestos y cumplimiento normativo en México.

## 🚀 Características

- ✅ **Responsivo**: Compatible con móvil, tablet y desktop
- 💬 **Comentarios**: Sistema de comentarios abierto sin autenticación
- 🔍 **Búsqueda**: Filtrado de posts por término y categoría
- 🎨 **Diseño profesional**: Interfaz limpia y moderna
- 📱 **PWA-ready**: Funciona offline (opcional)
- ⚡ **Rápido**: Optimizado para Vercel

## 📋 Contenido Incluido

1. **Regulación de Casinos en México** - Marco legal
2. **Licencias DGJS** - Proceso de obtención
3. **LFPIORPI (Antilavado)** - Obligaciones de PLD/AML
4. **Impuestos en Gaming** - IEPS, erogaciones, impacto tributario

## 🛠 Stack Técnico

- **Frontend**: React 18
- **Hosting**: Vercel (gratis)
- **Almacenamiento de comentarios**: localStorage (cliente)
- **CSS**: Vanilla CSS (sin dependencias externas)

## 📦 Instalación Local

### Prerrequisitos
- Node.js 16+ 
- npm o yarn

### Pasos

```bash
# 1. Clonar o descargar el repositorio
cd gaming-blog/frontend

# 2. Instalar dependencias
npm install

# 3. Ejecutar en desarrollo
npm start
```

La aplicación se abrirá en `http://localhost:3000`

## 🌐 Deployment en Vercel

### Opción 1: Desde Vercel Dashboard (Recomendado)

1. **Crear cuenta en Vercel**: https://vercel.com/signup
2. **Conectar GitHub**:
   - Sube este proyecto a GitHub
   - En Vercel, click en "Add New Project"
   - Selecciona el repositorio
3. **Configurar**:
   - Framework: React
   - Build Command: `cd frontend && npm install && npm run build`
   - Output Directory: `frontend/build`
   - Click "Deploy"

4. **¡Listo!** Tu blog estará en vivo en una URL como `tu-blog.vercel.app`

### Opción 2: Desde CLI (Línea de comandos)

```bash
# 1. Instalar Vercel CLI globalmente
npm install -g vercel

# 2. Iniciar sesión
vercel login

# 3. En la carpeta del proyecto, ejecutar
vercel

# 4. Seguir las instrucciones interactivas
```

## 📝 Agregar Nuevos Posts

Editar `/frontend/src/data/posts.js`:

```javascript
{
  id: 5,
  title: "Tu nuevo artículo",
  author: "Tu nombre",
  date: "2024-07-15",
  category: "Nueva Categoría",
  image: "URL de imagen",
  excerpt: "Resumen del artículo...",
  content: `# Título
  
Contenido en markdown...
  `,
  commentCount: 0
}
```

## 🎨 Personalizar Colores

Editar `/frontend/src/App.css`:

```css
/* Cambiar colores principales */
.header {
  background: linear-gradient(135deg, #TU_COLOR_1 0%, #TU_COLOR_2 100%);
}

.post-category {
  background-color: #TU_COLOR_ACENTO;
}
```

## 📱 Responsive Design

El blog es totalmente responsive:
- **Desktop**: 3 columnas de posts
- **Tablet**: 2 columnas
- **Móvil**: 1 columna

## 💬 Sistema de Comentarios

- **Almacenamiento**: localStorage del navegador
- **Persistencia**: Los comentarios se guardan en el cliente
- **Sin moderar**: Todos los comentarios se publican inmediatamente
- **Anónimo**: No se requiere login

**Nota**: Si quieres comentarios en servidor, puedes agregar una API con:
- Firebase/Firestore (gratis hasta cierto punto)
- MongoDB + Express
- Supabase (PostgreSQL gratis)

## 🔧 Personalización Avanzada

### Cambiar nombre del blog

1. Editar `Header.jsx`
2. Cambiar título en `index.html`
3. Actualizar en `vercel.json`

### Agregar Google Analytics

Agregar a `public/index.html`:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

### Agregar formulario de contacto

1. Instalar: `npm install axios`
2. Crear componente `ContactForm.jsx`
3. Usar servicio como Formspree o EmailJS

## 📚 Estructura del Proyecto

```
gaming-blog/
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── components/
│   │   │   ├── Header.jsx
│   │   │   ├── PostList.jsx
│   │   │   ├── PostDetail.jsx
│   │   │   └── CommentSection.jsx
│   │   ├── data/
│   │   │   └── posts.js
│   │   ├── App.jsx
│   │   ├── App.css
│   │   └── index.jsx
│   └── package.json
├── vercel.json
├── .gitignore
└── README.md
```

## 🚨 Solución de Problemas

### "Error: Module not found"
```bash
cd frontend
npm install
```

### Los comentarios no se guardan
- Verifica que localStorage no esté deshabilitado en el navegador
- Prueba en modo incógnito
- En navegadores privados, localStorage es limitado

### Cambios no se ven después de deploy
```bash
# Forzar redeploy
vercel --prod
```

## 📞 Contacto

Para soporte o preguntas: [Tu email aquí]

## 📄 Licencia

Este proyecto está bajo licencia MIT. Libre para usar, modificar y distribuir.

---

**¡Felicidades por tu nuevo blog sobre regulación de gaming! 🎉**
