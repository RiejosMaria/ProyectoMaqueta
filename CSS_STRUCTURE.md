# Estructura CSS Modular - ProyectoMaqueta

## 📁 Directorio `/components/`

Los estilos CSS se han separado en archivos modulares específicos por componente. Esto mejora la **mantenibilidad**, **rendimiento** y **organización** del código.

### Orden de Carga en HTML

Los archivos CSS se cargan en este orden específico (importante para evitar conflictos):

1. **variables.css** - Variables CSS globales y temas (colores, espacios, etc.)
2. **reset.css** - Reset global, estilos base del body, títulos, párrafos
3. **header.css** - Header, navbar, menú hamburguesa
4. **theme-switcher.css** - Selector de tema (claro/oscuro)
5. **hero.css** - Sección hero principal
6. **buttons.css** - Todos los tipos de botones
7. **layout.css** - Grids principales y layout
8. **cards.css** - Cards de artículos
9. **flip-cards.css** - Cards giratorias
10. **tabs.css** - Sistema de tabs
11. **sidebar.css** - Sidebar y widgets
12. **media.css** - Media boxes, videos, listas
13. **tables.css** - Tablas y badges
14. **forms.css** - Formularios y controles
15. **footer.css** - Footer
16. **carousel.css** - Carrusel
17. **bento.css** - Grid Bento
18. **accordion.css** - Acordeón

## 📊 Componentes Incluidos

| Componente    | Archivo              | Resumen                                      |
| ------------- | -------------------- | -------------------------------------------- |
| Variables CSS | `variables.css`      | Colores, tipografía, radios, espacios        |
| Reset Global  | `reset.css`          | Estilos iniciales, body, links, img          |
| Header        | `header.css`         | Navbar, logo, navegación, hamburguesa        |
| Theme Picker  | `theme-switcher.css` | Selector de tema claro/oscuro/sistema        |
| Hero          | `hero.css`           | Sección principal con gradientes             |
| Botones       | `buttons.css`        | Botones primarios, secundarios, hero buttons |
| Layout        | `layout.css`         | Grid principal responsive                    |
| Cards         | `cards.css`          | Cards de artículos con hover                 |
| Flip Cards    | `flip-cards.css`     | Cards giratorias en 3D                       |
| Tabs          | `tabs.css`           | Pestañas sin JavaScript                      |
| Sidebar       | `sidebar.css`        | Barra lateral, widgets, avatar SVG           |
| Media         | `media.css`          | Listas, videos, feature boxes                |
| Tables        | `tables.css`         | Tablas, badges de estado                     |
| Forms         | `forms.css`          | Inputs, selects, fieldsets, validación       |
| Footer        | `footer.css`         | Pie de página                                |
| Carousel      | `carousel.css`       | Carrusel de imágenes puro CSS                |
| Bento         | `bento.css`          | Grid Bento masonry                           |
| Accordion     | `accordion.css`      | Acordeón con detalles/summary                |

## 🎨 Variables CSS Globales

Definidas en `variables.css`:

```css
--primary: #4338ca /* Color primario */ --primary-dark: #3730a3 /* Color primario oscuro */ --secondary: #0284c7 /* Color secundario */ --bg: #f8fafc
  /* Fondo */ --surface: #ffffff /* Superficie (cards, etc) */ --text: #1e293b /* Texto */ --title: #1e293b /* Títulos */ --text-muted: #475569
  /* Texto atenuado */ --text-light: #ffffff /* Texto claro */ --border: #e2e8f0 /* Bordes */ --success: #059669 /* Verde de éxito */ --error: #dc2626
  /* Rojo de error */ --radius: 8px /* Radio de bordes */;
```

### Tema oscuro

Se activa automáticamente con:

- `<html data-theme="dark">`
- `<html data-theme="system">` (respeta preferencias del SO)

## 🔧 Cómo Modificar

### Cambiar colores globales

Edita `variables.css` - Los cambios se aplicarán a todo el sitio.

### Añadir un nuevo componente

1. Crea un archivo `components/mi-componente.css`
2. Añade el `<link>` en el orden correcto en `index.html`
3. Usa las variables CSS definidas

### Reorganizar

El archivo `styles.css` antiguo ya no se usa. Si necesitas actualizar algo, edita el archivo CSS específico del componente.

## ✅ Ventajas de esta estructura

- ✅ **Modular** - Cada componente tiene su propio archivo
- ✅ **Mantenible** - Fácil encontrar y actualizar estilos
- ✅ **Escalable** - Perfecto para proyectos grandes
- ✅ **Reutilizable** - Classes consistentes
- ✅ **Optimizable** - Puedes eliminar CSS no usado
- ✅ **Colaborativo** - Múltiples desarrolladores pueden trabajar sin conflictos

## 📝 Notas

- Los archivos CSS pueden combinarse/minificarse en producción
- El orden de carga es importante para la cascada CSS
- Todas las variables están centralizadas en `variables.css`
- Los temas se manejan con atributos `data-theme`
