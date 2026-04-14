## Apuntes unidad 2 :  Graficación 2D
La graficación bidimensional es una forma de representar y trabajar con objetos en un plano de dos dimensiones, utilizando herramientas matemáticas y digitales. Gracias a esto, es posible crear figuras, modificarlas y darles diferentes formas según lo que se necesite. A lo largo de este trabajo se explican distintos temas que permiten entender cómo funcionan estos procesos, como las transformaciones geométricas, que sirven para mover, girar o cambiar el tamaño de los objetos, así como la representación matricial, que ayuda a realizar estos cambios de manera más eficiente. También se incluyen otros elementos importantes como las curvas, los fractales y la creación de fuentes de texto, los cuales permiten generar diseños más complejos y visualmente atractivos. En conjunto, todos estos conceptos ayudan a comprender mejor cómo se construyen y manipulan los gráficos en 2D dentro de diferentes aplicaciones digitales.


## 2.1  Transformación bidimensional.

La transformación bidimensional es el proceso mediante el cual se modifican las características de una figura dentro de un plano de dos dimensiones (2D). Estas modificaciones pueden afectar su posición, tamaño, orientación o forma, sin necesidad de crear una nueva figura.
Se basa en operaciones matemáticas aplicadas a las coordenadas de los puntos que forman la figura, lo que permite obtener una nueva representación de la misma. Entre estas operaciones se encuentran la traslación, el escalamiento, la rotación y el sesgado.
Este tipo de transformación es muy importante en áreas como la graficación por computadora, el diseño gráfico y la animación, ya que permite manipular imágenes y objetos de manera eficiente, facilitando su visualización, movimiento y análisis.

**Aplicaciones**

-Diseño gráfico: En el diseño gráfico, las transformaciones bidimensionales permiten modificar imágenes y figuras sin tener que crearlas desde cero, se utilizan para cambiar el tamaño (escalado), mover elementos (traslación) o girarlos (rotación). Esto facilita la creación de logotipos, ilustraciones y composiciones visuales de manera más rápida y precisa.


-Animación: En la animación, estas transformaciones son esenciales para dar movimiento a los objetos. Por ejemplo, un personaje puede moverse de un lugar a otro (traslación), girar (rotación) o cambiar de tamaño (escala), gracias a esto, se pueden crear secuencias fluidas que simulan movimiento en pantalla


-Modelado en 2D: En el modelado en 2D, se utilizan para diseñar personajes, escenarios y objetos dentro de videojuegos o aplicaciones. Las transformaciones permiten posicionar correctamente cada elemento en la escena y ajustar su tamaño o dirección.


-Interfaz de usuario (UI): En las interfaces de usuario, las transformaciones permiten mejorar la experiencia del usuario. Por ejemplo, los botones pueden cambiar de tamaño al tocarlos (escala), moverse o animarse para llamar la atención.




## 2.1.1. Traslación.

La traslación es una transformación bidimensional que consiste en mover una figura de una posición a otra en línea recta, sin cambiar su forma, tamaño ni orientación, es decir, la figura solo se desliza en el plano. Para trasladar un punto, se le suman dos valores llamados tx y ty a sus coordenadas originales si tenemos un punto (x, y), después de la traslación se convierte en (x + tx, y + ty), estos valores indican cuánto se mueve el objeto en el eje X y en el eje Y.
El conjunto de valores (tx, ty) se conoce como vector de traslación, ya que indica la dirección y la distancia del movimiento este vector nos dice hacia dónde y cuánto se va a desplazar la figura. Cuando se traslada una figura como un polígono, se aplica el mismo vector de traslación a cada uno de sus vértices después, se reconstruye la figura con las nuevas coordenadas, manteniendo su forma original.


**Características**
-Cambio de posición mediante coordenadas: La traslación consiste en desplazar un punto desde una posición original (x, y) hacia una nueva posición (x’, y’), este desplazamiento se realiza sumando las distancias de traslación en cada eje  donde Tx y Ty representan las magnitudes de desplazamiento en los ejes X y Y, respectivamente.


-Uso del vector de traslación: El par ordenado (Tx, Ty) se denomina vector de traslación o vector de cambio, ya que define tanto la dirección como la distancia del desplazamiento. Este vector es fundamental para describir el movimiento aplicado a cualquier objeto dentro del plano cartesiano.


-Aplicación en polígonos: En el caso de figuras compuestas por múltiples puntos, como los polígonos, la traslación se realiza aplicando el mismo vector de traslación a cada uno de sus vértices. Como resultado, la figura se reposiciona completamente sin sufrir alteraciones en su forma, tamaño o proporciones.


-Aplicación en objetos curvos: Para figuras definidas mediante curvas, como circunferencias o elipses, la traslación implica modificar sus parámetros principales, como las coordenadas del centro. Una vez trasladados estos puntos de referencia, la figura se reconstruye en su nueva ubicación manteniendo sus características originales.


-Naturaleza de las distancias de traslación
Las distancias de traslación pueden tomar cualquier valor real, es decir, pueden ser positivas, negativas o nulas. Un valor positivo indica un desplazamiento en el sentido positivo del eje, mientras que un valor negativo indica un movimiento en sentido contrario.



-Limitaciones dentro del sistema de representación: Cuando un objeto es trasladado fuera de los límites del área de visualización o del sistema gráfico, pueden presentarse diferentes situaciones, como la omisión parcial del objeto, su recorte o incluso la generación de errores en el sistema. Estas limitaciones dependen del entorno o software utilizado.


-Conservación de las propiedades geométricas: Una característica esencial de la traslación es que no altera las propiedades del objeto. Es decir, la figura conserva su forma, tamaño, orientación y proporciones, ya que únicamente cambia su posición en el plano.

## 2.1.2. Escalamiento.

El escalamiento es una transformación geométrica bidimensional que consiste en modificar el tamaño de un objeto dentro del plano cartesiano, ya sea aumentándolo o reduciéndolo, sin alterar su forma general. Esta transformación se realiza mediante el uso de factores de escala, los cuales determinan cuánto se expanden o contraen las dimensiones del objeto en cada eje.

Para aplicar el escalamiento, se multiplican las coordenadas de cada punto del objeto por los factores de escala correspondientes en los ejes X y Y. Si un punto original tiene coordenadas (x, y), sus nuevas coordenadas (x’, y’) se obtienen de la siguiente manera:
**x’= X⋅ sx    y’= y⋅ sy** donde Sx y Sy representan los factores de escalamiento en los ejes X y Y, respectivamente.

El efecto del escalamiento depende del valor de estos factores:

-Si el factor es mayor que 1, el objeto aumenta de tamaño (ampliación).

-Si el factor está entre 0 y 1, el objeto se reduce (disminución).

-Si el factor es igual a 1, el objeto permanece sin cambios.


El escalamiento permite generar efectos visuales importantes, como el zoom, y es ampliamente utilizado en áreas como gráficos por computadora, animación, diseño digital y modelado geométrico.

Tipos de escalamiento

**1. Escalamiento uniforme**: En este tipo de transformación, los factores de escala son iguales en ambos ejes, es decir, Sx = Sy, esto provoca que el objeto cambie de tamaño de manera proporcional, manteniendo exactamente su forma y proporciones originales. Es el tipo de escalamiento más utilizado cuando se desea ampliar o reducir un objeto sin distorsionarlo.



**2. Escalamiento diferencial (no uniforme)**: En este caso, los factores de escala son diferentes en cada eje, es decir, sx ≠sy como resultado, el objeto se deforma, ya que se estira o comprime en una dirección más que en la otra. Este tipo de escalamiento se utiliza cuando se desea modificar la forma del objeto o adaptarlo a ciertas condiciones específicas.


**Características**


-Uso de factores de escala: El escalamiento se realiza mediante dos factores, Sx y Sy, que representan el cambio de tamaño en los ejes X y Y, respectivamente. Estos factores son valores numéricos reales positivos que determinan cómo se transformarán las dimensiones del objeto.



-Efecto de los valores de escalamiento: El resultado de la transformación depende del valor de los factores de escala:

Cuando los valores son mayores que 1, el objeto experimenta un aumento de tamaño (ampliación).

Cuando los valores están entre 0 y 1, el objeto se reduce (disminución).

Cuando los valores son iguales a 1, el objeto no sufre ningún cambio en su tamaño.


-Independencia por eje: Los factores Sx y Sy pueden aplicarse de manera independiente, lo que permite modificar el tamaño del objeto de forma distinta en cada eje esto proporciona flexibilidad para adaptar la figura a diferentes necesidades o condiciones.


-Escalamiento uniforme: Cuando Sx = Sy, se produce un escalamiento uniforme por lo que en este caso, el objeto cambia de tamaño de manera proporcional en todas sus dimensiones, conservando su forma, proporciones y apariencia original. Este tipo de escalamiento es ideal cuando se desea ampliar o reducir una figura sin deformarla.



-Escalamiento diferencial (no uniforme): Cuando sx ≠sy, se presenta un escalamiento diferencial, en este caso, el objeto se modifica de manera desigual en cada eje, lo que provoca una distorsión en su forma. Es decir, la figura puede estirarse o comprimirse en una dirección específica.



-Aplicación a todos los puntos del objeto: El escalamiento se aplica a cada uno de los puntos que conforman la figura al multiplicar todas las coordenadas por los factores de escala, se obtiene una nueva representación del objeto con el tamaño modificado.


-Conservación parcial de propiedades: Aunque el escalamiento modifica el tamaño del objeto, en el caso del escalamiento uniforme se conservan sus proporciones. Sin embargo, en el escalamiento diferencial estas proporciones pueden alterarse, generando cambios en la forma del objeto.


**2.1.3. Rotación.**

La rotación es una transformación geométrica bidimensional que consiste en girar un objeto o figura alrededor de un punto fijo, denominado centro de rotación o pivote, dentro del plano cartesiano. Durante este proceso, cada uno de los puntos que conforman la figura se desplaza siguiendo trayectorias circulares, manteniendo constante su distancia respecto al punto de rotación.

Esta transformación se define mediante un ángulo de rotación (\theta), el cual determina la magnitud del giro, así como su dirección. Por convención, los ángulos positivos representan una rotación en sentido antihorario, mientras que los ángulos negativos indican una rotación en sentido horario.

A diferencia de otras transformaciones, como el escalamiento o el sesgado, la rotación no modifica las propiedades geométricas del objeto, tales como su tamaño, forma o proporciones. Únicamente altera su orientación y posición en el plano.

La rotación puede realizarse con respecto al origen del sistema de coordenadas (0,0) o alrededor de cualquier punto arbitrario (x_r, y_r). En este último caso, el proceso implica trasladar temporalmente el objeto para que el punto de rotación coincida con el origen, aplicar la rotación y posteriormente regresar el objeto a su posición original.

En el ámbito de la computación gráfica, la rotación se expresa comúnmente mediante representaciones matemáticas, como matrices de transformación, lo que permite aplicar esta operación de manera eficiente a todos los puntos de un objeto.


**Características**

-Definición mediante ángulo y punto de rotación : Para realizar una rotación es necesario especificar dos elementos fundamentales: el ángulo de rotación y el punto de rotación o pivote (xr, yr). Estos determinan la magnitud del giro y el punto alrededor del cual se realiza la transformación.

2. Sentido de la rotación: El sentido en el que se realiza la rotación depende del signo del ángulo:

-Un ángulo positivo indica una rotación en sentido antihorario.


-Un ángulo negativo indica una rotación en sentido horario.

-Trayectoria circular de los puntos: Durante la rotación, cada punto del objeto se desplaza siguiendo una trayectoria circular alrededor del punto pivote, manteniendo constante su distancia respecto a este.

-Conservación de la forma y el tamaño: La rotación es una transformación rígida, lo que significa que no altera las propiedades geométricas del objeto. La figura conserva su forma, tamaño y proporciones, cambiando únicamente su orientación.

-Aplicación uniforme a todos los puntos: Para que la rotación sea correcta, el mismo ángulo debe aplicarse a todos los puntos del objeto. Esto garantiza que la figura no se deforme durante el proceso.

-Rotación respecto al origen y puntos arbitrarios:

La rotación puede realizarse:

-Respecto al origen (0,0), utilizando directamente las ecuaciones de transformación.


-Respecto a un punto arbitrario, en cuyo caso se requiere trasladar el objeto al origen, aplicar la rotación y posteriormente regresarlo a su posición original
 
## 2.1.4. Sesgado.

El sesgado (también conocido como shear) es una transformación geométrica bidimensional que consiste en inclinar o deformar un objeto mediante el desplazamiento proporcional de sus puntos a lo largo de uno de los ejes del plano cartesiano. A diferencia de otras transformaciones como la traslación o la rotación, el sesgado sí altera la forma del objeto, aunque mantiene el paralelismo entre sus líneas.

Esta transformación se realiza modificando las coordenadas de los puntos del objeto en función de un factor de sesgo, el cual determina el grado de inclinación aplicado. Como resultado, la figura adquiere una apariencia inclinada o “recostada”, generando un efecto visual de distorsión controlada.

El sesgado es ampliamente utilizado en áreas como el diseño gráfico, la animación y el modelado digital, ya que permite crear efectos visuales dinámicos, perspectivas simuladas y formas más complejas a partir de figuras simples.


**Características**

-Transformación no rígida: El sesgado es una transformación no rígida, lo que significa que modifica la forma del objeto original. A diferencia de la traslación o la rotación, aquí sí existe deformación.



-Desplazamiento proporcional de los puntos: Los puntos del objeto se desplazan en función de su posición respecto a uno de los ejes. Este desplazamiento es proporcional, lo que genera la inclinación característica de la figura.



-Conservación del paralelismo: Aunque el objeto se deforma, las líneas que eran paralelas antes de la transformación continúan siéndolo después del sesgado.


-Dependencia de un factor de sesgo: El grado de inclinación del objeto depende de un valor llamado factor de sesgo, el cual determina cuánto se desplazan los puntos del objeto.



5. Tipos de sesgado

-Sesgo horizontal: En este tipo de transformación, los puntos se desplazan en dirección horizontal (eje X), mientras que las coordenadas en el eje Y permanecen constantes es decir, el objeto se inclina hacia los lados.

-Sesgo vertical: En este caso, los puntos se desplazan en dirección vertical (eje Y), mientras que las coordenadas en el eje X permanecen constantes.
Esto provoca que la figura se incline hacia arriba o hacia abajo.

## 2.2.Representación matricial de las transformaciones bidimensionales.

En el ámbito de la graficación por computadora, las transformaciones bidimensionales pueden representarse de manera eficiente mediante el uso de matrices, lo que permite realizar operaciones geométricas de forma estructurada y sistemática. Esta representación, conocida como representación matricial, facilita la aplicación de transformaciones como traslación, rotación, escalamiento y sesgado sobre objetos en el plano cartesiano.

Existen dos formas principales de representar las coordenadas de un punto dentro de este enfoque. La primera consiste en expresar el punto como un vector renglón, donde la matriz de transformación se multiplica por la derecha del vector para obtener el nuevo punto transformado. La segunda forma es representar el punto como un vector columna, en cuyo caso la matriz de transformación se multiplica por la izquierda. Ambas notaciones son válidas, aunque la representación mediante vectores columna es la más utilizada en la mayoría de aplicaciones gráficas.

Una de las principales ventajas de la representación matricial es que permite manejar secuencias de transformaciones de manera eficiente. En muchas aplicaciones, como la animación o el diseño asistido por computadora (CAD), es común aplicar múltiples transformaciones de forma consecutiva. Por ejemplo, un objeto puede trasladarse, rotarse y escalarse en distintos pasos para lograr un resultado final. En estos casos, cada transformación se representa mediante una matriz, y el resultado total se obtiene mediante la multiplicación de dichas matrices.

De esta manera, si se tiene un punto P y varias transformaciones representadas por matrices M_1, M_2, M_3, etc., es posible calcular directamente la posición final del punto combinando todas las matrices en una sola operación. Esto evita tener que recalcular las coordenadas paso a paso después de cada transformación, lo que mejora significativamente la eficiencia computacional.

En este contexto, algunas matrices contienen información específica según el tipo de transformación. Por ejemplo, una matriz puede incluir los ángulos de rotación y los factores de escala, mientras que otra puede incorporar los valores de traslación, relacionados con el desplazamiento del objeto o con el centro de rotación. La combinación de estas matrices permite representar transformaciones complejas de manera compacta.

Por otro lado, la representación matricial también puede compararse con otras formas de representación, como los grafos. Mientras que los grafos representan relaciones mediante nodos y conexiones visuales, la representación matricial organiza la información en forma de tablas o matrices. Esta forma presenta ventajas importantes, como la ausencia de superposición entre elementos, lo que facilita la lectura de la información, así como la identificación clara de conexiones o relaciones existentes o inexistentes.

Sin embargo, también presenta algunas desventajas. Por ejemplo, puede requerir un mayor espacio para representar la misma cantidad de información en comparación con un grafo tradicional. Además, puede resultar menos intuitiva para quienes no están familiarizados con este tipo de representación, y puede dificultar el seguimiento de relaciones complejas o recorridos entre elementos.


## 2.3. Trazo de líneas curvas.

El trazo de líneas curvas es un proceso fundamental en la representación gráfica bidimensional, ya que permite la creación de formas más complejas, suaves y naturales en comparación con las líneas rectas. A través de este tipo de trazado, es posible generar figuras con mayor nivel de detalle y estética, lo que resulta esencial en áreas como el diseño gráfico, la animación y la modelación digital.

A diferencia de las líneas rectas, que se definen mediante ecuaciones simples, las líneas curvas requieren el uso de funciones matemáticas o conjuntos de puntos que describen su trayectoria. Estas curvas pueden representarse mediante distintos métodos, como curvas paramétricas, funciones polinomiales o interpolación de puntos, lo que permite controlar su forma y comportamiento con mayor precisión.

El trazo de curvas facilita la representación de formas orgánicas y fluidas, como contornos de objetos, siluetas, trayectorias de movimiento y elementos naturales. Gracias a esto, se pueden superar las limitaciones geométricas de las líneas rectas, logrando representaciones más realistas y visualmente atractivas.

En la práctica, el trazado de líneas curvas se realiza a partir de puntos de control, los cuales determinan la forma de la curva. Modificando estos puntos, es posible ajustar la curvatura, la dirección y la suavidad de la línea. Este principio es ampliamente utilizado en herramientas de diseño digital, donde el usuario puede manipular curvas de manera interactiva.

Además, el uso de curvas es esencial en la construcción de figuras más complejas, ya que muchas formas pueden descomponerse en segmentos curvos. Esto permite modelar objetos con mayor precisión y flexibilidad, especialmente en aplicaciones como gráficos por computadora, diseño asistido por computadora (CAD) y desarrollo de videojuegos.


## 2.3.1. Bézier.

Las curvas de Bézier son un tipo de representación matemática ampliamente utilizada en la creación de gráficos y diseños en dos dimensiones, especialmente en el trazado de líneas curvas suaves y precisas. Este tipo de curvas fue desarrollado por el ingeniero francés Pierre Bézier por encargo de la empresa Renault, con el objetivo de definir de manera matemática las transiciones suaves en las formas de los automóviles.

Estas curvas se generan a partir de funciones polinómicas, comúnmente de grado tres (curvas cúbicas), lo que permite representar una gran variedad de formas curvas sin necesidad de recurrir a cálculos matemáticos excesivamente complejos. Gracias a esto, las curvas de Bézier logran un equilibrio entre precisión y eficiencia en su aplicación.

Una de las principales características de las curvas de Bézier es que están definidas por un conjunto de puntos de control. Estos puntos no solo incluyen aquellos por donde pasa la curva, sino también puntos externos que determinan su dirección y curvatura. Al modificar la posición de estos puntos, es posible ajustar la forma de la curva de manera intuitiva, lo que facilita su uso en entornos de diseño gráfico.

Además, las curvas de Bézier permiten generar trazos continuos y suaves, evitando cambios bruscos o discontinuidades en la forma. Esta propiedad las hace especialmente útiles en aplicaciones donde se requiere una alta calidad visual, como en la creación de tipografías, ilustraciones y gráficos vectoriales.

En el ámbito del diseño digital, las curvas de Bézier son fundamentales en herramientas como Inkscape y Adobe Illustrator, donde se utilizan para dibujar y manipular formas complejas de manera precisa. Su facilidad de uso y capacidad para generar curvas suaves las convierten en una herramienta esencial en el diseño moderno.

Otra ventaja importante de estas curvas es su simplicidad y eficiencia, ya que permiten crear formas complejas utilizando un número reducido de puntos de control. Esto facilita su implementación en aplicaciones interactivas y proyectos que requieren rapidez en el diseño sin sacrificar calidad.

Sin embargo, las curvas de Bézier también presentan algunas limitaciones. Cada segmento de curva está definido entre un conjunto específico de puntos de control, lo que puede restringir la complejidad de las formas si no se combinan múltiples segmentos. Por ello, en diseños más avanzados es común utilizar varias curvas de Bézier conectadas entre sí.


<img width="348" height="421" alt="image" src="https://github.com/user-attachments/assets/cff2ca46-d3df-4ce7-a215-4aec66ce3415" />


## 2.3.2. B-spline.

Las curvas B-spline (Basis spline o “splines básicas”) son un tipo de función matemática utilizada en la representación de curvas suaves dentro del área de gráficos por computadora y análisis numérico. Estas curvas fueron introducidas por el matemático Isaac Jacob Schoenberg, quien acuñó el término “B-spline” como abreviatura de basis spline. Su principal característica es que poseen un soporte mínimo, lo que significa que cada segmento de la curva está influenciado únicamente por un conjunto limitado de puntos de control.

En términos matemáticos, una B-spline es una función definida a partir de polinomios por tramos, lo que permite construir curvas suaves con un alto grado de continuidad. Un teorema fundamental establece que cualquier función spline de cierto grado y suavidad puede expresarse como una combinación lineal de B-splines del mismo grado, lo que las convierte en una base muy eficiente para representar curvas complejas.

Una de las características más importantes de las curvas B-spline es su estabilidad numérica, ya que pueden evaluarse mediante el algoritmo de de Boor, el cual permite calcular puntos sobre la curva de manera precisa y estable. Aunque existen variantes más rápidas, estas suelen sacrificar estabilidad, por lo que el algoritmo de de Boor sigue siendo ampliamente utilizado.

Desde el punto de vista geométrico, las B-spline pueden considerarse como una generalización de las curvas de Bézier, ya que permiten trabajar con múltiples segmentos sin necesidad de aumentar el grado del polinomio. Esto evita problemas como el fenómeno de Runge y proporciona una mayor flexibilidad en la construcción de curvas.

A diferencia de las curvas de Bézier, donde toda la curva depende de todos los puntos de control, en las B-spline cada punto de control afecta solo una parte de la curva. Esto permite un control local, es decir, modificar una sección de la curva sin alterar completamente el resto de la figura, lo que resulta muy útil en procesos de diseño.

Las curvas B-spline ofrecen una gran flexibilidad y control en la modelación, permitiendo la creación de formas complejas mediante la combinación de múltiples segmentos suaves. Gracias a esto, son ampliamente utilizadas en aplicaciones donde se requiere precisión y detalle en la geometría.

En el ámbito práctico, las B-spline tienen múltiples aplicaciones. En el diseño asistido por computadora (CAD), se emplean para modelar superficies tridimensionales complejas con gran exactitud. En la animación, permiten generar movimientos suaves y continuos, fundamentales para la creación de gráficos dinámicos y personajes en 3D. Asimismo, en el diseño industrial, se utilizan para desarrollar productos con formas funcionales y estéticamente agradables, mejorando aspectos como la ergonomía y la usabilidad.

** Ejemplo**

En la animación realizada, el personaje está construido utilizando curvas spline, específicamente curvas Bézier, que son un tipo de representación matemática muy utilizada en gráficos por computadora.

Las curvas Bézier funcionan mediante puntos de control, los cuales permiten definir la forma de la curva. En lugar de formar líneas rectas entre puntos, estas curvas generan transiciones suaves y continuas, lo que resulta ideal para dibujar figuras orgánicas, como el cuerpo del conejo en la animación.

Este tipo de curvas pertenece a la familia de las splines, que son funciones matemáticas diseñadas para crear formas suaves a partir de varios puntos. Dentro de esta misma familia también se encuentran las B-spline (Basis spline), que son una generalización más avanzada.

<img width="589" height="477" alt="image" src="https://github.com/user-attachments/assets/8d8932b7-3159-4809-94ab-d873a0bce836" />

<img width="589" height="248" alt="image" src="https://github.com/user-attachments/assets/6912dcd8-578c-4b72-b689-10335242315c" />

## 2.4. Fractales

Un fractal es un objeto geométrico cuya estructura se repite a diferentes escalas, es decir, presenta un patrón que se reproduce de forma similar tanto en su forma completa como en sus partes más pequeñas. Esta característica se conoce como autosimilitud, y permite que los fractales tengan una apariencia compleja a partir de reglas simples.

El término “fractal” fue propuesto en 1975 por el matemático Benoît Mandelbrot, y proviene del latín fractus, que significa “quebrado” o “fragmentado”. Este nombre describe la naturaleza irregular y fragmentada de estas figuras, las cuales no siguen las formas geométricas tradicionales.

Una de las propiedades más importantes de los fractales es que poseen una dimensión fractal, la cual no necesariamente es un número entero. A diferencia de las figuras clásicas (como líneas, cuadrados o cubos), los fractales pueden tener dimensiones intermedias, lo que refleja su nivel de complejidad y detalle.

Aunque el concepto de fractal es relativamente moderno, muchas de estas estructuras ya eran estudiadas en matemáticas desde principios del siglo XX. Los métodos para medir su complejidad, como la dimensión fractal, surgieron dentro del desarrollo de la teoría de la medida.

En la graficación 2D, los fractales son muy importantes porque permiten generar imágenes complejas y detalladas mediante algoritmos matemáticos. Se utilizan para representar fenómenos naturales como montañas, nubes, costas o plantas, ya que muchas de estas formas presentan comportamientos similares a los fractales.


## 2.5. Uso y creación de fuentes de texto.

Las fuentes de texto, también conocidas como tipografías, son un elemento fundamental en la representación gráfica, ya que permiten comunicar información de manera visual, clara y estética. En la graficación bidimensional, las fuentes no solo cumplen una función informativa, sino también visual, ya que influyen en la apariencia, el estilo y la legibilidad de los contenidos. La correcta elección de una tipografía puede mejorar significativamente la comprensión del mensaje y la experiencia del usuario.

El uso de fuentes de texto es esencial en diversas áreas como el diseño gráfico, las interfaces de usuario, los videojuegos y las aplicaciones digitales. A través de ellas, es posible organizar la información, resaltar elementos importantes y transmitir diferentes estilos visuales, como formalidad, modernidad o creatividad. Además, factores como el tamaño, el grosor, el espaciado y el contraste de las letras son determinantes para garantizar una adecuada legibilidad, especialmente en medios digitales.

Por otro lado, la creación de fuentes de texto es un proceso que combina principios de diseño gráfico con fundamentos matemáticos. En la actualidad, las tipografías digitales se construyen principalmente mediante gráficos vectoriales, lo que permite que puedan escalarse a distintos tamaños sin perder calidad. Cada carácter se diseña a partir de líneas y curvas, comúnmente utilizando curvas de Bézier, las cuales permiten definir formas suaves y precisas mediante el uso de puntos de control.

Durante el proceso de creación, se diseñan individualmente los caracteres, cuidando aspectos como la proporción, el equilibrio visual y la coherencia del estilo. También se consideran elementos como el espaciado entre letras, conocido como interletraje o kerning, que influye directamente en la legibilidad del texto. Una vez diseñados, los caracteres se digitalizan y se almacenan en formatos como TrueType u OpenType, los cuales permiten su uso en diferentes sistemas y aplicaciones.

En la graficación 2D, las fuentes de texto tienen una gran importancia, ya que pueden integrarse fácilmente en composiciones visuales y ser transformadas mediante operaciones como escalado, rotación o traslación sin perder calidad. Esto se debe a su naturaleza vectorial, que las hace altamente adaptables a distintos contextos y dispositivos.

## Bibliografías 

Sign in - Google Accounts. (s. f.). https://classroom.google.com/u/1/c/ODQxMTczMTY4MTE1/a/ODU4NTM2NTMwNjc2/details

Salazar, H. (s. f.). Graficacion Unidad II. Buap. https://www.cs.buap.mx/~hilario_sm/slide/graficacion/Unidad-II.pdf

Martinez, P. (2025, 3 marzo). Transformación Bidimensional. Prezi. https://prezi.com/p/rvfqhafuenzp/transformacion-bidimensional/

Graficación2D-transformaciones bidimensionales. (s. f.). Slideshare. https://www.slideshare.net/slideshow/graficacion2d-transformaciones-bidimensionales/271921986

Unidad II. (2012, 14 diciembre). Graficación. https://smoke5284.wordpress.com/unidad-ii/

Coob, S. (2019, 22 noviembre). Transformaciones Bidimensionales y Sesgado. Scribd. https://www.scribd.com/document/438661564/Transformaciones-Bidimencionales-docx


Valdes, A. S. (2013b, septiembre 24). 2.4 Representación matricial. https://graficacionito.blogspot.com/2013/09/24-representacion-matricial.html

Tepole, A. C. (2025, 18 septiembre). Trazado de Líneas Curvas: Bézier y B-spline. Prezi. https://prezi.com/p/s8ll8r8m3tir/trazado-de-lineas-curvas-bezier-y-b-spline/

Unknown. (s. f.-a). Curvas de Bézier. https://oscarhumbertoramirezcruzgraficacion.blogspot.com/2017/11/curvas-de-bezier.html

Curvas B-spline. (s. f.). (C) Copyright 2017. https://docs.bentley.com/LiveContent/web/MicroStation%20Help-v26/es/GUID-E54007AE-BB6E-55AA-A09C-A1F5E39A58A5.html

Fractales. (s. f.). https://fernandez-torres-jose.blogspot.com/2012/08/fractales.html?m=1












