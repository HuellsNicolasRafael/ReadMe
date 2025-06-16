# Trabajo Práctico Integrador – Programación Visual

> Carrera: Analista Programador Universitario
> Facultad de Ingeniería – Año 2025
> Materia: Programación Visual
> Modalidad: Trabajo grupal – Integrador Final

---

## 📚 Índice

- [🎯 Objetivo pedagógico](#-objetivo-pedagógico)
- [🛠️ Tecnologías utilizadas](#-tecnologías-utilizadas)
- [📁 Estructura del proyecto](#-estructura-del-proyecto)
- [🔧 Funcionalidades](#-funcionalidades)
- [⚙️ Detalle técnico por módulo](#-detalle-técnico-por-módulo)
- [🧪 Manual de pruebas](#-manual-de-pruebas)
- [🧹 Convenciones de código](#-convenciones-de-código)
- [🚀 Instalación y ejecución local](#-instalación-y-ejecución-local)
- [🧩 Posibles mejoras futuras](#-posibles-mejoras-futuras)
- [👥 Integrantes del grupo](#-integrantes-del-grupo)
- [📸 Captura de pantalla (ejemplo)](#-captura-de-pantalla-ejemplo)
- [📌 Notas finales](#-notas-finales)

---

## 🎯 Objetivo pedagógico

Este trabajo tiene como objetivo aplicar en conjunto los conocimientos adquiridos en Programación Visual a través del desarrollo de una SPA (Single Page Application) basada en React, utilizando un enfoque modular, profesional y con consumo de APIs REST externas.

Se busca que los estudiantes:

- Dominen el ciclo completo de una aplicación frontend (setup, desarrollo, testing, documentación).
- Comprendan el uso de herramientas modernas (React + Redux + Vite).
- Apliquen separación de responsabilidades, arquitectura por features y versionado por ramas.
- Trabajen colaborativamente usando Git y GitHub.

---

## 🛠️ Tecnologías utilizadas

- ⚛️ React 18
- ⚡ Vite
- 🧠 Redux Toolkit (estado global)
- 🔁 React Router DOM (SPA routing)
- 🌐 fetch API (consumo REST)
- 🛒 FakeStore API ([https://fakestoreapi.com/products](https://fakestoreapi.com/products))
- 🧰 ESLint (estándares de código)
- 📦 pnpm (package manager)
- 🗃️ Arquitectura modular por features
- 💬 Markdown (documentación)

---

## 📁 Estructura del proyecto

```bash
src/
├── assets/                      # Recursos gráficos
├── features/
│   ├── inicio/                  # Página principal (cards)
│   │   └── Inicio.jsx
│   ├── favoritos/               # Módulo de favoritos
│   │   ├── Favoritos.jsx
│   │   ├── FavoritoComponent.jsx
│   │   └── favoritosSlice.js
│   ├── detalle/                 # Detalle de productos
│   │   └── Detalle.jsx
│   └── formulario/              # Crear y editar productos
│       └── productosSlice.js
├── App.jsx                      # Rutas principales
├── main.jsx                     # Bootstrap de la app
├── store.js                     # Redux global store
└── vite.config.js
```

---

## 🔧 Funcionalidades

- Página de Inicio con cards de productos (imagen, nombre, precio, descripción, categoría).
- Checkbox o ícono para marcar productos como favoritos.
- Navegación SPA fluida entre rutas.
- Página de Detalle con información ampliada del producto.
- Página de Favoritos filtrando por estado global.
- Componente de formulario reutilizable para crear o editar productos.
- Estado global compartido para productos y favoritos.
- Modularización y separación por responsabilidades.

---

## ⚙️ Detalle técnico por módulo

| Módulo     | Descripción                                                                                                          |
| ---------- | -------------------------------------------------------------------------------------------------------------------- |
| Inicio     | Carga los productos desde FakeStore API. Renderiza cada item como card con botón de detalles y checkbox de favorito. |
| Favoritos  | Filtra los productos marcados por el usuario. Usa favoritosSlice.js para gestión del estado.                         |
| Detalle    | Muestra descripción completa. Se accede por id desde React Router DOM (parámetro en URL).                            |
| Formulario | Permite crear o editar un producto. El formulario es dinámico y reutilizable. Maneja validaciones básicas.           |
| Redux      | store.js centraliza slices. Redux Toolkit se encarga de immutabilidad y lógica de actualización.                     |

---

## 🧪 Manual de pruebas

| Componente | Qué probar                         | Cómo                                               |
| ---------- | ---------------------------------- | -------------------------------------------------- |
| Inicio     | Cards cargadas correctamente       | Refrescar y verificar la carga desde API externa   |
| Favoritos  | Estado persistente                 | Marcar favoritos y cambiar de página               |
| Detalle    | Navegación con ID dinámico         | Verificar redirección desde botón “Ver más”        |
| Formulario | Edición con datos pre-cargados     | Simular edición desde estado local                 |
| Redux      | Estados actualizados correctamente | Usar Redux DevTools para observar actions y states |

---

## 🧹 Convenciones de código

- JSX con PascalCase en componentes.
- Nombres de archivo en camelCase.js para slices y componentes.
- Separación estricta de lógica (slices) y vista (JSX).
- Hooks y lógica de efectos en useEffect/useDispatch.
- Uso de variables de entorno si fuese necesario (API base URL).
- Commits semánticos: feat:, fix:, refactor:, doc:.

---

## 🚀 Instalación y ejecución local

1. Clonar el repositorio:

```bash
git clone https://github.com/usuario/tp-programacion-visual.git
cd tp-programacion-visual
```

2. Instalar dependencias:

```bash
pnpm install
```

3. Ejecutar servidor local:

```bash
pnpm dev
```

4. Acceder a la app:

```
http://localhost:5173
```

---

## 🧩 Posibles mejoras futuras

- Integración de autenticación (ej: Firebase Auth).
- Testing con Jest + React Testing Library.
- Persistencia real de productos nuevos (simulada actualmente).
- Deploy en Netlify o Vercel.
- Uso de una base de datos falsa tipo json-server.

---

## 👥 Integrantes del grupo

| Nombre completo  | Usuario GitHub |
| ---------------- | -------------- |
| Juan Pérez       | @juanp         |
| Mariela González | @mgonzalez     |
| Lucas Herrera    | @lucash        |

> Reemplazar con los datos reales de tu equipo

---

## 📸 Captura de pantalla (ejemplo)

Vista del Home:

![Vista de productos](https://via.placeholder.com/900x500.png?text=Captura+de+pantalla+Home)

---

## 📌 Notas finales

Este proyecto fue desarrollado como evaluación final integradora de la materia Programación Visual.
Cada integrante asumió roles técnicos diferentes (ruteo, estado, diseño UI, lógica) para fomentar el trabajo colaborativo.
La entrega está estructurada, documentada y versionada conforme a buenas prácticas modernas.

---

¿Querés que te lo divida en secciones independientes para documentación interna también (por ejemplo, un README por cada feature)? Puedo ayudarte a armar una Wiki o guía de navegación técnica.
