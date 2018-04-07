# Lección 3: Fundamentos cartográficos y geodésicos

## Geodesia

* Geodesia: la ciencia que se encarga del estudio de la forma de la Tierra. Uno de los objetivos principales de la geodesia es establecer un sistema de referencia y definir un conjunto de puntos (conocidos como vértices geodésicos) cuyas coordenadas en dicho sistema sean conocidas con una precisión elevada.

* Geodesia esferoidal: La determinación de la forma y dimensiones de la Tierra.
* Geodesia física: La ciencia encargada de analizar el campo gravitatorio terrestre y sus variaciones-
* Astronomía geodésica.
* Proyecciones cartográficas.


## Elipsoide de referencia y geoide

* Elipsoide de referencia y el geoide: conceptos básicos para asimilar la forma de la Tierra.

Podemos seguir tratando de asimilar la forma de la Tierra a la de una superficie teórica, aunque no ya la de una esfera sino la de lo que se denomina un *elipsoide*.

Sobre un elipsoide, el radio de la Tierra ya no es constante, sino que depende del emplazamiento.

La necesidad de trabajar con un elipsoide global para todo el planeta es más reciente, pero ya desde hace casi un siglo se hace patente que debe realizarse un esfuerzo por homogeneizar el uso de elipsoides, de tal modo que pueda trabajarse con una referencia internacional que facilite el uso de cartografía en las distintas zonas del planeta.

El elipsoide WGS–84 es muy empleado en la actualidad, pues es el utilizado por el sistema GPS.

El geoide:
* Superficie tridimensional en cuyos puntos la atracción gravitatoria es constante
* No es una superficie regular como el elipsoide.
* Presenta protuberancias y depresiones que lo diferencian.
* La densidad de la Tierra no es constante en todos sus puntos, y ello da lugar a que el geoide sea una superficie irregular como consecuencia de las anomalías gravimétricas que dichas variaciones de densidad ocasionan.
* Alturas Geoidales: Diferencias, con un orden máximo de +-100 metros, entre la superficie del geoide y del elipsoide.

* Datum: Conjunto formado por una superficie de referencia (el elipsoide) y un punto en el que «enlazar» este al geoide.
* Punto astronómico fundamental: punto en el que enlaza el datum con el geoide. En él, el elipsoide es **tangente** al geoide. En este punto:
  * La altura geoidal es igual a cero.
  * La vertical al geoide y al elipsoide son idénticas.

Para un mismo elipsoide pueden utilizarse distintos **puntos fundamentales**, que darán lugar a distintos **datum** y a **distintas coordenadas** para un mismo punto.

## Sistemas de coordenadas

* Proyección cartográficas: Proyección que sitúa los elementos de la superficie del elipsoide sobre una superficie plana.
* Coordenadas cartesianas: coordenadas resultantes al aplicar una proyección cartográfica.

### Coordenadas geográficas

El sistema de coordenadas geográficas es un sistema de coordenadas esféricas mediante el cual un punto se localiza con dos valores angulares.

* Latitud:
  * Ángulo φ formado por la línea que une el centro de la esfera terrestre con un punto de su superficie y el plano ecuatorial.
  * Paralelos: líneas formadas por puntos de la misma latitud que forman círculos concéntricos paralelos al ecuador.
  * Es de 0 grados en el ecuador.
  * Puede expresarse especificando si el punto se sitúa al norte del ecuador (N) o al sur del ecuador (S) o especificando el signo, positivo o negativo respectivamente.

* Longitud:
  * Ángulo λ formado entre dos de los planos que contienen a la línea que une los Polos.
  * Meridianos: líneas formadas por puntos de igual longitud.
  * Meridiano de Greenwich: Meridiano de referencia que pasa por el observatorio de Greenwich, en el Reino Unido. Divide el globo en hemisferio Este y Oeste.
  * El primer plano es un plan arbitrario que se toma como referencia.
  * El segundo plano, además de contener a la línea de los polos, contiene al punto en cuestión.
  * Puede expresarse especificando si el punto se sitúa al este del meridiano (E) o al oeste (O), o especificando el signo, positivo o negativo respectivamente.


* Las coordenadas geográficas resultan de gran utilidad, especialmente cuando se trabaja con grandes regiones.
* No obstante, no se trata de un sistema cartesiano, y tareas como la medición de áreas o distancias es mucho más complicada.
* Si bien la distancia entre dos paralelos es prácticamente constante (un grado de latitud equivale más o menos a una misma distancia en todos los puntos)
* La distancia entre dos meridianos no es constante, y varía entre unos 11,3 kilómetros en el Ecuador hasta los cero kilómetros en los polos, donde los meridianos convergen.

### Proyecciones Cartográficas

* Proyección cartográfica:
    * Resultado del proceso de asignar una coordenada plana a cada punto de la superficie de la Tierra.
    * Correspondencia matemática biunívoca entre los puntos de una esfera o elipsoide y sus transformados en un plano.

    * Una aplicación `f` que a cada par de coordenadas geográficas `(φ,λ)` le hace corresponder un par de coordenadas cartesianas `(x,y)`:

    ```
    x=f(φ,λ);
    y=f(φ,λ);
    ```

    * De igual modo, las coordenadas geográficas puede obtenerse a partir de las cartesianas según:

    ```
    φ = g(x,y) ; λ = g(x,y)
    ```

#### Tipos de Proyecciones

> La elección de una u otra proyección es función de las necesidades particulares.

Clasificación según la superficie sobre la que se proyectan los puntos:

* Cónicas:
  * La superficie desarrollable es un cono
  * Ejemplos:
    * Proyección cónica equiárea de Albers
    * Proyección conforme cónica de Lambert

* Cilíndricas:
   * La superficie desarrollable es un cilindro
   * Al proyectar, los meridianos se convierten en lineas paralelas, así como los paralelos, aunque la distancia entre estos últimos no es constante.
   * Concepciones:
    * Proyección normal o simple: el cilindro se sitúa de forma tangente al ecuador.
    * Proyección transversa: el cilindro se sitúa de forma secante a los meridianos.
    * Proyección oblicua: el cilindro se sitúa de forma secante a otros puntos.
  * Ejemplos:
    * La proyección de Mercator
    * La proyección transversa de Mercator
    * La proyección cilíndrica de Miller
    * La proyección cilíndrica equiárea de Lambert.

* Planas o azimutales
  * La superficie desarrollable es directamente un plano
  * En función de la posición del punto de fuga:
    * Gnómica o central: El punto de fuga se sitúa en el centro del elipsoide
    * Estereográfica: El plano es tangente y el punto de fuga se sitúa en las antípodas del punto de tangencia. La proyección polar estereográfica es empleada habitualmente para cartografiar las regiones polares
    * Ortográfica. El punto de fuga se sitúa en el infinito

* Otros:
  * Existen proyecciones no utilizan una superficie desarrollable como tal sino modificaciones a esta idea (como las policónicas que utilizan varios conos)
  * En algunos casos surgen como una necesidad cartográfica concreta

Clasificación según las propiedades métricas que conserven:

* Equiárea:
  * Se mantiene una escala constante.
  * La relación entre un área terrestre y el área proyectada es la misma independientemente de la localización.
  * Puede emplearse para comparar superficies.
* Conformes:
  * Mantienen la forma de los objetos, ya que no provocan distorsión de los ángulos.
  * Los meridianos y los paralelos se cortan en la proyección en ángulo recto, igual que sucede en la realidad.
  * Su principal desventaja es que introducen una gran distorsión en el tamaño, y objetos que aparecen proyectados con un tamaño mucho mayor que otros pueden ser en la realidad mucho menores que estos.
* Equidistantes:
  * Se mantienen las distancias.


* Anamorfosis: distorsión al aplicar una proyección

* Codificación de los sistemas de referencia EPSG.


### Sistema UTM

* Una de las proyecciones más extendidas en todos los ámbitos es la **proyección universal transversa de Mercator**.
* Esta proyección da lugar al sistema de coordenadas **UTM**.
* Este sistema fue desarrollado por el ejército de los Estados Unidos.
* Se trata de un sistema completo para cartografiar la practica totalidad de la Tierra.

* La Tierra se divide en una serie de zonas rectangulares mediante una cuadricula y se aplica una proyección y unos parámetros geodésicos concretos a cada una de dichas zonas.
* En la actualidad se emplea un único elipsoide, **WGS–84**
* Con este sistema, las coordenadas de un punto no se expresan como coordenadas terrestres absolutas, sino mediante la zona correspondiente y las coordenadas relativas a la zona UTM en la que nos encontremos.


#### Cuadrícula UTM

* La cuadricula UTM tiene un total de 60 husos numerados entre 1 y 60.
* **Longitud**: cada huso abarca una amplitud de 6◦ de longitud.
* El huso 1 se sitúa entre los 180◦y 174◦O, y la numeración avanza hacia el Este.
* **Latitud**: cada huso se divide en 20 zonas, que van desde los 80◦S hasta los 84◦N.
* Éstas se codifican con letras desde la C a la X, no utilizándose las letras I y O por su similitud con los dígitos 1 y 0.
* Cada zona abarca 8 grados de longitud, excepto la X que se prolonga unos 4 grados adicionales.

* Una zona UTM se localiza con un número y una letra, y es en función de la zona como posteriormente se dan las coordenadas que localizan un punto.
* Estas coordenadas se expresan en metros y expresan la distancia entre el punto y el origen de la zona UTM en concreto.
* El origen de la zona se sitúa en el punto de corte entre el meridiano central de la zona y el ecuador.
* Para evitar la aparición de números negativos, se considera que el origen no tiene una coordenada X de 0 metros, sino de 50000.
* Cuando se trabaja en el hemisferio sur (donde las coordenadas Y serían siempre negativas), se considera que el origen tiene una coordenada Y de 10000000 metros, lo cual hace que todas las coordenadas referidas a él sean positivas.
* Para las zonas polares no resulta adecuado emplear el sistema UTM, ya que las distorsiones que produce son demasiado grandes. En su lugar, se utiliza el sistema **UPS** (Universal Polar Stereographic).

### Transformación de Coordenadas

### Conversión de Coordenadas

### Codificación de sistemas de referencia

## Escala

## Generalización Cartográfica
