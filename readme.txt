El BOM (Browser Object Model) consiste en el navegador de objetos, el historial, la pantalla, la ubicación y el documento que son elementos secundarios de la ventana. 

En el nodo del documento está el DOM (Document Object Model), el modelo de objeto del documento, que representa el contenido de la página


****************************
*html
    * head
        * title
        * meta
    * body
        * header
            * nav
        * section
            * article
        * footer
***************************

Para ver todas las etiquetas se puede acceder al siguiente link:
https://allthetags.com/
http://html5doctor.com/

Algunas de las etiquetas más conocidas y usadas son:

    Etiquetas de cabecera (head)
        doctype: indica al navegador el tipo de documento que se está          mostrando.
        html: es la etiqueta que envuelve todo el documento
        head: El elemento head contiene documentos de metadata, como        links estaticos o titulos.
        meta: Metadata que no puede ser representada por otros              elementos de HTML.

    Etiquetas del cuerpo del documento (body):
        article: es la parte de nuestro contenido que puede             vivir por sí mismo. Pueden haber tantos                artícle como proyectos o eventos tenga                 nuestro portafolio.
        nav: Para hacer menús de navegación.
        aside: Contenido menos relevante, como publicidad, etc.
        section: Sirve para diferenciar las secciones principales del contenido.
        header: Cabecera del documento.
        footer: Pie de página del documento.
        h1 - h6: Títulos de nuestro sitio web. 
        table: Tablas de contenidos, similar a la estructura de las hojas de calculo.
        ul - ol:   Listas de items. Sin orden o ordenada.
        div: Cualquier división para organizar el contenido.
        a: corresponde a un ancla o enlace a una url interna o    externa del documento.
        img: con esta etiqueta podemos enlazar imágenes en el     documento.
        figure: le da un contexto semántico a las imágenes.
        hr: Divisor en horizontal. Cierra sola la etiqueta
        p: define el texto de un párrafo.
        small: aplica una apariencia de texto reducido en tamaño.
        strong: aplica al texto un formato de negritas.

Para link hay algunos atributos, en la cabecera head del documento:
        rel: indica la relación del recurso con el contenido.
        type: indica el tipo de recurso / formato.
        href: indica la ubicación (url) del recurso enlazado.

-/*/*--*/*-/**-/*-*-/*-*/-*-/*-/-*/**-/*/-*-/-*/-/*/*--*/*-/**-/*-*-

Hay tres opciones para incluir estilos que definan la apariencia de tu html:

    Estilos en línea: se definen directamente en el elemento html que quieres estilizar, se agregan con el atributo style.
    Estilos con el tag Style: regularmente este tag se incluye dentro de la etiqueta head del html.
    Estilos enlazados desde un archivo css externo: utilizando la etiqueta link que nos permite enlazar recursos externos.

A CSS, se le llama hojas de estilos en cascada porque los estilos que se definen para una página, se van aplicando de arriba hacia abajo, y de lo más general a lo más particular, teniendo prioridad lo más particular. Esto es, los estilos que prevalecen son los que han sido definidos en línea, luego los que fueron definidos mediante la etiqueta style en la cabeza o cuerpo del html, y por último los estilos definidos en archivos externos enlazados con la etiqueta link. Esta prioridad se puede alterar al usar el modificador **!important"" en la definición de algún estilo en particular, aunque esto no es recomendado.

-/*/*--*/*-/**-/*-*-/*-*/-*-/*-/-*/**-/*/-*-/-*/-/*/*--*/*-/**-/*-*-

Unidades de medida y colores

Hay varias unidades de medida con las que se puede trabajar en CSS: %, em, rem, px, pt, fr, vw, vh
Las medidas más comunes y utilizadas son los pixeles. Un pixel es la menor unidad homogénea en color que forma parte de una imagen digital. Es la unidad más práctica y fácil de utilizar y manipular, y es la que utilizaremos mayormente en este curso.

Los colores en CSS pueden ser representados de al menos tres formas diferentes:

    Representados con palabras claves para cada color, como: red, green, blue, pink, yellow, black, etc.
    Usando la composición de tres colores (rojo, verde y azul): para esto podemos usar notación exadecimal o las funciones rgb() y rgba().
    Usando la composición mediante valores de Matiz, Saturación y Luminosidad con: hls() y hlsa().

Con respecto a los valores hexadecimales, cada color está representado por 6 digitos, que representan 3 pares de hexadecimales: FF - FF - FF (rojo, verde y azul), en el que cada par puede tomar valores hexadecimales entre 00 y FF. Cada uno equivale a valores decimales entre 0 y 255, donde 0 es la ausencia de ese color y 255 la mayor cantidad disponible. De esta manera cada color se forma por la combinación de diferentes proporciones de rojo, verde y azul.

    #000000 es equivalente a Negro
    #FF0000 es equivalente a Rojo
    #00FF00 es equivalente a Verde
    #0000FF es equivalente a Azul
    #FFFFFF es equivalente a Blanco

-/*/*--*/*-/**-/*-*-/*-*/-*-/*-/-*/**-/*/-*-/-*/-/*/*-

line-height para modificar el alto de linea
font-size para modificar el tamaño de la fuente
font-weight para modificar el tipo de fuente
font-style para modificar el estilo de la fuente
letter-spacing para modificar el espacio entre letras
text-transform para transformar la fuente (mayusculas, minuculas, etc)
text-decoration para moodificar la decoración de la fuente

-/*/*--*/*-/**-/*-*-/*-*/-*-/*-/-*/**-/*/-*-/-*/-/*/*-

Rellenos

Así como el margen separa a los elementos html entre sí, la propiedad padding de relleno, permite definir una separación entre el contenido interno y el borde de un elemento.

Al inspeccionar los elementos html en el navegador, se puede apreciar el margin con color naranja y el padding con color verde.

Una forma de identificar cuándo es mejor usar margin o padding en un elemento, es evaluando la necesidad de usar borde o background, ya que son éstos: el borde y el background, los que realmente diferencian el uso de uno u otro.

-/*/*--*/*-/**-/*-*-/*-*/-*-/*-/-*/**-/*/-*-/-*/-/*/*-

Modelo de caja

El modelo de caja es un concepto teórico de css que representa a cada elemento html en base sus propiedades de: margin, border, padding y dimensiones (alto y ancho).
Para visualizar un elemento html en su representación como modelo de caja debemos irnos a la parte baja de la sección styles del inspector de elementos, o en la sección llamada Computed.

En el modelo de caja, el ancho total de un elemento html equivale a la sumatoria de los valores de: width, padding-left, padding-right, border-left-width, border-right-width. De manera similar aplica para el alto total de cada elemento. Aunque margin-left y margin-right, forman parte del modelo de caja, no se incluyen para el calculo del ancho total.

Con la propiedad box-sizing, y en particular con el valor border-box de esta propiedad, podemos modificar el comportamiento del modelo de caja para que nuestro elemento nunca supere el tamaño máximo que le hayamos definido en width y height. Esta es la opción recomendad para trabajar.

-/*/*--*/*-/**-/*-*-/*-*/-*-/*-/-*/**-/*/-*-/-*/-/*/*-

Propiedades de flexbox

Flexbox se refiere al tipo de display en css que permite un manejo flexible de la alineación, dimensionamiento y distribución de elementos html.

Esta propiedad se aplica a un elemento padre, pero va a afectar principalmente a sus elementos hijos directos. Por defecto, los elementos internos quedan alineados unos seguidos de los otros. El comportamiento del modelo de caja de estos elementos hijos también se ha modificado, ya que pierden el efecto de su propiedad margin.

Los elementos hijos de un padre con propiedad display: flex tienen a su disposición algunas nuevas propiedades que aportan mayor flexibilidad a su comportamiento. Una de estas propiedades es flex-shrink que, junto a la propiedad flex-wrap del padre, permite adaptar y distribuir los elementos de manera dinámica en el espacio horizontal disponible hasta ocupar todo el espacio, y luego pasar a ocupar dinamicamente las siguiente filas hacia abajo.

-/*/*--*/*-/**-/*-*-/*-*/-*-/*-/-*/**-/*/-*-/-*/-/*/*-

