# Preguntas Regenera360

Página para que los alumnos de cada clase de Regenera360 dejen sus preguntas y voten por las que comparten.

- **Alumnos:** `https://dsuarezcganregen.github.io/preguntas-regenera360/?c=<clase>`
- **Administración:** `https://dsuarezcganregen.github.io/preguntas-regenera360/admin.html`
- **Pantalla para Zoom:** `https://dsuarezcganregen.github.io/preguntas-regenera360/sesion.html?c=<clase>` (se abre desde la administración)

## Cómo funciona

- Cada clase tiene su enlace, fecha de apertura y fecha de cierre. Antes de abrir, el enlace muestra cuándo abre; después de cerrar, queda en solo lectura.
- Los alumnos ponen nombre y pregunta, sin crear cuenta. El voto se cuenta uno por pregunta por navegador.
- Solo daniel@ganaderiaregenerativa.com entra a la administración: crea, archiva y borra clases, marca preguntas como respondidas, marca las que no son del tema, las manda a otra clase, junta las repetidas y descarga en CSV.
- Las preguntas fuera de tema van a la bandeja "Preguntas por ubicar" hasta que se elige su clase. Llegan con sus votos y el alumno ve de dónde venían.
- Cada clase muestra arriba el resumen de su sesión (las clases que cierran a la misma hora son una sola sesión), con orden sugerido por tema y botón para compartirlo por WhatsApp.
- La pantalla para Zoom muestra una pregunta a la vez, juntando todas las clases de la sesión, de la más votada a la menos votada, sin las fuera de tema ni las repetidas.

## Tareas automáticas

- **Resumen antes de la sesión** (tarea programada de Claude, todos los días a las 12:05 hora de México): cuando una clase acaba de cerrar, agrupa sus preguntas por tema, sugiere repetidas y fuera de tema (Daniel confirma en la administración), te avisa al teléfono y guarda las preguntas en el "REGENERA360 — Banco de preguntas". Después de la sesión pone al día el banco con las respondidas.
- **Mantener Supabase activo** (`.github/workflows/mantener-activo.yml`): consulta la base dos veces al día para que Supabase no pause el proyecto, y deja una nota mensual para que GitHub no apague la tarea.

## Dónde viven los datos

Supabase, proyecto "Preguntas Regenera360". La clave en `config.js` es la pública y solo permite lo que las reglas de la base dejan.
