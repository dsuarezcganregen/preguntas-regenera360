# Preguntas Regenera360

Página para que los alumnos de cada clase de Regenera360 dejen sus preguntas y voten por las que comparten.

- **Alumnos:** `https://dsuarezcganregen.github.io/preguntas-regenera360/?c=<clase>`
- **Administración:** `https://dsuarezcganregen.github.io/preguntas-regenera360/admin.html`

Cómo funciona:

- Cada clase tiene su enlace, fecha de apertura y fecha de cierre. Antes de abrir, el enlace muestra cuándo abre; después de cerrar, queda en solo lectura.
- Los alumnos ponen nombre y pregunta, sin crear cuenta. El voto se cuenta uno por pregunta por navegador.
- Solo daniel@ganaderiaregenerativa.com entra a la administración: crea clases, marca preguntas como respondidas, borra y descarga en CSV.
- Los datos viven en Supabase (proyecto "Preguntas Regenera360"). La clave en `config.js` es la pública y solo permite lo que las reglas de la base dejan.
- `.github/workflows/mantener-activo.yml` consulta la base dos veces al día para que Supabase no pause el proyecto.
