# Instrucciones para el Agente de Traducción

## Objetivo

Traducir los artículos de [webgpufundamentals.org](https://webgpufundamentals.org/) del inglés al español.

## Archivos del proyecto de traducción

- **Este archivo (`AGENTS.md`)**: Instrucciones generales de traducción.
- **`.translation/glossary.md`**: Glosario de términos técnicos. Consultarlo SIEMPRE antes de traducir.
- **`.translation/translation_progress.md`**: Estado de progreso. Consultarlo para saber qué traducir y actualizarlo al terminar.

## Estructura de archivos

- **Originales en inglés**: `webgpu/lessons/*.md`
- **Traducciones al español**: `webgpu/lessons/es/*.md`
- **Configuración de idioma**: `webgpu/lessons/es/langinfo.hanson` (ya configurado)

Los archivos traducidos deben tener **exactamente el mismo nombre** que el original.

## Reglas de traducción

### SÍ se traduce

- El campo `Title:` del frontmatter
- El campo `Description:` del frontmatter
- El campo `TOC:` del frontmatter
- Todo el texto explicativo entre bloques de código
- Los comentarios en bloques de pseudocódigo que son parte de la explicación
- Las notas al pie (`[^nombre]`): el identificador NO se traduce, pero el contenido SÍ
- Los textos interactivos que ve el usuario (ej: "drag the vertices" → "arrastra los vértices")

### NO se traduce

- Código fuente (JavaScript, WGSL, HTML, CSS)
- Comentarios dentro del código JS/WGSL/HTML
- Nombres de API de WebGPU/WGSL (device, adapter, pipeline, bindGroup, etc.)
- URLs y **enlaces internos** (ej: `webgpu-textures.html`)
- Atributos HTML
- Directivas del sistema de build: `{{{example ...}}}`, `{{#escapehtml}}`, etc.
- Los valores de `label:` en el código (son identificadores técnicos)
- Los nombres de archivos en rutas

## Reglas Críticas de Integridad Estructural

El sistema de build (`lesson-builder`) es extremadamente estricto. El archivo en español debe ser un **espejo estructural** del inglés.

1.  **Paridad de Enlaces**: Los enlaces internos deben ser **idénticos** a los del archivo original.
    -   Si el original tiene una errata (ej: `[text](webpgu-textures.html)`), la traducción **DEBE** mantener esa misma errata. No intentes corregirla.
    -   Cualquier diferencia en el destino de un enlace provocará un error "Fatal error" en el build.
2.  **No añadir HTML/CSS extra**: No añadas etiquetas `<link>`, `<script>`, `<style>` o `<img>` que no existan en el original.
3.  **Mantenimiento de IDs**: Si el original tiene `<a id="some-id"></a>`, debe mantenerse exactamente igual.

### Terminología técnica

- **Términos de la API WebGPU/WGSL**: NO traducir (pipeline, buffer, bind group, render pass, compute pass, workgroup, sampler, adapter, device, uniform, storage, layout, entry point, canvas, mipmap)
- **Tipos de shaders**: Usar el término en inglés pero aclarar la primera vez que aparece en cada artículo. Ejemplo: "vertex shader (shader de vértices)"
- **Conceptos generales de gráficos**: Traducir con el término inglés entre paréntesis la primera vez. Ejemplo: "espacio de recorte (clip space)"
- **Consultar siempre `.translation/glossary.md`** para decisiones específicas

### Estilo

- Español neutro/internacional (sin regionalismos)
- Mantener el tono didáctico y cercano del original
- Usar "tú" (informal) para dirigirse al lector, como hace el original con "you"

## Flujo de trabajo por sesión

1. Leer `.translation/translation_progress.md` para identificar el siguiente archivo
2. Leer `.translation/glossary.md` para la terminología
3. Leer el archivo original en inglés completo
4. Traducir sección por sección, respetando toda la estructura markdown y HTML
5. Guardar en `webgpu/lessons/es/` con el mismo nombre
6. Actualizar `.translation/translation_progress.md` marcando el archivo como completado
7. Si aparecen términos nuevos que requieran decisión, añadirlos a `.translation/glossary.md`

## Referencia

- La traducción coreana (`webgpu/lessons/ko/`) es la más completa y sirve como modelo estructural
- El archivo `toc.hanson` en la raíz define el orden de los artículos
- Los archivos `.js` y `.css` asociados a las lecciones NO se traducen (son compartidos entre idiomas)
- Los enlaces internos como `(webgpu-textures.html)` NO se modifican (el sistema de build los resuelve por idioma)
