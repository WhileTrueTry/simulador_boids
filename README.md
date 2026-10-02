# Simulador 3D de modelos boids (Bandadas emergentes)

Simulación interactiva de una bandada de aves como sistema complejo: cada ave aplica reglas **locales**
(separación, alineación, cohesión) y la bandada emerge sin líder ni centro de masa global.

**Probalo en línea:** https://WhileTrueTry.github.io/simulador_boids/

## Qué incluye

- `index.html` — Simulador 3D: WebGL2 con respaldo a Canvas 2D, un único archivo sin dependencias.
- `simulador_boids_2d.html` — Versión 2D original.

Ambos se abren directamente en Edge, Chrome o Firefox; no hace falta servidor ni conexión a internet.
La única información que se guarda en el navegador es el tema (claro/oscuro).

## Modelos implementados

- Reglas de Reynolds (1987) con formulación de *steering* acotado.
- Vecindad métrica (radio) o topológica (k vecinos más cercanos), según Ballerini et al. (2008).
- Zonas de repulsión / orientación / atracción de Couzin et al. (2002), con métricas de polarización (φ) y momento angular (m).
- Individuos informados como «líderes» (Couzin, Krause, Franks y Levin, 2005).
- Ruido angular y transición orden–desorden (Vicsek et al., 1995).
- Dormidero, velocidad de crucero y alabeo inspirados en StarDisplay (Hildenbrandt, Carere y Hemelrijk, 2010).
- Halcón autónomo con ataques periódicos (Storms, Carere, Zoratto y Hemelrijk, 2019).

## Controles

| Acción | Cómo |
|---|---|
| Orbitar la cámara | arrastrar |
| Acercar / alejar | rueda del mouse |
| Desplazar | Shift + arrastrar o botón derecho |
| Pausar / un paso / reiniciar | Espacio / N / R |
| Reset de cámara / rotación automática | C / O |
| Depredador fijo | clic corto con el rol del cursor en «Depredador» |

Los parámetros se ajustan en vivo desde el panel lateral; se pueden exportar e importar como JSON.
Once *presets* ilustran fenómenos de la literatura (fragmentación en mundos grandes, fases de Couzin, migración guiada, transición de fase, ataque de halcón).

## Referencias principales

- Reynolds, C. W. (1987). Flocks, herds, and schools: A distributed behavioral model. *Computer Graphics*, 21(4), 25–34.
- Vicsek, T. et al. (1995). Novel type of phase transition in a system of self-driven particles. *Physical Review Letters*, 75(6), 1226–1229.
- Couzin, I. D. et al. (2002). Collective memory and spatial sorting in animal groups. *Journal of Theoretical Biology*, 218(1), 1–11.
- Couzin, I. D. et al. (2005). Effective leadership and decision-making in animal groups on the move. *Nature*, 433, 513–516.
- Ballerini, M. et al. (2008). Interaction ruling animal collective behavior depends on topological rather than metric distance. *PNAS*, 105(4), 1232–1237.
- Hildenbrandt, H., Carere, C. & Hemelrijk, C. K. (2010). Self-organized aerial displays of thousands of starlings: a model. *Behavioral Ecology*, 21(6), 1349–1359.
- Storms, R. F. et al. (2019). Complex patterns of collective escape in starling flocks under predation. *Behavioral Ecology and Sociobiology*, 73, 10.

## Licencia

Código bajo licencia MIT (ver `LICENSE`).
