# Auto-party: datos de dos cuentas

## Qué es esto

Aquí hay datos del auto-party de dos cuentas, CUENTA_A y CUENTA_B, del 2026-10-10 al 2026-10-24. Los nombres de las cuentas y de los demás jugadores están anonimizados (CUENTA_A, CUENTA_B, J001, J002…). Las fechas y horas son las originales, en hora local del PC.

## Qué hace el auto-party, visto desde fuera

Invita a grupo a los jugadores que se acercan al punto de farmeo y los saca del grupo cuando se alejan. Nada más.

## Cifras

Todas las cifras se calculan a partir de `datos/eventos_party.csv`. «Invitaciones» cuenta los eventos `invitacion` (incluidos los reintentos).

### Eventos por tipo y cuenta

| Tipo | CUENTA_A | CUENTA_B | Total |
|---|---:|---:|---:|
| `acepta_cuenta_propia` | 10 | 62 | 72 |
| `expulsion` | 244 | 124 | 368 |
| `inicio_sesion` | 266 | 158 | 424 |
| `invitacion` | 1071 | 443 | 1514 |
| `invitacion_cuenta_propia` | 151 | 8 | 159 |
| `rechaza_invitacion` | 18 | 8 | 26 |
| `salida_grupo` | 29 | 13 | 42 |

### Invitaciones por hora del día

| Hora | CUENTA_A | CUENTA_B | Total |
|---|---:|---:|---:|
| 00 | 4 | 39 | 43 |
| 01 | 0 | 31 | 31 |
| 02 | 0 | 23 | 23 |
| 03 | 0 | 26 | 26 |
| 04 | 0 | 0 | 0 |
| 05 | 0 | 0 | 0 |
| 06 | 0 | 0 | 0 |
| 07 | 0 | 0 | 0 |
| 08 | 0 | 1 | 1 |
| 09 | 12 | 6 | 18 |
| 10 | 47 | 10 | 57 |
| 11 | 62 | 5 | 67 |
| 12 | 140 | 1 | 141 |
| 13 | 122 | 3 | 125 |
| 14 | 61 | 8 | 69 |
| 15 | 126 | 1 | 127 |
| 16 | 86 | 0 | 86 |
| 17 | 18 | 0 | 18 |
| 18 | 61 | 27 | 88 |
| 19 | 73 | 49 | 122 |
| 20 | 104 | 68 | 172 |
| 21 | 48 | 34 | 82 |
| 22 | 71 | 58 | 129 |
| 23 | 36 | 53 | 89 |

### Intervalo entre invitaciones consecutivas de la misma cuenta

Se muestran todos los intervalos y, aparte, solo los de hasta 10 minutos (para dejar fuera las pausas largas entre sesiones).

| Cuenta | Intervalos | n | Mín | p10 | Mediana | p90 |
|---|---|---:|---:|---:|---:|---:|
| CUENTA_A | todos | 1070 | 0.0 s | 2.0 s | 32.5 s | 5.8 min |
| CUENTA_A | ≤ 10 min | 1010 | 0.0 s | 2.0 s | 28.0 s | 3.8 min |
| CUENTA_B | todos | 442 | 0.0 s | 11.1 s | 52.5 s | 8.7 min |
| CUENTA_B | ≤ 10 min | 405 | 0.0 s | 11.0 s | 41.0 s | 4.6 min |

### Tiempo entre el 1.er y el 2.º intento al mismo jugador

| Cuenta | n | Mediana | Rango |
|---|---:|---:|---|
| CUENTA_A | 201 | 60.0 s | 14.0 s a 9.8 min |
| CUENTA_B | 107 | 61.0 s | 14.0 s a 9.8 min |

### Tiempo entre invitar a un jugador y sacarlo del grupo

Se vincula cada expulsión con la última invitación al mismo jugador de la misma cuenta, con un máximo de 24 horas de diferencia. Las expulsiones sin invitación previa en los datos (o a más de 24 horas) quedan fuera del cálculo.

| Cuenta | Con invitación previa | Sin invitación previa | Mediana | p90 |
|---|---:|---:|---:|---:|
| CUENTA_A | 241 | 3 | 60.0 s | 2.8 min |
| CUENTA_B | 121 | 3 | 46.0 s | 2.2 min |

### Jugadores distintos invitados

Por día: número de jugadores distintos invitados en cada día con actividad. Por jugador: cuántas veces se invita al mismo jugador (cuenta los primeros intentos, no los reintentos).

| Cuenta | Días con invitaciones | Distintos por día (mín / media / máx) | Jugadores | Veces por jugador (media / máx) |
|---|---:|---|---:|---|
| CUENTA_A | 12 | 6 / 43.2 / 119 | 408 | 2.1 / 25 |
| CUENTA_B | 7 | 1 / 30.3 / 99 | 182 | 1.8 / 19 |

### Horas entre el primer y el último evento

Primera y última hora con algún evento en el día (`datos/resumen_diario.csv`).

| Fecha | Cuenta | Primera | Última | Horas entre ambas |
|---|---|---|---|---:|
| 2026-10-10 | CUENTA_A | 12:18:13 | 20:28:06 | 8.2 |
| 2026-10-11 | CUENTA_A | 12:40:45 | 23:17:48 | 10.6 |
| 2026-10-12 | CUENTA_A | 10:12:32 | 21:31:50 | 11.3 |
| 2026-10-13 | CUENTA_A | 17:52:29 | 22:53:27 | 5.0 |
| 2026-10-14 | CUENTA_A | 09:41:02 | 21:36:52 | 11.9 |
| 2026-10-15 | CUENTA_A | 07:18:42 | 20:58:27 | 13.7 |
| 2026-10-16 | CUENTA_B | 20:26:40 | 23:58:19 | 3.5 |
| 2026-10-17 | CUENTA_A | 20:22:37 | 23:56:25 | 3.6 |
| 2026-10-17 | CUENTA_B | 00:01:38 | 23:55:35 | 23.9 |
| 2026-10-18 | CUENTA_A | 00:03:07 | 22:34:06 | 22.5 |
| 2026-10-18 | CUENTA_B | 00:03:16 | 22:32:06 | 22.5 |
| 2026-10-19 | CUENTA_A | 09:58:32 | 12:16:48 | 2.3 |
| 2026-10-19 | CUENTA_B | 09:57:56 | 20:50:04 | 10.9 |
| 2026-10-20 | CUENTA_A | 18:29:30 | 20:57:29 | 2.5 |
| 2026-10-20 | CUENTA_B | 17:26:01 | 20:47:09 | 3.4 |
| 2026-10-22 | CUENTA_A | 13:44:31 | 20:02:02 | 6.3 |
| 2026-10-22 | CUENTA_B | 13:43:30 | 13:43:30 | 0.0 |
| 2026-10-23 | CUENTA_A | 12:58:15 | 18:07:04 | 5.1 |
| 2026-10-23 | CUENTA_B | 13:10:55 | 21:01:10 | 7.8 |
| 2026-10-24 | CUENTA_A | 09:10:42 | 12:47:59 | 3.6 |
| 2026-10-24 | CUENTA_B | 09:10:50 | 12:55:46 | 3.7 |

## Diccionario de datos

### `datos/eventos_party.csv`

| Columna | Contenido |
|---|---|
| `fecha_hora` | Fecha y hora local del PC (`AAAA-MM-DD HH:MM:SS`). |
| `cuenta` | `CUENTA_A` o `CUENTA_B`. |
| `tipo` | Tipo de evento (tabla siguiente). |
| `objetivo` | Jugador al que se refiere el evento, anonimizado (`J001`…) o `CUENTA_x`. Vacío si no aplica. |
| `motivo` | Dato extra según el tipo. Vacío si no aplica. |

| Tipo | Significado | `motivo` |
|---|---|---|
| `invitacion` | Invitación a un jugador. | `intento=N` (1 es la primera vez, 2 o más son reintentos) |
| `invitacion_cuenta_propia` | Invitación a la otra cuenta del conjunto. | vacío (o `intento=N`) |
| `acepta_cuenta_propia` | Se acepta la invitación de la otra cuenta. | vacío |
| `rechaza_invitacion` | Se rechaza una invitación de otro grupo. | vacío |
| `expulsion` | Se saca a un jugador del grupo. | `salio_area`, `lejos_spot` u `otro` |
| `salida_grupo` | La cuenta sale del grupo de otro jugador. | vacío |
| `inicio_sesion` | Se registra el arranque del auto-party. | vacío |

### `datos/resumen_diario.csv`

Una fila por día y cuenta con eventos.

| Columna | Contenido |
|---|---|
| `fecha`, `cuenta` | Día y cuenta. |
| `invitaciones` | Eventos `invitacion` (con reintentos). |
| `reintentos` | De las invitaciones, las que tienen `intento` 2 o mayor. |
| `expulsiones_salio_area`, `expulsiones_lejos_spot`, `expulsiones_otro` | Expulsiones por motivo. |
| `jugadores_distintos_invitados` | Jugadores distintos entre las invitaciones del día. |
| `primera_hora`, `ultima_hora` | Hora del primer y del último evento del día. |

## Limitaciones

- Solo están los eventos que el programa registró en sus propios archivos de registro; puede haber hechos que no quedaron anotados.
- Las horas son las del reloj local del PC.
- No se incluyen eventos de las otras funciones del programa, solo los del auto-party.
- Los registros de las dos cuentas pueden solaparse; los eventos repetidos se han unificado (misma cuenta, misma hora, mismo tipo y mismo jugador).
- Tras cada arranque del programa (`inicio_sesion`) se vuelve a invitar a los jugadores cercanos, lo que sube las repeticiones por jugador.
- Los intervalos de tiempo se calculan entre eventos registrados y pueden incluir pausas del propio registro.
