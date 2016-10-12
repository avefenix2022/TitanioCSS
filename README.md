# Nuestro Framework Titanio CSS

Nos basamos en el framework Skeleton: [getskeleton.com](http://getskeleton.com). Con una anchura para el contenido de **960px**.

Por media queries:

*   por debajo de **550px** se apila el contenido, con una anchura del contenido del **100%**,
*   entre **400 y 500px** esta anchura es del **85%** ,
*   y por encima de los **550px** del **80%**.

Las guías de estilo se deben:

*   comprender,
*   aprender, y
*   aplicar siempre

y cualquier desviación debe ser justificada.

<small>(Basada en [http://cssguidelin.es/)](http://cssguidelin.es/)</small>

## Sintaxis y formato del documento

**El código debe de ser y parecer limpio**

## Reglas

*   **(4) espacios** para indentar, no tabular.
*   Columna de **80 caracteres** de ancho.
*   CSS multilínea.
*   **Orden alfabético.**
*   Una columna para la propiedad y otra para el valor.
*   Uso de espacios en blanco para facilitar la lectura.

<pre>      
.baz {
    background-color:      green;
    color:                 red;
    display:               block;
}
     </pre>

## Varios archivos Css

Es una buena idea dividir trozos discretos de código css en archivos independientes para posteriormente procesarlos y concatenarlos en un archivo único.

## Tabla de contenido

Una tabla de contenidos marca un esqueleto sobre el que apoyar la estructura del documento.

<pre>         
/**

* TABLA DE CONTENIDO
*
* AJUSTES
* Global ................. Variables y configuraciones disponibles Globalmente.
* Tipografías
* Estilos Base
*
* HERRAMIENTAS
* Mixins ................. Mixins útiles.
*
* GENÉRICO
* Normalize.css .......... Normalize.
* Box-sizing ............. Box-sizing.
*
* BASE
* Encabezamientos ........ H1-H6.
*
* OBJETOS
* Contenedores ........... Contenedores.
* Grid ................... Regilla de maquetación de 12 columnas
*
* COMPONENTES
* Cabecera de las Página . Encabezado principal de la página.
* Pies de las Página ..... El pie de página.
* Botones ................ Elementos Button.
* Links .................. Etiquetas a.
* Forms .................. Formularios.
* Lists .................. Listas ordenadas y no ordenadas.
* Code ................... Etiqueta pre y code.
* Tables ................. Estilos de tablas.
* Spacing ................ Separaciones y espacios.
* Utilities .............. Diferentes utilidades.
* Clearing ............... Para limpiar float.
* 
* MEDIA QUERIES
*
* Para menores de 400px */
* ...
*
* Mayor que Móviles de 400px */
* @media (min-width: 400px) {}
*
* Mayor que Phablet de 550px (También el punto cuando empieza a activarse el grid) */
* @media (min-width: 550px) {}
*
* Mayor que Tablet */
* @media (min-width: 750px) {}
*
* Mayor que Ordenador */
* @media (min-width: 1000px) {}
*
* Mayor que Ordenadorp HD */
* @media (min-width: 1200px) {}

**/
     </pre>

## Ancho de 80 caracteres

Siempre que sea posible, la anchura de los archivos css se limitará a 80 caracteres. Las razones para esto incluyen:

*   Capacidad para abrir varios documentos uno al lado del otro.
*   Visualizar los archivos css en sitios como GitHub y ventanas de terminal.
*   Proporcionar una longitud de línea cómoda para comentarios.

<pre>         
/ **
* Este es el tamaño de un comentario con una longitud de 80 catacteres de ancho.
*
* Lorem ipsum dolor sit amet, consectetur adipisicing elit. Numquam dignissimos 
* facilis eveniet, incidunt voluptatem sit soluta maiores qui ducimus blanditiis
* impedit autem dolorum, cum veritatis ratione ut. Debitis, hic repellendus.
** /
     </pre>

## Títulos

**Comenzar cada nueva sección principal con un título**

<pre>         
/*------------------------------------*\
    #SECTION-TITLE
\*------------------------------------*/

.selector {}
     </pre>

El título de la sección está **precedido de un símbolo de almohadilla (#) que nos permita realizar búsquedas más específicas**. En lugar de buscar simplemente SECCIÓN-TITULO que pueden producir muchos resultados que una búsqueda más restringida de **#SECCIÓN-TÍTULO** la cual debería devolver solo la sección en cuestión.

**Dejar un retorno de carro entre este título y la siguiente línea de código.**

Si está trabajando en un proyecto en el que cada sección es su propio archivo, este título debería aparecer en la parte superior de cada uno de ellos. Si está trabajando en un proyecto con varias secciones por archivo, **cada título debe ir precedido de cinco (5) retornos de carro**. Este espacio en blanco adicional junto con un título hace que las nuevas secciones sean mucho más fácil de detectar cuando uno se desplaza a través de archivos de gran tamaño:

<pre>     
/*------------------------------------*\
    #A-SECTION
\*------------------------------------*/

.selector {}
1
2
3
4
5
/*------------------------------------*\
    #ANOTHER-SECTION
\*------------------------------------*/

/**
 * Comment
 */

.another-selector {}
     </pre>

## Anatomía de un conjunto de reglas

Antes de discutir la forma en que escribimos conjuntos de reglas, primero vamos a familiarizarnos con la **terminología**:

<pre>      
[selector] {
    [propiedad]: [valor];
    [<--declaracion--->]
}
      </pre>

Por ejemplo:

<pre>    
.foo, .foo--bar, 
.baz {
    display:               block;
    background-color:      green;
    color:                 red;
}
      </pre>

*   Selectores relacionados en la misma línea; no relacionados en nuevas líneas.
*   Un espacio antes de abrir unas llaves ' {'
*   Propiedades y valores en la misma línea.
*   Al menos un espacio después de lo dos punto (:)
*   Propiedades y valores en dos columnas.
*   Cada declaración en una nueva línea.
*   La llave de apertura ({) en la misma línea que el último selector.
*   La primera declaración en una nueva línea después de nuestra llave de apertura ({)
*   La llave de cierre (}) en su propia línea nueva.
*   la sangría de cada declaración con **cuatro (4)** espacios;
*   Un punto y coma (;) al fina de nuestra última declaración (aunque no sea obligatoria).
*   Los valores **siempre con unidades** incluso los de valor '0'.

## CSS Multi-línea

El CSS debe ser escrito en **múltiples líneas**, excepto en circunstancias muy específicas.  
**Hay ventajas para esto, como con conjuntos de reglas similares, que solo llevan una declaración, por ejemplo**:

<pre>
.icon {
    display: inline-block;
    width:  16px;
    height: 16px;
    background-image: url(/img/sprite.svg);
}

.icon--home     { background-position:   0     0  ; }
.icon--person   { background-position: -16px   0  ; }
.icon--files    { background-position:   0   -16px; }
.icon--settings { background-position: -16px -16px; }
      </pre>

**Cuando la presentación en una sola línea proporciona mejor la información por simplicidad y comparación se puede codificar en una sola línea.**

## Sangría

Se pueden sangrar selectores con sus declaraciones para indicar relaciones entre ellos:

<pre>          
.foo {}

    .foo__bar {}

        .foo__baz {}
      </pre>

De esta manera, un desarrollador puede ver a simple vista que `.foo__baz {}` vive en el interior de `.foo__bar {}` y este vive dentro `.foo {}`.

Esta cuasi-replicación del DOM le dice a los desarrolladores mucho acerca de donde se espera que las clases van a ser utilizadas sin que tengan que hacer referencia a un fragmento de código HTML.

## Sangría Sass

Sass proporciona una funcionalidad de anidación (**nesting**), como esta:

<pre>
.foo {
    color: red;

    .bar {
        color: blue;
    }

}
      </pre>

Que se compilará a:

<pre>          
.foo { color: red; }
.foo .bar { color: blue; }
      </pre>

Cuando sangramos en Sass, nos ceñimos a los mismos cuatro (4) espacios, y también dejar una línea en blanco antes y después del conjunto de reglas anidadas.

**La anidación en Sass debe evitarse siempre que sea posible, por especificidad!**

## Alinear

Intentar alinear cadenas idénticas y relacionadas en las declaraciones, por ejemplo:

<pre>          
.foo {
    -webkit-border-radius: 3px;
       -moz-border-radius: 3px;
            border-radius: 3px;
}

.bar {
    position:              absolute;
    top:                   0;
    right:                 0;
    bottom:                0;
    left:                  0;
    margin-right:          -10px;
    margin-left:          -10px;
    padding-right:        10px;
    padding-left:         10px;
}
      </pre>

## Significado de los espacios en blanco

Podemos proporcionar una gran cantidad de información mediante el uso libre y juicioso de espacios en blanco entre los conjuntos de reglas.  
Utilizamos:

*   **Una (1)** línea vacía entre los conjuntos de reglas estrechamente relacionados.
*   **Dos (2)** líneas vacías entre los conjuntos de reglas vagamente relacionados.
*   **Cinco (5)** líneas vacías entre secciones.

Por ejemplo:

<pre>          
/*------------------------------------*\
    #FOO
\*------------------------------------*/

.foo {}

    .foo__bar {}

.foo--baz {}

/*------------------------------------*\
    #BAR
\*------------------------------------*/

.bar {}

    .bar__baz {}

    .bar__foo {}
      </pre>

## Marcado HTML

Con los **atributos**:

<pre>        
<div class="box">
      </pre>

Al escribir varios valores en un atributo de clase, hay que separarlos con **dos (2)** espacios:

<pre>        
<div class="foo  bar">
      </pre>

Cuando hay **varias clases que están relacionadas entre sí, podrá agruparlas entre corchetes ([ y ])**, así:

<pre>          
<div class="[ box  box--highlight ]  [ bio  bio--long ]">
      </pre>

[Leer más+](http://csswizardry.com/2014/05/grouping-related-classes-in-your-markup/)

Al igual que con nuestros conjuntos de reglas CSS, es posible utilizar los espacios en blanco de forma significativa en el código HTML. Puede denotar **descansos temáticos en el contenido** con **cinco (5)** líneas vacías, por ejemplo:

<pre>         
<header class="page-head">
    ...
</header>

<main class="page-content">
    ...
</main>

<footer class="page-foot">
    ...
</footer>
      </pre>

Para **fragmentos independientes**, pero vagamente relacionados el marcado es con **una sola línea** en blanco, por ejemplo:

<pre>          
<ul class="primary-nav">

    <li class="primary-nav__item">
        <a href="/" class="primary-nav__link">Home</a>
    </li>

    <li class="primary-nav__item  primary-nav__trigger">
        <a href="/about" class="primary-nav__link">About</a>

        <ul class="primary-nav__sub-nav">
            <li><a href="/about/products">Products</a></li>
            <li><a href="/about/company">Company</a></li>
        </ul>

    </li>

    <li class="primary-nav__item">
        <a href="/contact" class="primary-nav__link">Contact</a>
    </li>

</ul>
      </pre>

Esto permite a los desarrolladores detectar **partes separadas del DOM de un vistazo**.

## Comentarios

La sobrecarga cognitiva de trabajar con CSS es enorme. Con tantos matices que dificulta ser consciente de todos, y más de los específicos de cada proyecto, la peor situación que la mayoría de los desarrolladores se encuentran es que no son la persona que escribió el código. Estas pueden recordar sus propias clases, reglas,... que es manejable hasta cierto punto, pero cualquier persona que hereda CSS apenas tiene posibilidades.

El CSS necesita más comentarios.

Como regla general, se debe comentar cualquier cosa que no sea evidente a partir solo del código. Es decir, no hay necesidad de decirle a alguien que color: red; colorea la fuente de rojo, pero si se está utilizando overflow: hidden; para borrar los desbordamientos -en contraste con un elemento con desbordamiento, esto es probablemente algo que vale la pena documentar.

Para grandes comentarios que documentan secciones o componentes enteros, usamos un comentario de varias líneas de ancho de **80** columnas. Por ejemplo:

<pre>          
/**
 * La cabecera de la página principal tiene dos estados:
 *
 * 1) Cabecera de la página normal sin imagenes de fondo. Solo contiene el logo
 * y el menu de navegación.
 * 2) Cabecera de la página con imagen de fondo cover y etiquetas de cabecera.
 *
 */
      </pre>

Este nivel de detalle debería ser la norma para todas las descripciones de códigos.

## Extensión de reglas

Cuando trabajamos con el patrón OOCSS, con reglas que pueden estar relacionadas incluso en archivos diferentes se deben de indicar estas extensiones.

En el archivo del objeto:

<pre>        
/**
 * Extiende `.btn {}` en _components.buttons.scss.
 */

.btn {}
      </pre>

Y en el archivo del Tema:

<pre>          
/**
 * Estas reglas extienden `.btn {}` en _objects.buttons.scss.
 */

.btn--positive {}

.btn--negative {}
      </pre>

La existencia de este sencillo comentario que requiere poco esfuerzo, puede proporcionar una ventaja para los desarrolladores que desconocen de dónde heredan los estilos.

## Comentarios del preprocesador

Con la mayoría, si no todos lo pre-procesadores, tenemos la opción de escribir comentarios que no serán compilados a nuestro fichero CSS resultante. Como regla general, se debe de usar estos comentarios para documentar código que afecte al archivo precompilado y que no va a aparecer escrito en el archivo CSS porque allí no se aplica. Si se está documentando código que se compila, utilizar los comentarios que se compilará también. Por ejemplo, esto es correcto:

<pre>          
// Dimensiones de imágnes @2x:
$sprite-width:  920px;
$sprite-height: 212px;

/**
 * 1\. Tamaño por defecto de icono 16px.
 * 2\. Retina sprite se muestra en el tamaño correcto.
 */
.sprite {
    width:  16px; /* [1] */
    height: 16px; /* [1] */
    background-image: url(/img/sprites/main.png);
    background-size: ($sprite-width / 2 ) ($sprite-height / 2); /* [2] */
}
      </pre>

Hemos comentado las variables, las cuales no se muestran en nuestro archivo CSS junto con estos comentarios, mientras que nuestro código CSS que se compila en el archivo CSS se documenta el uso final del CSS compilado con comentarios. Esto significa que sólo tenemos la información correcta y relevante a nuestra disposición al depurar nuestras hojas de estilo compiladas.

## Eliminar comentarios

No hace falta decir que en el **entorno de producción** no deben de aparecer estos comentarios. **Todos los CSS deben de ser minificados** lo que conlleva la pérdida de estos comentarios antes de ser desplegados los archivos.
