# Shoot Dead

Prototipo de **shooter tactico CQB** estilo *Ready or Not*, jugable directamente en el navegador.

> Estado: **prototipo de mecanicas** (Fase 1). El objetivo no es el apartado visual, sino validar el *feel*: movimiento, ADS, disparo, recarga, puertas e IA basica.

## Como jugar

Sin instalacion y sin dependencias. Solo necesitas conexion a internet la primera vez (Three.js se carga desde CDN).

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
- Disparo por *raycast* con dispersion, retroceso y recarga con cadencia.
- **Hitboxes de capsula vertical** por enemigo (cuerpo de pies a hombros, cabeza aparte) con multiplicador de dano x2.6 en tiros a la cabeza.
- Trazadoras visibles y marcas de impacto (rojas sobre enemigo, blancas sobre geometria).
- Nivel CQB: pasillo, pasillos laterales, cajas de cobertura y puertas operables.
- IA de enemigos con **linea de vision real** (oclusion por paredes), cono de vision, maquina de estados `patrol -> alert -> combat`, ronda de waypoints, orbita a distancia de combate y fuego.
- Vida, dano, muerte y respawn. Agacharse reduce la probabilidad de ser alcanzado.
- HUD: vida, municion, estado del arma, hostiles restantes, bajas y minimapa con cono de vision.
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
- [x] Hitboxes correctos y dano a la cabeza
- [ ] Ajustar el *feel* con feedback de juego

### Fase 2 — Profundidad de mecanicas
- [ ] Granadas y humo
- [ ] Comandos de escuadron
- [ ] Modo *flashbang* y vision reducida
- [ ] Objetivos (rescatar rehenes, asegurar zona)
- [ ] Sistema de puntuacion tactico (uso de fuerza)
- [ ] Sonido (disparos, pasos, reacciones)
- [ ] IA que use cobertura y coordine entre enemigos
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
