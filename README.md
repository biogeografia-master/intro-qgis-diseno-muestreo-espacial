Práctica de desarrollo 5. PD05. Introducción a QGIS, diseño de muestreo
espacial estratificado<small><br>Biogeografía (GEO-131)<br>Universidad
Autónoma de Santo Domingo (UASD)<br>Semestre 2024-02</small>
================
El Tali
2024-11-12

<!-- README.md se genera a partir de README.Rmd. Por favor, edita ese archivo. -->

Versión HTML (quizá más legible),
[aquí](https://biogeografia-master.github.io/intro-qgis-diseno-muestreo-espacial/README.html)

# Fecha/hora de entrega

**26 de noviembre de 2024, 11:59 pm.**

# Objetivos

- Instalar el software QGIS y algunos de sus complementos esenciales
  para trabajos en biogeografía.

- Realizar, con el software QGIS, un diseño de muestreo espacial
  estratificado usando coberturas del suelo.

# Mandato global

1.  **Acepta la asignación, genera tu repositorio personalizado y
    clónalo en tu cuenta del servidor RStudio**. Este paso sigue el
    procedimiento estándar que aprendiste en PD anteriores. De todas
    formas, te lo refresco de forma resumida. Primero ve al [portal de
    la asignatura](https://github.com/biogeografia-202402), haz clic en
    el enlace de la PD04 y acepta la asignación. Se creará un
    repositorio personalizado en la [organización
    biogeografia-202402](https://github.com/biogeografia-202402). El
    nombre de tu repo personalizado normalmente será algo tal que: “base
    del repo” + “tu nombre de usuario de GitHub” (como sufijo). Clona tu
    repositorio personalizado en el servidor RStudio. Para ello, deberás
    acceder al servidor con tus credenciales, copiar la ruta en GitHub
    de tu repo personalizado (botón verde `Code` en GitHub) y realizar
    el procedimiento estándar de nuevo proyecto con control de versiones
    en RStudio.

2.  Realiza los ejercicios y ve colocando los entregables de cada
    ejercicio, en el cuaderno RMarkdown
    `entregables-intro-qgis-diseno-muestreo-espacial-estratificado.Rmd`,
    el cual está vacío y funciona como una plantilla. Cada ejercicio
    dispone de un título de nivel 1 (“\#”) en el referido documento.
    Cuando se te pida entregar capturas de pantalla, las deberás subir a
    tu clon del repo en el servidor RStudio e insertarlas (como ya
    sabes), en la referida plantilla. A partir de la plantilla,
    generarás un PDF que tejeras usando RStudio. Deberás usar estilos de
    formato (los títulos debidamente escritos, el texto normal también,
    siguiendo lo aprendido en las PD anteriores), referencias
    bibliográficas, referencias cruzadas a figuras y tablas (es decir,
    necesitarás que las figuras y tablas tengan título o “*caption*”).
    Nota que usarás un cuaderno RMarkdown ligeramente parecido al que
    has usado en otras PD, sólo que en este caso no será un manuscrito.
    Entregarás, como suele ser habitual en las PD, tu repo con los
    cambios empujados (`commit>push`) a GitHub, donde aparecerán tanto
    tu cuaderno RMarkdown, como tu PDF debidamente tejido.

3.  Específicamente para el ejercicio 5, reproduce el vídeo de apoyo
    (los ejercicios 1 al 4 no tienen grandes complicaciones, así que
    realízalos leyendo directamente las instrucciones incluidas). El
    enlace del vídeo de apoyo exclusivo para dicho ejercicio, lo
    encontrarás en el [portal de la
    asignatura](https://github.com/biogeografia-202402), al lado del
    nombre de esta asignación (“PD05”). El vídeo explica cómo realizar
    los pasos necesarios para el diseño de muestreo espacial
    estratificado, y algunos detalles sobre el tipo de muestreo y la
    fuente ráster usada.

4.  **IMPORTANTE**. Anuncia tus elecciones en el foro (familia de GBIF
    para el ejercicio 4, capa vectorial del ejercicio 5); si alguna
    opción ya está elegida, deberás elegir otra. En el caso del
    ejercicio 5, reserva “estudiante-01.kml” para mí.

# Ejercicios

## Ejercicio 1. Instalación de QGIS

**Resumen:** En este primer paso, aprenderás a descargar e instalar QGIS
en tu computadora.

1.  Dirígete al sitio oficial de QGIS en <https://qgis.org/>.
2.  Elige la versión de tu sistema operativo y descarga el instalador.
3.  Ejecuta el instalador y sigue las instrucciones en pantalla hasta
    finalizar la instalación.
4.  Abre QGIS para comprobar que se ha instalado correctamente.

**Entrega:** Párrafo resumen del proceso realizado y captura de pantalla
del programa QGIS abierto en tu computadora. *Caption* sugerido para la
imagen (puedes usar uno escrito por ti): “Captura de QGIS después de la
instalación.”

## Ejercicio 2. Instalación del complemento QuickMapServices

**Resumen:** En este paso, aprenderás a instalar un complemento que te
permitirá cargar mapas base como Google Maps o OpenStreetMap.

1.  Abre QGIS.
2.  Dirígete a la barra de menú y selecciona “Complementos” \>
    “Administrar e instalar complementos…”.
3.  En la ventana emergente, escribe “QuickMapServices” en la barra de
    búsqueda.
4.  Selecciona el complemento “QuickMapServices” de la lista y haz clic
    en “Instalar complemento”.
5.  Activa los *contributed packs*, en “Web” \> “QuickMapServices” \>
    “Settings” \> Pestaña “More services” \> Botón “Get contributed
    packs”.
6.  Una vez instalado y activados los *contributed packs*, regresa a la
    ventana principal de QGIS y haz clic en el menú “Web” \>
    “QuickMapServices” y elige un mapa base, como Google Maps o
    OpenStreetMap; explora otras opciones, como las de CartoDB, Stamen,
    Bing y ESRI. Enfócaño en el área de República Dominicana, usando la
    herramienta de Zoom convenientemente.

**Entrega:** Párrafo resumen del proceso realizado y captura de pantalla
de QGIS con un mapa base cargado, por ejemplo, Google Maps. *Caption*
sugerido para la imagen (puedes usar uno escrito por ti): “Uso de
QuickMapServices para cargar un mapa base en QGIS.”

## Ejercicio 3. Instalación del complemento GBIF Occurrences

**Resumen:** Con este complemento, podrás acceder y cargar datos de
biodiversidad directamente desde GBIF.

1.  En QGIS, dirígete a “Complementos” \> “Administrar e instalar
    complementos…”.
2.  Busca “GBIF Occurrences” y haz clic en “Instalar complemento”.
3.  Una vez instalado, podrás acceder al complemento desde el menú
    “Vector” \> “GBIF Occurrences” \> “Load GBIF Occurrences”.
4.  Haz búsqueda de la familia que hayas elegido, restringiendo sólo
    para República Dominicana, porque si realizas una búsqueda global,
    el complemento podría devolver numerosos registros difíciles de
    manejar.

**Entrega:** Párrafo resumen del proceso realizado y captura de pantalla
mostrando el complemento “GBIF Occurrences” instalado y disponible en
QGIS. *Caption* sugerido para la imagen (puedes usar uno escrito por
ti): “Complemento GBIF Occurrences instalado en QGIS.”

## Ejercicio 4. Representación en QGIS de un CSV descargado desde GBIF

**Resumen:** Aprenderás a visualizar datos biogeográficos de GBIF en
QGIS.

1.  Visita <https://www.gbif.org/> para acceder la interfaz web de GBIF.
    Esta interfaz antes proporcionaba descargas sin necesidad de
    registrarte en el servicio, pero ahora es prácticamene obligatorio
    crearte una cuenta, así que, tendrás que crearla.
2.  Busca una familia de organismos de tu elección (asegúrate de no
    elegir la misma familia que otro compañero o compañera),
    restringiendo sólo para República Dominicana, porque si realizas una
    búsqueda global, el complemento podría devolver numerosos registros
    difíciles de manejar.
3.  Descarga los registros en formato CSV.
4.  En QGIS, dirígete a “Capa” \> “Añadir capa” \> “Añadir capa de texto
    delimitado”.
5.  Busca y selecciona el CSV descargado.
6.  Asegúrate de que las coordenadas se interpreten correctamente y
    agrega la capa.
7.  Dirígete a las propiedades de la capa y en la sección “Símbolo”,
    elige una simbolización por color basada en el género de los
    organismos.
8.  Asegúrate de usar una base cartográfica de fondo, como
    OpenStreetMap, que sirva de referencia territorial.

**Entrega:** Párrafo resumen del proceso realizado y captura de pantalla
mostrando los registros de GBIF visualizados en QGIS con una
simbolización por color según el género. *Caption* sugerido para la
imagen (puedes usar uno escrito por ti): “Representación en QGIS de
datos de GBIF con simbolización por género.”

## Ejercicio 5 (plato fuerte). Diseño de muestreo espacial estratificado usando QGIS y fuentes de datos globales

**Resumen:** Aprenderás a realizar un diseño de muestreo espacial
estratificado por coberturas, lanzando 30 puntos aleatoriamente
localizados sobre dos coberturas del suelo diferentes, distribuidos
proporcionalmente según el área de cada cobertura.

> Para este ejercicio específicamente, dispone de un vídeo de apoyo. El
> enlace lo encontrarás en el [portal de la
> asignatura](https://github.com/biogeografia-202402), al lado del
> nombre de esta asignación (“PD05”). El vídeo explica cómo realizar los
> pasos necesarios para el diseño de muestreo espacial estratificado, y
> algunos detalles sobre el tipo de muestreo y la fuente ráster usada.

En este ejercicio, explorarás cómo se distribuyen distintas coberturas
dentro de una pequeña área de RD (diferente para cada estudiante),
usando una fuente abierta y un software SIG, en este caso QGIS.

La capa ráster de coberturas es el mapa global titulado “Land Cover
100m: version 3 Globe 2015-2019” (Buchhorn et al., s. f.). El mapa se
elaboró de forma sistemática para todos los años comprendidos en el
periodo 2015-2019, pero en esta ejercicio sólo usarás la fuente de 2019.
El ráster tiene una resolución espacial de 100m, y representa múltiples
coberturas del suelo clasificadas mediante algoritmos de *machine
learning*. Fue elaborado por el equipo del componente global del
Servicio de Monitoreo de Tierras de Copernicus, el cual produce
sistemáticamente mapas globales de cobertura y cambios en la cobertura
del suelo, así como estadísticas sobre la superficie cubierta por cada
cobertura. Los principales insumos usados para realizar dicho mapa,
fueron observaciones del satélite PROBA-V, organizadas en millones de
teselas (cuadros) equivalentes a los del satélite Sentinel-2, de 110x110
km.

Estos son los pasos clave que debes dar para realizar un muestreo
estratificado:

1.  Elige y descarga, desde [esta
    ruta](https://github.com/biogeografia-master/intro-qgis-diseno-muestreo-espacial/tree/main/fuentes),
    una capa vectorial. Identifícala en función del número de estudiante
    que hayas elegido (nota que los nombres de archivo siguen el patrón
    `estudiante-##.kml`, donde `##` son dígitos identificadores). Elige
    un archivo, no olvides anunciarlo en el foro, y recuerda que
    `estudiante-01.kml` es del Tali.

2.  Carga tu capa vectorial elegida en QGIS.

3.  Descarga, [desde aquí](https://lcviewer.vito.be/download), la capa
    ráster del año 2019 correspondiente al mapa “Land Cover 100m:
    version 3 Globe 2015-2019”. Para esto, haz clic sobre el área que
    cubre nuestro país, luego elige “*Discrete classification*” dentro
    del grupo *Land Cover Classification* y finalmente presiona el botón
    “2019” para iniciar la descarg. Normalmente, obtendrás un archivo
    con el nombre
    “W080N20_PROBAV_LC100_global_v3.0.1_2019-nrt_Discrete-Classification-map_EPSG-4326.tif”.
    Ten presente que el archivo que descargarás cubre un área de mucho
    mayor tamaño que la isla Española (abarca partes de Centroamérica y
    Sudamérica); esto se debe a que el Servicio de Monitoreo de Tierras
    de Copernicus ofrece cuadros (teselas) muy grandes, de 20x20 grados
    (~2200x2150 km). Más adelante, te explico cómo recortar el ráster
    dentro de tu área elegida.

4.  Observa el área del ráster de coberturas dentro tu capa elegida,
    identifica qué coberturas están presentes y cómo éstas se
    distribuyen espacialmente, y qué tan repartidas proporcionalmente
    están las coberturas. Usa la herramienta de “Identificación de
    elementos” (*Identify features*) para hacer clic sobre el ráster y
    explorar los valores numéricos de cada celda; dichos valores se
    corresponden con la leyenda de la tabla 4 de [este
    PDF](https://zenodo.org/records/4723921/files/CGLOPS1_PUM_LC100m-V3_I3.4.pdf?download=1).
    Para usuarios/as avanzados/as: existe un complemento llamado “*Value
    tool*” que ofrece el valor de las celdas sin necesidad de hacer clic
    sobre ellas, basta con pasar el puntero del ratón por encima del
    ráster (si te interesa, instala primero dicho complemento).

5.  Realiza el muestreo espacial estratificado en tu área (recuerda, 30
    puntos en total en toda tu área de trabajo elegida). Para esto,
    primero divide tu área según el uso y la cobertura del terreno y
    luego lanza los puntos aleatoriamente. ¿Cómo se hace en QGIS? Te lo
    detallo:

- Carga la capa de raster de uso y cobertura del suelo en QGIS.
  Normalmente, será un archivo que descargarías en la ruta mencionada
  arriba, y que tendrá por nombre algo tal que
  “W080N20_PROBAV_LC100_global_v3.0.1_2019-nrt_Discrete-Classification-map_EPSG-4326.tif”.

- Corta el ráster. Usando la herramienta `Clip Raster by Mask Layer`
  (`Cortar Ráster por capa de máscara`) del menú `Raster>Misceléneos`,
  recorta el ráster de coberturas a tu capa vectorial. Indícale que la
  capa de máscara es tu capa vectorial, y que el ráster de entrada (el
  ráster a recortar) es el de coberturas. Elige una ruta/nombre para el
  ráster de salida (por ejemplo, `coberturas-recortado.tif`), y presiona
  ejecutar.

- Clasificación del Raster. Para simplificar, reclasifica el ráster de
  coberturas que acabas de recortar en sólo dos clases: las celdas de
  bosque (con valores originalmente de 111 a 126, representadas por
  tonos verdes) deberían reclasificarse a valor 1; las celdas restantes
  (por ejemplo, matorral, urbano), deberían reclasificarse a valor 0.
  Para esto, necesitarás revisar la tabla 4 de [este
  PDF](https://zenodo.org/records/4723921/files/CGLOPS1_PUM_LC100m-V3_I3.4.pdf?download=1).
  Usa la herramienta `Reclassify by table` (`Reclasificar por tabla`) en
  QGIS para hacer la reclasificación. Para esto, deberás crear una tabla
  de reclasificación, donde los valores que representan el bosque asuman
  valor 1 y todos los restantes valores se reasignen a 0. Debes observar
  tanto la creación de la tabla como la forma de elegir los límites de
  los umbrales. Usa [este vídeo (en
  español)](https://www.youtube.com/watch?v=hT_7BI93gEg) o [este otro
  (en inglés)](https://www.youtube.com/watch?v=s7KrIjvcCz0) para
  informarte sobre el uso de la herramienta. Define una ruta y un nombre
  de salida para el ráster reclasificado, por ejemplo,
  `coberturas-reclasificado.tif`. Para usuarios/as avanzados/as: QGIS
  está preparado para realizar el diseño de muestreo estratificando con
  más de dos clases, en cuyo caso seguirías los mismos pasos explicados
  hasta este punto, conservando las clases que sean de tu interés.

- Símbolos y visualización. Cuando hayas reclasificado la capa, se
  cargará automáticamente en el lienzo de QGIS si así se especificó al
  momento de crearla. Modifica la simbología de la capa ráster
  reclasificada, estableciendo el valor máximo a 1, para visualizar las
  coberturas agrupadas rápidamente.

- Convierte de ráster a vectorial (polígonos). Convierte el raster
  reclasificado en una capa vectorial. Utiliza el comando
  `Poligonizar "Ráster a Vectorial` (`Polygonize (Raster to Vector)`)
  del menú `Ráster>Conversión`, y elige una ruta y nombre de archivo de
  salida (por ejemplo, `cobertura-vectorial.gpkg`).

- Del vectorial de coberturas, selecciona los polígonos con valor “1” en
  el campo DN. Para esto, abre la tabla de atributos del vectorial, y
  selecciona los elementos de interés. Puedes hacerlo usando el ratón y
  manteniendo la tecla `Control` (`Ctrl`) del teclado presionada, pero
  si son muchos elementos (polígonos), éste podría no ser un método
  práctico. Puedes seleccionar también por atributos, para lo cual, abre
  la tabla de atributos, y usa la herramienta
  `Seleccionar elementos usando una expresión` (coloca la expresión
  `"DN" = 1` y presiona `Seleccionar elementos`), o la herramienta
  `Seleccionar/filtrar elementos usando un formulario` (escribe `1` en
  el campo de formulario `DN` y presiona `Seleccionar elementos`).

- Lanza los puntos aleatorios. Abre la herramienta
  `Puntos aleatorios en los límites de la capa` del menú
  `Vector>Herramientas de investigación`, en `Capa de entrada` elige el
  vectorial de coberturas, marca la opción
  `Sólo elementos seleccionados` y en número de puntos deberás escribir
  cuántos puntos aleatorios lanzar (ver siguiente oración), no cambies
  la opción `Distancia mínima entre puntos` y elige una ruta y nombre de
  salida para el vectorial de puntos aleatorios (por ejemplo,
  `puntos-bosque.gpkg`). El número de puntos a lanzar debe ser
  proporcional a la superficie que ocupa el bosque en tu área elegida.
  Supón que, en tu área elegida, el bosque ocupa el 70%. Pues bien, de
  30 puntos en total que debes lanzar en tu área elegida (número
  aproximado, no es estricto), lanzarás aleatoriamente en tu área
  elegida, 21 (el 70%, que equivale a `30x0.7`) deberían caer en bosque,
  y los restantes 9 en la otra cobertura. Puedes calcular el área de la
  cobertura bosque y de la cobertura no bosque usando la herramienta
  `Añadir atributos de geometría` en el menú
  `Vector>Herramientas de geometría`. Sin embargo, para mantener la
  práctica lo más simple posible, realiza el cálculo de proporciones por
  medio de estimación visual, para lo cual, observa los polígonos de
  bosque y no bosque y estima que proporciones hay (por ejemplo, 40% y
  60%, o 20% y 80%), y usa dichas proporciones para decidir cuántos
  puntos lanzar dentro de cada cobertura.

- Repite los pasos 5.6 y 5.7 para el área de no bosque.

- Simboliza los puntos. Define una simbología común para los puntos que
  corresponden a la cobertura bosque, y otra simbología, también común,
  para los puntos de la cobertura no bosque, de tal suerte que los
  puntos dentro de la cobertura bosque tendrán la misma simbología entre
  sí, pero se diferenciarán de los puntos de la cobertura no bosque (y
  viceversa). Puedes usar el color o la forma del punto, o ambas. Bonus:
  si puedes, coloca etiquetas a cada punto, yendo a la pestaña
  `Etiquetas` del panel `Estilo de capas`, definiendo
  `Etiquetas sencillas` y en `Valor` colocando eligiendo el campo `id`.
  Esto hará que los puntos tengan un rótulo único que los diferencie
  entre sí.

- Paso final. Observa el resultado de los puntos aleatorios con la capa
  vectorial de coberturas. Deberías notar que la proporcionalidad en
  cuanto al área (estimada o calculada) de cada cobertura se corresponde
  con la proporcionalidad de tipos puntos. El mapa de los puntos
  aleatorios deberá figurar en el documento de entrega (ver párrafo
  siguiente).

**Entrega:** Un texto (dentro del archivo de plantilla) explicando el
proceso y mostrando los resultados. El texto puede tener la extensión
que consideres conveniente, sin que sea excesiva (considera un límite
bueno unas 5 páginas máximo), donde se apliquen estilos de título
adecuadamente (títulos, cuerpo de texto, pie de figura, y cualquier
otro), y donde se inserten figuras, pies de figuras, tablas, títulos de
tablas, referencias cruzadas a figuras/tablas, citas y lista de
referencias bibliográficas.

## Recordatorios finales

- De forma general, no olvides usar referencias bibliográficas. Por
  ejemplo, estas dos son obligatorias en distintos ejercicios, pero
  puedes añadir otras, como el dataset de GBIF específico (el cual tiene
  un DOI), referencias sobre tu familia elegida, etc.

  - [QGIS. (n.d.). QGIS Geographic Information
    System.](https://qgis.org/)
  - [GBIF. (n.d.). GBIF: Global Biodiversity Information
    Facility.](https://www.gbif.org/)

- **RECUADRO: recomendaciones básicas de redacción**

> Usa una voz (activa o pasiva) de forma consistente, pero sólo ten
> presente que la redacción de manuscritos científicos a menudo se
> utilizan ambas voces, dependiendo del contexto y el mensaje que el/la
> autor/a quiera transmitir. Veamos algunos ejemplos:
>
> **Voz activa en manuscrito científicos:**
>
> - **Analicé** los datos utilizando el lenguaje de programación Python.
>
> - El experimento **mostró** que la temperatura afecta directamente la
>   tasa de reacción.
>
> - Los investigadores **encontraron** una correlación significativa
>   entre las dos variables.
>
> La voz activa puede hacer que la redacción parezca más directa y
> clara, y es especialmente útil cuando el/la autor/a quiere enfatizar
> quién llevó a cabo una acción o cuándo se desea hacer una afirmación
> fuerte.
>
> **Voz pasiva en artículos científicos:**
>
> - Los datos **fueron analizados** utilizando el lenguaje de
>   programación Python.
>
> - **Se observó** que la temperatura afecta directamente la tasa de
>   reacción.
>
> - Una correlación significativa **fue encontrada** entre las dos
>   variables.
>
> La voz pasiva es común en la redacción científica porque a menudo se
> prefiere un tono más impersonal, enfocando la atención en los
> resultados y procedimientos en lugar de en quienes llevaron a cabo la
> investigación. También puede ser útil cuando no se quiere o no es
> relevante especificar quién realizó la acción.
>
> **En todas mis prácticas, está completamente permitido usar IA
> (e.g. chatGPT), pero te recomiendo que la uses más como tutor que como
> redactor**. Tal como te sugerí arriba, no le pidas que te resuelva los
> problemas del mandato. Pídele que te dé ideas, y que luego tú las
> mejores o las descartes. No abuses tampoco del texto, pues mucha
> redacción no siempre es mejor; en redacción de ensayos “menos es más”.
> Cruza las redacciones que te ofrezca con tu conocimiento, y revisa si
> los términos o conceptos usados son descabellados (toda IA se inventa
> cosas, cuidate de no caer en esa trampa). Nunca le pidas referencias
> bibliográficas, porque se va equivocar.

# Referencias

<div id="refs" class="references csl-bib-body hanging-indent"
entry-spacing="0" line-spacing="2">

<div id="ref-buchhorn" class="csl-entry">

Buchhorn, M., Smets, B., Bertels, L., Roo, B. D., Lesiv, M., Tsendbazar,
N.-E., Herold, M. y Fritz, S. (s. f.). *Copernicus Global Land Service:
Land Cover 100m: collection 3: epoch 2019: Globe*.
<https://doi.org/10.5281/ZENODO.3939050>

</div>

</div>
