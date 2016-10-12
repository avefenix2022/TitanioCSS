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
