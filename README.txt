WebAR project (MindAR + A-Frame) - VENADO

Contenido:
- index.html                # Página principal (usa MindAR + A-Frame)
- VENADO_DEFINITIVO.glb     # Tu modelo 3D (copiado)
- targets.mind              # NO incluido: archivo de target que debes generar
                            #   (explicado abajo)

Objetivo:
Al apuntar con la cámara a la imagen target (la foto del venado que me enviaste),
aparecerá el modelo 3D 'VENADO_DEFINITIVO.glb' centrado sobre la imagen.

Pasos para generar el archivo 'targets.mind' (necesario):
========================================================
MindAR usa un archivo binario (.mind) que contiene la información del target
listo para que el navegador haga image-tracking. Para generar ese archivo
podés elegir cualquiera de estas opciones:

1) Usar la utilidad de línea de comandos de MindAR (recomendado para desarrolladores):
   - Necesitás Node.js y npm instalados.
   - Instalar la herramienta (ejemplo):
       npm install -g @zackiri/mindar-cli
     (el paquete exacto puede variar; si no funciona, buscá 'mindar cli' o 'mindar image train')
   - Generar el target desde la imagen (ejemplo):
       mindar-image-train --input target-image.jpg --output targets.mind
     (ajustá nombres según la herramienta que instales)
   - Copiá el 'targets.mind' generado a la carpeta del proyecto (junto a index.html).

2) Usar el servicio web oficial / herramienta online de MindAR (si está disponible):
   - Subís la imagen, el servicio devuelve el archivo .mind que podés descargar.
   - Subís / colocás 'targets.mind' en la misma carpeta que index.html.

3) Si preferís no usar MindAR:
   - Alternativas: AR.js (pattern markers) o WebXR Image Tracking. Tené en cuenta que
     la creación del archivo de target (patt / mind / NFT) siempre necesitará un paso
     de preprocesado con la herramienta correspondiente.

Notas importantes:
- Asegurate que la imagen original (target) esté impresa en buena calidad. Las imágenes
  con buena textura y contraste funcionan mejor.
- Ajustá la escala en index.html (atributo scale del <a-gltf-model>) para que el venado
  quede con la altura deseada sobre la imagen.
- Para probar localmente en móvil podés usar un hosting simple (GitHub Pages, Netlify, surge.sh).
  Si subís el contenido a GitHub Pages, la URL será algo como:
    https://<tu_usuario>.github.io/<repo>/
  Después generás un QR que apunte a esa URL.

Cómo probar:
1) Generá o obtené 'targets.mind' y ponelo en la carpeta del proyecto.
2) Subí toda la carpeta a un hosting estático (GitHub Pages, Netlify, Vercel, surge).
3) Abrí la URL con el móvil y permití acceso a la cámara.
4) Apuntá al target impreso y el modelo debería aparecer centrado.

Si querés, yo puedo:
- Ayudarte a generar el archivo 'targets.mind' si me permitís usar una herramienta online (yo te guío paso a paso),
- O bien, si preferís, puedo darte comandos precisos y enlaces para generar el archivo en tu máquina,
- También puedo subir el proyecto a GitHub Pages por vos (si me das permisos o un repo) o guiarte en hacerlo.

-- Fin del README --
