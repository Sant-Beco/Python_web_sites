# 🐍 Mi Viaje con Python - Documentación del Proyecto

> Sitio web educativo basado en CS50's Introduction to Programming with Python

## 📁 Estructura del Proyecto

```
mi-viaje-python/
├── index.html                 # Página principal
├── weeks/                     # Páginas de cada semana
│   ├── week0.html            # Functions, Variables
│   ├── week1.html            # Conditionals
│   ├── week2.html            # Loops
│   ├── week3.html            # Exceptions (próximamente)
│   ├── week4.html            # Libraries (próximamente)
│   ├── week5.html            # Unit Tests (próximamente)
│   ├── week6.html            # File I/O (próximamente)
│   ├── week7.html            # Regular Expressions (próximamente)
│   ├── week8.html            # OOP (próximamente)
│   └── week9.html            # Et Cetera (próximamente)
├── assets/
│   ├── css/
│   │   └── styles.css        # 🎨 CSS CENTRALIZADO - UN SOLO ARCHIVO
│   └── js/
│       └── main.js           # JavaScript compartido
└── README.md                 # Este archivo
```

## 🎨 Sistema de Diseño

### Variables CSS Centralizadas

Todas las variables están definidas en `assets/css/styles.css`:

```css
:root {
    /* Colores */
    --bg-primary: #0a0e14;
    --bg-secondary: #151b23;
    --bg-code: #1a1f29;
    --accent-python: #ffd43b;
    --accent-blue: #4a9eff;
    --accent-green: #7ec699;
    --accent-red: #ff6b6b;
    
    /* Tipografía */
    --font-serif: 'Merriweather', serif;
    --font-mono: 'JetBrains Mono', monospace;
    
    /* Espaciado */
    --spacing-sm: 1rem;
    --spacing-md: 2rem;
    --spacing-lg: 3rem;
    
    /* Transiciones */
    --transition-normal: 0.3s ease;
}
```

## 🧩 Componentes Reutilizables

### 1. Cards (Tarjetas)
```html
<div class="card">
    <h3>Título</h3>
    <p>Contenido...</p>
</div>
```

### 2. Cajas Especiales

**Conceptos:**
```html
<div class="concept-box">
    <h3>Concepto</h3>
    <p>Explicación...</p>
</div>
```

**Ejemplos:**
```html
<div class="example-box">
    <h3>📝 Ejemplo</h3>
    <p>Código de ejemplo...</p>
</div>
```

**Advertencias:**
```html
<div class="warning-box">
    <h3>⚠️ Advertencia</h3>
    <p>Cuidado con...</p>
</div>
```

**Información:**
```html
<div class="info-box">
    <h3>ℹ️ Información</h3>
    <p>Dato importante...</p>
</div>
```

### 3. Bloques de Código
```html
<div class="code-container">
    <div class="code-header">
        <span class="code-dot red"></span>
        <span class="code-dot yellow"></span>
        <span class="code-dot green"></span>
        <span class="code-title">nombre_archivo.py</span>
    </div>
    <pre><code><span class="keyword">def</span> <span class="function">main</span>():
    <span class="function">print</span>(<span class="string">"Hola mundo"</span>)</code></pre>
</div>
```

**Clases de sintaxis:**
- `.keyword` - Palabras clave (def, if, for, etc.)
- `.function` - Nombres de funciones
- `.string` - Strings
- `.comment` - Comentarios
- `.number` - Números

### 4. Grids Responsivos
```html
<div class="content-grid">
    <div class="card">Card 1</div>
    <div class="card">Card 2</div>
    <div class="card">Card 3</div>
</div>
```

### 5. Navegación entre Páginas
```html
<div class="navigation">
    <a href="week0.html" class="nav-button prev">← Semana Anterior</a>
    <a href="week2.html" class="nav-button next">Semana Siguiente →</a>
</div>
```

## ✨ Animaciones Automáticas

Todas las secciones tienen animaciones `fadeInUp` automáticas con delays escalonados:

```css
.section:nth-child(1) { animation-delay: 1s; }
.section:nth-child(2) { animation-delay: 1.2s; }
.section:nth-child(3) { animation-delay: 1.4s; }
```

## 🎯 Características Interactivas (JavaScript)

### 1. Botón Copiar Código
Automáticamente agrega botones "📋 Copiar" a todos los bloques de código.

### 2. Progress Bar
Barra de progreso en la parte superior que muestra el scroll de la página.

### 3. Parallax Sutil
El fondo animado ajusta su opacidad según el scroll.

### 4. Smooth Scroll
Navegación suave al hacer click en enlaces internos.

## 📱 Responsive Design

El diseño es completamente responsive con breakpoint en 768px:

```css
@media (max-width: 768px) {
    .page-title { font-size: 2rem; }
    .content-grid { grid-template-columns: 1fr; }
    .navigation { flex-direction: column; }
}
```

## 🚀 Stack Tecnológico

- **HTML5** - Estructura semántica
- **CSS3** - Diseño y animaciones (Variables CSS, Grid, Flexbox)
- **JavaScript Vanilla** - Interactividad
- **Google Fonts** - Tipografía (Merriweather + JetBrains Mono)

## 📝 Cómo Crear una Nueva Página de Semana

1. **Copiar la estructura base:**
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semana X: Título | Mi Viaje con Python</title>
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Merriweather:wght@300;400;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="../assets/css/styles.css">
</head>
<body>
    <div class="bg-animation"></div>
    
    <header>
        <div class="header-content">
            <div class="header-title">
                <a href="../index.html" class="logo">🐍</a>
                <h1>Mi Viaje con Python</h1>
                <span class="week-badge">SEMANA X</span>
            </div>
            <nav>
                <a href="../index.html">Inicio</a>
                <a href="weekX.html" class="active">Semana X</a>
            </nav>
        </div>
    </header>

    <main>
        <div class="page-header">
            <h1 class="page-title">Semana X</h1>
            <p class="page-subtitle">Subtítulo del Tema</p>
        </div>

        <!-- Tus secciones aquí -->
        <section class="section">
            <div class="section-header">
                <span class="section-icon">📚</span>
                <h2>Título de Sección</h2>
            </div>
            <!-- Contenido -->
        </section>

        <div class="navigation">
            <a href="weekX-1.html" class="nav-button prev">← Semana Anterior</a>
            <a href="weekX+1.html" class="nav-button next">Semana Siguiente →</a>
        </div>
    </main>

    <footer>
        <p>🐍 Mi Viaje con Python | Semana X | CS50 2026</p>
    </footer>
    <script src="../assets/js/main.js"></script>
</body>
</html>
```

2. **Usar los componentes CSS existentes** (no crear estilos inline)
3. **Mantener la estructura de secciones** con iconos y headers
4. **Agregar navegación** entre semanas al final

## 🎨 Paleta de Colores

| Color | Variable | Uso |
|-------|----------|-----|
| ![#ffd43b](https://via.placeholder.com/15/ffd43b/000000?text=+) `#ffd43b` | `--accent-python` | Títulos principales, hover effects |
| ![#4a9eff](https://via.placeholder.com/15/4a9eff/000000?text=+) `#4a9eff` | `--accent-blue` | Subtítulos, enlaces |
| ![#7ec699](https://via.placeholder.com/15/7ec699/000000?text=+) `#7ec699` | `--accent-green` | Ejemplos, success |
| ![#ff6b6b](https://via.placeholder.com/15/ff6b6b/000000?text=+) `#ff6b6b` | `--accent-red` | Advertencias, errores |
| ![#0a0e14](https://via.placeholder.com/15/0a0e14/000000?text=+) `#0a0e14` | `--bg-primary` | Fondo principal |
| ![#151b23](https://via.placeholder.com/15/151b23/000000?text=+) `#151b23` | `--bg-secondary` | Cards, header |
| ![#1a1f29](https://via.placeholder.com/15/1a1f29/000000?text=+) `#1a1f29` | `--bg-code` | Bloques de código |

## 📋 Checklist para Nuevas Páginas

- [ ] Usar `<link rel="stylesheet" href="../assets/css/styles.css">`
- [ ] Incluir `<div class="bg-animation"></div>`
- [ ] Header con `.header-content`, `.header-title`, `.week-badge`
- [ ] `.page-header` con `.page-title` y `.page-subtitle`
- [ ] Secciones con clase `.section`
- [ ] Section headers con `.section-header` e ícono
- [ ] Bloques de código con estructura completa
- [ ] Navegación al final con `.navigation`
- [ ] Footer con información de la semana
- [ ] Script `<script src="../assets/js/main.js"></script>` antes de `</body>`

## 🎓 Contenido Actual

### ✅ Completadas:
- **Semana 0:** Functions, Variables (100% completa)
- **Semana 1:** Conditionals (100% completa)
- **Semana 2:** Loops (100% completa)

### 🔜 Próximamente:
- Semana 3: Exceptions
- Semana 4: Libraries
- Semana 5: Unit Tests
- Semana 6: File I/O
- Semana 7: Regular Expressions
- Semana 8: Object-Oriented Programming
- Semana 9: Et Cetera

## 💡 Tips de Desarrollo

1. **Nunca uses estilos inline** - Todo debe estar en `styles.css`
2. **Reutiliza las clases existentes** - No inventes nuevas si no es necesario
3. **Mantén la consistencia** - Usa los mismos patrones en todas las páginas
4. **Optimiza imágenes** - Si agregas imágenes, comprimelas
5. **Testa responsive** - Siempre verifica en móvil

## 🔧 Mantenimiento

### Modificar Colores
Editar las variables en `:root` en `styles.css`

### Cambiar Tipografía
Modificar las variables `--font-serif` y `--font-mono`

### Ajustar Espaciado
Cambiar las variables `--spacing-*`

## 📄 Licencia

Este proyecto es un recurso educativo personal basado en el curso CS50 de Harvard.

## 🙏 Créditos

- **CS50's Introduction to Programming with Python** - Harvard University
- **David J. Malan** - Instructor del curso
- **Diseño y Desarrollo** - Mi Viaje de Aprendizaje 2026

---

**🐍 Happy Coding! 🚀**