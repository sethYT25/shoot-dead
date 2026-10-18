# Shoot Dead

Prototipo de **shooter tactico CQB** estilo *Ready or Not*, jugable directamente en el navegador.

> Estado: **prototipo de mecanicas** (Fase 1). El objetivo no es el apartado visual, sino validar el *feel*: movimiento, ADS, disparo, recarga, puertas e IA basica.

## Como jugar

Sin instalacion, sin dependencias, sin internet:

1. Abre `index.html` en tu navegador (doble clic).
2. Pulsa **Jugar**.
3. El navegador pedira bloquear el puntero — acepta para controlar la camara.

### Controles

| Accion | Tecla |
|---|---|
| Mover | `W` `A` `S` `D` |
| Mirar | Raton |
| Disparar | Clic izquierdo |
| Apuntar (ADS) | Clic derecho |
| Recargar | `R` |
| Agacharse | `Ctrl` o `C` |
| Correr | `Shift` |
| Saltar | `Espacio` |
| Abrir / cerrar puerta | `E` |
| Pausa | `Esc` |

## Mecanicas incluidas (Fase 1)

- Movimiento FPS con aceleracion, *sprint*, agacharse y salto.
- Camara FPS con ADS (zoom y reduccion de dispersion).
- Disparo por *raycast* con dispersion, retroceso vertical y recarga con cadencia.
- Nivel CQB: pasillo, pasillos laterales, cajas de cobertura y puertas operables.
- IA de enemigos: rondas de patrulla por waypoints, deteccion por linea de vision y cono de vision, reaccion y disparo.
- Vida, dano, muerte y respawn.
- HUD: vida, municion, estado del arma, bajas y minimapa.
- Colisiones con paredes, cajas y puertas.

## Estructura

```
shoot-dead/
├─ index.html   # Prototipo completo y jugable (un solo archivo)
├─ README.md
└─ .gitignore
```

En la Fase 2 (si el prototipo convence) se migra a una estructura modular:

```
src/
├─ core/     # loop, input, estado
├─ player/   # movimiento, camara, ADS
├─ weapons/  # stats, recarga, balistica
├─ ai/       # sospechosos, patrullas, reaccion
├─ world/    # nivel, puertas, cobertura
└─ ui/       # HUD, comandos de escuadron
```

## Roadmap

### Fase 1 — Nucleo tactico (actual)
- [x] Movimiento, ADS, disparo, recarga
- [x] Nivel CQB con puertas
- [x] IA basica de enemigos
- [ ] Ajustar el *feel* con tu feedback

### Fase 2 — Profundidad de mecanicas
- [ ] Granadas y humo
- [ ] Comandos de escuadron
- [ ] Modo *flashbang* y vision reducida
- [ ] Objetivos (rescatar rehenes, asegurar zona)
- [ ] Sistema de puntuacion tactico (uso de fuerza)
- [ ] Migracion a estructura modular + Vite

### Fase 3 — El salto real
- [ ] Portar el diseno a **Unreal 5** (o Godot 4)
- [ ] Graficos, animaciones y audio reales
- [ ] Niveles disenados a mano
- [ ] Multijugador cooperativo

## Nota sobre el alcance

Un *tactical shooter* tipo *Ready or Not* es un proyecto de equipo y de anos. Este repositorio es el **nucleo de mecanicas** que sirve de base y de prueba de diseno. Todo el software usado es libre y gratuito.

## Licencia

MIT
