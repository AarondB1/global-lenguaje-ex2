# Global Languages - Angular + Bootstrap

Proyecto académico de una página web institucional para el Centro de Idiomas **Global Languages**.

## Requisitos de la rúbrica cubiertos

- Idiomas disponibles y programas de estudio.
- Niveles de aprendizaje y modalidad de enseñanza.
- Información de docentes, especialidades e idiomas.
- Horarios y promociones.
- Testimonios de estudiantes.
- Historia, misión, visión y valores.
- Diseño responsive.
- Angular mediante componentes standalone y rutas.
- Bootstrap 5 + Bootstrap Icons.
- Servicio centralizado para los datos.
- Formulario funcional de solicitud de información.
- **Nuevo:** cuestionario interactivo de nivelación de inglés con progreso, validación de respuestas, resultado orientativo y recomendación de programa.
- Estructura preparada para trabajo con Git, ramas y Pull Requests.

## Instalación

```bash
npm install
npm start
```

Luego abre:

```text
http://localhost:4200
```

## Compilar para producción

```bash
npm run build
```

## Estructura

```text
src/app/
├── app.component.ts
├── app.config.ts
├── app.routes.ts
├── data/
│   └── language-center.service.ts
├── shared/
│   ├── navbar/
│   └── footer/
└── pages/
    ├── home/
    ├── idiomas/
    ├── nivelacion/  # Nuevo cuestionario interactivo
    ├── programas/
    ├── docentes/
    ├── horarios/
    ├── testimonios/
    └── nosotros/
```

## Git: flujo recomendado para demostrar la rúbrica

Primera configuración:

```bash
git init
git add .
git commit -m "chore: crear proyecto Angular Global Languages"
git branch -M main
```

Rama para inicio:

```bash
git checkout -b feature/inicio
git add .
git commit -m "feat: crear página de inicio responsive"
git checkout main
```

Rama para programas:

```bash
git checkout -b feature/programas
git add .
git commit -m "feat: agregar idiomas y programas de estudio"
git checkout main
```

Rama para docentes y horarios:

```bash
git checkout -b feature/docentes-horarios
git add .
git commit -m "feat: agregar docentes horarios y promociones"
git checkout main
```

Rama para testimonios y nosotros:

```bash
git checkout -b feature/institucional
git add .
git commit -m "feat: agregar testimonios e información institucional"
git checkout main
```

## Pull Requests

Si usas GitHub:

1. Crea el repositorio `global-languages`.
2. Sube `main`.
3. Publica cada rama.
4. Crea un Pull Request desde cada `feature/...` hacia `main`.
5. Revisa los cambios.
6. Integra el Pull Request.
7. Mantén mensajes de commit claros.

Ejemplo:

```bash
git remote add origin TU_URL_DEL_REPOSITORIO
git push -u origin main
git push -u origin feature/inicio
```

## Qué explicar al docente

- `app.routes.ts`: separa las páginas mediante rutas.
- `LanguageCenterService`: centraliza los datos para evitar repetir información.
- Cada carpeta de `pages` representa un componente funcional.
- `shared/navbar` y `shared/footer` son componentes reutilizables.
- Bootstrap aporta grid, botones, tablas, formularios y responsive.
- `@for` renderiza listas desde los datos del servicio.
- `HorariosComponent` usa `FormsModule` y un formulario funcional.
- `NivelacionComponent` gestiona las respuestas, calcula el puntaje y muestra una recomendación; la vista se actualiza con las plantillas de Angular.

## Estructura con app.html

El componente raíz usa `src/app/app.html` mediante `templateUrl`, y los componentes tienen sus propios archivos `.html` y `.css` para mantener la interfaz separada de la lógica TypeScript.
