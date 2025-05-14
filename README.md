# Pruebas-Unitarias
Pruebas-Unitarias Tarea

## Identificación de métodos


| **Método**                  | **Parámetros de Entrada**                                  | **Resultado/Efecto en Repositorio**                                                                 |
|-----------------------------|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `crearTarea`                | `descripcion: String`, `etiquetas: List<String> = emptyList()` | Agrega nueva `Tarea` al repositorio (`repositorio.agregar()`).                                      |
| `asignarTarea`              | `tareaId: Long`, `usuarioId: Int`                          | Actualiza la tarea con el usuario asignado (modifica entidad en repositorio).                       |
| `obtenerHistorialTarea`     | `tareaId: Long`                                            | **Solo lectura**: Retorna historial (no modifica repositorio).                                      |
| `filtrarPorTipo`            | `tipo: String`                                             | **Consulta repositorio**: Retorna actividades del tipo especificado (sin modificaciones).           |
| `filtrarPorEstado`          | `estado: Estado`                                           | **Consulta repositorio**: Retorna tareas en ese estado (sin modificaciones).                        |
| `filtrarPorEtiqueta`        | `etiqueta: String`                                         | **Consulta repositorio**: Retorna actividades con la etiqueta (sin modificaciones).                 |
| `filtrarPorUsuario`         | `usuarioId: Int`                                           | **Consulta repositorio**: Retorna tareas asignadas al usuario (sin modificaciones).                  |
| `filtrarPorFecha`           | `fecha: String` (ej: "hoy")                                | **Consulta repositorio**: Retorna eventos de la fecha especificada (sin modificaciones).             |
| `crearEvento`               | `descripcion: String`, `fecha: String`, `ubicacion: String`| Agrega nuevo `Evento` al repositorio (`repositorio.agregar()`).                                      |
| `listarActividades`         | *(Ninguno)*                                                | **Consulta repositorio**: Retorna lista completa de actividades (sin modificaciones).                |
| `crearSubtarea`             | `parentId: Long`, `descripcion: String`                    | Agrega subtarea al repositorio y actualiza tarea padre (`repositorio.agregar()` + actualización).    |
| `cambiarEstadoTarea`        | `tareaId: Long`, `opcionElegida: Int` (1-3)                | Actualiza estado de la tarea en repositorio (modifica entidad).                                     |
| `obtenerResumenTareas`      | *(Ninguno)*                                                | **Consulta repositorio**: Retorna estadísticas de tareas (sin modificaciones).                       |
| `obtenerEventosProgramados` | *(Ninguno)*                                                | **Consulta repositorio**: Retorna conteo de eventos por fecha (sin modificaciones).                  |
| `crearUsuario`              | `nombre: String`, `email: String`                          | Agrega nuevo `Usuario` a `userRepository` (`userRepository.agregar()`).                             |
| `listarUsuarios`            | *(Ninguno)*                                                | **Consulta userRepository**: Retorna lista de usuarios (sin modificaciones).                         |
| `buscarActividad`           | `id: Long`                                                 | **Consulta repositorio**: Retorna actividad por ID o `null` (sin modificaciones).                    |

