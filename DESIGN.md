# Ancla Web — sistema visual

## Mundo
Carta náutica de noche: isolíneas de profundidad doradas sobre azul abisal. El ancla queda "fondeada" en la carta, con ondas de sonar. Elegante, poco texto, cada sección con un solo mensaje.

## Color
| Token | Valor | Uso |
|---|---|---|
| `--abyss` | `#08142a` | Fondo del inicio, trabajos y cierre |
| `--navy` | `#0b1a2e` | Fondo base |
| `--tide` / `--rise` | `#11243f` / `#16304f` | Superficies elevadas, scrollbar |
| `--gold` | `#e1b868` | Único acento: títulos en cursiva, botón principal, isolíneas, íconos |
| `--gold-hi` | `#f1d49a` | Hover del botón dorado |
| `--fog` | `#eef0f3` | Texto principal |
| `--mist` | `rgba(238,240,243,.66)` | Texto secundario |
| `--gold-line` / `--faint` | líneas de 1px | Separadores |

## Tipografía
- **Instrument Serif** (normal y cursiva): titulares. La palabra clave de cada título va en cursiva dorada.
- **Geist**: textos, botones y navegación.
- **Geist Mono**: solo para coordenadas y el número de teléfono (dato medido).

## Componentes
- Botón principal dorado tipo píldora (56px); secundario solo con contorno. `:active` escala a 0.97.
- Servicios como lista con líneas finas (no tarjetas); el ícono se redibuja al pasar el mouse.
- Trabajos: captura en "pantalla" + celular superpuesto; ambas se recorren solas (`pan`), aparecen con `clip-path`.
- Ruta del proceso: línea punteada dorada con paradas.

## Movimiento
- Curvas: `--ease-out: cubic-bezier(.23,1,.32,1)` para entradas; `--ease-io: cubic-bezier(.77,0,.175,1)` para desplazamientos.
- Momento firma: isolíneas en canvas que reaccionan al puntero en el inicio, ancla que baja y sonar.
- Pantalla de carga: el ancla se dibuja, aparece "Ancla web" y la cortina sube.
- `prefers-reduced-motion`: sin carga, sin recorridos, canvas estático.
