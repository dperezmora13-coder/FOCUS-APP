# FOCUS — Hipertrofia Mental 🧠

Una app web progresiva para trackear tu progreso académico como si fuera entrenamiento en el gym.

## Características

- **Pomodoro** integrado con modos de enfoque, descanso corto y descanso largo
- **Materias con barras de progreso** — cada unidad que apruebas sube tu nivel, cada reprobada lo baja
- **Racha diaria verificada con foto** — sube una foto de tu libreta para mantener la racha activa
- **Bottom sheet de racha** al estilo Apple (como la imagen de Healthy Habits)
- **Logros desbloqueables** conforme avanzas
- **Alertas de prioridad** — te avisa qué materia está en zona crítica
- **Diseño dark Apple** — fondo negro, SF Pro, transiciones fluidas
- **Base de datos local** — todo se guarda en localStorage, sin necesidad de backend

## Materias configuradas

| Materia | Unidades | Estado |
|---|---|---|
| Matemáticas Discretas | 6 | U1, U2 reprobadas |
| Programación | 5 | U1, U2, U3 reprobadas |
| Cálculo | 5 | U1, U2, U3 reprobadas |
| Probabilidad y Estadística | 5 | Sin datos |
| Química | 5 | Sin datos |
| Investigación | 4 | Sin datos |
| Contabilidad | 4 | Sin datos |

## Cómo subir a GitHub Pages

```bash
# 1. Crea un nuevo repo en github.com/new
# 2. Clona el repo
git clone https://github.com/TU_USUARIO/focus-app.git

# 3. Copia el archivo index.html al repo
cp index.html focus-app/

# 4. Sube los cambios
cd focus-app
git add .
git commit -m "Initial FOCUS app"
git push origin main

# 5. Ve a Settings > Pages > Source: main branch / root
# Tu app estará en: https://TU_USUARIO.github.io/focus-app
```

## Agregar al iPhone como PWA

1. Abre la app en Safari
2. Toca el botón de compartir (⬆)
3. Selecciona "Agregar a la pantalla de inicio"
4. Se instala como app nativa con ícono propio

## Tecnologías

- HTML5 / CSS3 / JavaScript vanilla
- localStorage para persistencia de datos
- PWA-ready (sin service worker externo requerido)
- Compatible con iPhone Safari / Chrome / Firefox

## Estructura del sistema de puntos

- Cada unidad aprobada: **+20 puntos**
- Cada unidad reprobada: **-40 puntos de porcentaje proporcional**
- Score máximo: **100 pts**
- Zona verde: 60+, Zona naranja: 30-59, Zona roja: 0-29
