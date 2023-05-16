Para aplicar estilos, se hace el llamado de lo que se le quiere poner el estilo, por ejemplo, un párrafo y todo el estilo que se le aplica, va entre {}:
p{
}

Se utilizan sets de valores que se conocen como llave y valor, llave es propiedad, por ejemplo, color y lleva dos puntos, ejemplo color:blue; y termina con punto y coma.

Para aplicar estilos, no es necesario memorizarlos todos. Solo se buscaría la propiedad (o el estilo), cuando se requiera.

Como CSS son hojas de estilos en cascada, si repetimos propiedad, el va a tomar la última que se aplique. 

Las propiedades se pueden colocar todas en una sola línea, si se quiere, aunque se ve mejor en cascada.

Para cargar estilos, se debe llamar el archivo css dentro de html, con la etiqueta <link>, no tiene cierre. Se coloca en el head. Luego es necesario colocar rel=stylesheets, para que entienda que esta referenciando una hoja de estilos.

Para que cargue rápido la hoja de estilos, se coloca antes de referenciar el archivo css la siguiente ruta: <link rel="preload" href="css/styles.css" as="style">

Para cambiar estilos de una palabra del h1, se puede utilizar la etiqueta <span><span/>.

Hay diferentes tamaños para las letras. Unos son los pixeles (ya no son tan recomendados), otro se llama rem y otro enm (el enm duplica el valor del tamaño que se tenga antes, para que el tamaño coincida, al segundo enm se le debe colocar la mitad del primer enm)

Los rem son los más utilizados y para evitar usar todo el tiempo la calculadora de rems, hay un codigo que se coloca en css que es el siguiente:
html
{
    font-size:62.5%
}
body
{
    font-size:16px
    }
Esto optimiza que se pueda ver en cualquier pantalla.
Un rem equivale a 10 px

Importante ver el tema de selectores que está en las diapositivas del curso, video # 24

Las clases permiten optimizar el código, se escriben en html. Se escriben por ejemplo class="titulo" y al llamarlas en css se escribiría .titulo

Si los selectores son iguales, tomará el ultimo estilo.
La especificidad es cuando el navegador selecciona el estilo que tiene mayor grado de importancia. El important es el más importante de todos pero no se recomienda mucho usarlo. Video 25

#Colores
:seudo selector que se coloca en css. Se indica con :root{} y permite almacenar variables de css. Se llaman también custom properties y es útil para paletas de colores.

Se crea en el root las paletas de colores y cuando se llaman en el determinado estilo, se llaman las variables. ej var(--primario).

Cambiar el tipo de fuente: propiedad font-family.
Una buena página para fuentes es Google Fonts, que proporciona el código de la fuente.
#OJO
Importante la especificidad al cargar los links, por ejemplo, en el caso de la fuente, debe cargarse primero este link antes de los demás links.

margin: posición en la que se va a cargar un elemento
margin-top: 0; /*margen hacia arriba*/
    margin-right: auto; /*margen derecha*/
    margin-bottom: 0; /*margen hacia abajo*/
    margin-left: auto; /*margen izquierda*/
margin permite optimizar codigo, colocando los 4 atributos en el sentido del reloj, es decir, quedaria arriba, derecha, abajo e izquierda
inclusive se puede optimizar mas el código, cuando los dos primeros valores se repiten, en el mismo orden, por ejemplo si tengo 0 auto 0 auto, solo lo dejo 0 auto y ya, css entiende que los dos primeros son arriba y abajo y luego derecha e izquierda. asi pasa cuando hay un solo rem.
justify-content: permite mover el contenido horizontalmente.
margin es del limite del elemento hacia afuera, con el elemento que tenga mas cercano, dependiendo de la direccion que se le indique.
padding es ayudar a "engordar" el elemento, hacerlo un poco mas alto, lo hace hacia adentro.

text= modificaciones a la fuente
font= cambiar la fuente

flexbox se usa desde el elemento padre. Sirve para alinear de forma horizontal, como por ejemplo, una navegación. primero se coloca display flex para activar display flexbox que permite modificar horizontalmente
distribuir el contenido, se inicia con la propiedad space

Experiencia de usuario con responsive, que utiliza media queries para que se adapten al tamaño de cada pantalla.

480 px = Móvil
780 px = Tablet
1140 px= Laptop y PC escritorio
1400 px= Gamer

agregar imágenes desde css con la propiedad background-image

background-image: url(../images/hero.jpg); Para colocarla con dirección
    background-repeat: no-repeat; Para que no se repita la imagen
    background-size: cover; para que cubra toda la pantalla y no quede cortada

    #display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;# El anterior código sirve para centrar todo un contenido.

    Para hacer un degradé, con la palabra to y la dirección (top, right, left, etc).

    Estas tres lineas de código, hacen lo mismo:
    /*grid-template-columns:*repeat(3, 1fr)
    /*grid-template-columns: 1fr, 1fr, 1fr; 
    /*grid-template-columns: 33.3% 33.3% 33.3%;*/

    CSS grid permite alinear elementos en columnas y filas. Flex box solo permite columnas.

flexbox= para elementos que estan dentro de contenedores
css grid= para distribuir diferentes areas de la web

