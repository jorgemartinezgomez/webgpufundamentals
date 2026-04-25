# Glosario de Traducción — WebGPU Fundamentals (EN → ES)

## Política general

1. Si el término es una API/función/tipo de WebGPU o WGSL → **NO traducir**
2. Si el término es un concepto general de gráficos → **traducir**, con el término en inglés entre paréntesis la primera vez que aparece en cada artículo
3. Si el término es un tipo de shader → usar el término en inglés y aclarar entre paréntesis la primera vez en cada artículo

## Términos que NO se traducen (se dejan en inglés)

| Término | Categoría |
|---------|-----------|
| shader | Universal en gráficos |
| buffer | Universal en programación |
| pipeline | API WebGPU |
| bind group | API WebGPU |
| render pass | API WebGPU |
| compute pass | API WebGPU |
| workgroup | API WGSL |
| sampler | API WebGPU |
| adapter | API WebGPU |
| device | API WebGPU |
| mipmap / mip level | Universal en gráficos |
| uniform | API WebGPU/WGSL |
| storage | API WebGPU/WGSL |
| entry point | Término técnico |
| layout | API WebGPU |
| canvas | API HTML |
| label | API WebGPU |
| array | Universal en programación |
| offset | Universal en programación |
| callback | Universal en programación |
| encoder | API WebGPU |

## Términos que SÍ se traducen

| Inglés | Español | Notas |
|--------|---------|-------|
| vertex shader | vertex shader (shader de vértices) | Aclarar entre paréntesis la 1ª vez por artículo |
| fragment shader | fragment shader (shader de fragmentos) | Aclarar entre paréntesis la 1ª vez por artículo |
| compute shader | compute shader (shader de cómputo) | Aclarar entre paréntesis la 1ª vez por artículo |
| texture | textura | Traducción directa |
| vertex / vertices | vértice / vértices | Traducción directa |
| fragment | fragmento | Cuando se refiere al concepto, no a la API |
| clip space | espacio de recorte (clip space) | Aclarar la 1ª vez |
| triangle | triángulo | |
| pixel | píxel | Con tilde |
| color | color | |
| floating point | punto flotante | |
| integer | entero | |
| unsigned | sin signo | |
| rasterize / rasterization | rasterizar / rasterización | |
| rendering / render | renderizado / renderizar | |
| draw / drawing | dibujar / dibujo | |
| command buffer | buffer de comandos | Mantener "buffer" |
| attribute | atributo | |
| parameter | parámetro | |
| return value | valor de retorno | |
| function | función | |
| iteration | iteración | |
| asynchronous | asíncrono/a | |
| best practice | buena práctica | |
| error message | mensaje de error | |
| clear value | valor de limpieza | |
| shading language | lenguaje de sombreado | |
| strongly typed | fuertemente tipado | |
| builtin | integrado / built-in | Mantener "builtin" si es nombre de API WGSL |
| internal state | estado interno | |
| resources | recursos | |
| depth | profundidad | En contexto 3D; "depth" si es parámetro de API |
| width / height | ancho / alto | |
| size | tamaño | |
| usage | uso | |
| flag | flag / bandera | Usar "flag" en contexto de programación |
| map / mapping (buffer) | mapear / mapeo | En contexto de acceso a buffers |
| submit | enviar / submit | Usar "enviar" en prosa, "submit" si es nombre de API |
| encode / encoding | codificar / codificación | |
| descriptor | descriptor | Se mantiene igual |
| attachment | attachment | En contexto de API (colorAttachment) |
| stage | etapa | |
| binding | binding | En contexto de API |
| location | location | En contexto de API |
| perspective projection | proyección en perspectiva | |
| orthographic projection | proyección ortográfica | |
| matrix / matrices | matriz / matrices | |
| projection matrix | matriz de proyección | |
| view matrix | matriz de vista | |
| camera matrix | matriz de cámara | |
| world matrix | matriz de mundo | |
| model matrix | matriz de modelo | |
| normal matrix | matriz normal | |
| scene graph | grafo de escena | |
| lighting | iluminación | |
| spotlight | foco / luz focal | |
| directional light | luz direccional | |
| point light | luz puntual | |
| specular | especular | |
| normal (vector) | normal | |
| cross product | producto cruzado | |
| dot product | producto escalar / producto punto | |
| field of view | campo de visión (field of view) | Aclarar la 1ª vez |
| aspect ratio | relación de aspecto | |
| z-buffer / depth buffer | z-buffer / buffer de profundidad | |
| face culling | face culling / descarte de caras | Aclarar la 1ª vez |
| winding order | orden de bobinado (winding order) | Aclarar la 1ª vez |
| mipmap / mip level | mipmap / nivel de mip | Se suele usar nivel de mip en prosa |
| texture view | vista de textura | |
| skybox | skybox | Mantener término en inglés |
| texel | téxel | Con tilde |
| bilinear filtering | filtrado bilineal (bilinear filtering) | Aclarar la 1ª vez |
| address mode | modo de direccionamiento (address mode) | |
