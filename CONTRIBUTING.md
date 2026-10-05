# Cómo trabajamos en los repositorios

Estas convenciones aplican a todos los repositorios de la organización, salvo que un repo tenga su propio `CONTRIBUTING.md`.

## Ramas

- `main` es la rama estable. **Nadie pushea directo a `main`.**
- Cada cambio se hace en una rama propia, creada desde `main`:
  - `feature/descripcion-corta` para funcionalidades nuevas
  - `fix/descripcion-corta` para correcciones
  - `docs/descripcion-corta` para documentación
- Nombres en minúscula y con guiones. Ejemplo: `feature/filtro-por-fecha`.

## Commits

Mensajes cortos y claros, en español, con un prefijo que indique el tipo de cambio:

| Prefijo | Uso | Ejemplo |
| --- | --- | --- |
| `feat:` | Funcionalidad nueva | `feat: agrega filtro por fecha al reporte` |
| `fix:` | Corrección de un error | `fix: corrige el cálculo del total mensual` |
| `docs:` | Documentación | `docs: agrega instrucciones de instalación` |
| `refactor:` | Cambio interno sin cambiar comportamiento | `refactor: separa la conexión a la base en un módulo` |
| `chore:` | Mantenimiento (dependencias, configuración) | `chore: actualiza dependencias` |

## Pull Requests

1. Al terminar el cambio, abrí un Pull Request contra `main`.
2. Completá la plantilla: qué cambia y cómo se probó.
3. Pedí revisión a al menos una persona que conozca el proyecto.
4. Se mergea solo cuando alguien lo aprobó.
5. Después del merge, borrá la rama.

## Credenciales y datos

- **Nunca** subir contraseñas, tokens, claves de API ni cadenas de conexión.
- Usar archivos de configuración local (por ejemplo `.env`) incluidos en el `.gitignore`, y dejar un `.env.example` sin valores reales.
- No subir datos reales de clientes ni exportaciones de bases de datos.
- Si subiste una credencial por error, avisá enseguida para rotarla: borrarla en un commit nuevo **no** la elimina del historial.

## Documentación

- **Técnica**: en cada repo, en el `README.md` y la carpeta `docs/`. Se actualiza en el mismo PR que cambia el código.
- **Funcional**: en el repositorio `documentacion-funcional`.
