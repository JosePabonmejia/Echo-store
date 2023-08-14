# Curso de Fundamentos de Sass: Crea tu Primera Landing Page 

## Características de SASS


* Modularización: Permite dividir los estilos en módulos más pequeños y manejables para simplificar el proceso de desarrollo y mantenimiento.
.
* Variables: Permite definir variables para almacenar valores reutilizables en un archivo SASS, lo que facilita la creación y el mantenimiento de hojas de estilo.
.
* Mixins: Permite definir mixins, que son bloques de código reutilizables que se pueden incluir en diferentes partes del CSS. Los mixins pueden contener variables y lógica, lo que facilita la creación de estilos más complejos y dinámicos.
.
* Selectores Anidados: Se pueden anidar selectores y reglas de estilo, lo que ayuda a organizar y estructurar el CSS de manera más intuitiva.
.
* Herencia: SASS permite la herencia de estilos entre selectores, lo que puede simplificar la creación y el mantenimiento de hojas de estilo.
.
* Funciones: Admite funciones que permiten realizar cálculos y operaciones complejas en el CSS. Las funciones se pueden utilizar para definir valores dinámicos, como la altura o el ancho de un elemento en función de otros valores.
.
* Importación: SASS admite la importación de archivos CSS y SASS, lo que facilita la organización y el mantenimiento de hojas de estilo.
.
* Directivas de control de flujo: SASS admite directivas de control de flujo, como if/else y for, que permiten realizar operaciones condicionales y repetitivas en el CSS.
.
* Operaciones aritméticas: SASS admite operaciones aritméticas, lo que permite realizar cálculos matemáticos directamente en el CSS.

## ¿Cómo funcionan los preprocesadores?

Un preprocesador es una herramienta que nos permite escribir pseudocódigo recibiendo como parámetro de entrada los estilos que posteriormente serán convertidos a CSS nativo. Podemos decir que funcionan de manera similar a los traductores pues al indicarle una sintaxis devuelve los valores en una sintaxis nueva.
En SASS se incluyen características adicionales, como variables, mixins, herencia de clases, entre otras, que hacen que el proceso de escritura de CSS sea más fácil y rápido.

Para poder hacer uso de un preprocesador, primero es necesario entender cómo funcionan los estilos CSS y el navegador. Los estilos CSS son interpretados y representados por el navegador, el cual se encarga de leer el código CSS y aplicarlo a los elementos o componentes HTML de la página. Es el navegador quien recorre la hoja de estilos, línea por línea, y asigna propiedades a los elementos de la página según lo indicado en el código CSS. Este proceso es fundamental para permitir que la página se estilice de la manera deseada, teniendo control sobre el diseño y la disposición de la página, proporcionando al usuario una experiencia visual atractiva, donde todos los elementos están estilizados y presentados de una manera agradable a la vista y fácil de interactuar.

## Ventajas de utilizar un Preprocesador

Los principales beneficios de usar un preprocesador como SASS son la rapidez y la productividad. Permitiendo que el código se pueda escribir de manera mucho más rápida y sencilla, ayudando a los desarrolladores a ahorrar tiempo y ser más productivos. También hacen que el mantenimiento del código sea más fácil, pues todos los estilos se guardan en un solo archivo. La reutilización de código es otro de los beneficios que nos trae el uso de un preprocesador, esto significa que los mismos estilos se pueden aplicar en varias páginas sin tener que escribir el código una y otra vez.
Finalmente el uso de preprocesadores nos permite que sea mucho más sencillo trabajar una página web de manera responsiva.

### Tipos de Preprocesadores

### Stylus

Stylus 
es un lenguaje de programación de hojas de estilo en cascada (CSS) que se compila en CSS estándar, está basado en JavaScript. Hay algunas diferencias importantes entre Stylus y SASS. La sintaxis de Stylus es más simple y clara, mientras que la sintaxis de SASS se considera más profesional y compleja. Stylus ofrece una mejor portabilidad y es más fácil de usar. Sin embargo, SASS ofrece mayor soporte al ser utilizado con una mayor cantidad de lenguajes de programación.

Conoce [Stylus](https://stylus-lang.com/)

### LESS
Una de las principales diferencias entre LESS y Sass es que Sass está codificado en Ruby y, por lo tanto, se procesa del lado del servidor, mientras que Less es una biblioteca de JavaScript (Como Stylus) y se procesa del lado del cliente. Un ejemplo es la forma en que ambos lenguajes manejan las variables es distinta. En LESS, los nombres de las variables se inicializan con @ y en Sass los nombres de las variables se inicializan con el símbolo $.

Conoce [LESS](https://lesscss.org/)


## El proceso de Compilado
.
Para hacer uso de SASS dentro de nuestro proyecto tenemos que tener en cuenta 3 puntos importantes que forman parte del proceso de compilación.
.

* ***Imput file (archivo de entrada):*** Es donde vamos a escribir nuestros estilos haciendo uso de la sintaxis de Sass, incluyendo la extensión .scss en el nombre del archivo.
.
* ***Output file (archivo de salida):*** Es donde se colocarán los estilos finales con CSS nativo, que provienen del archivo de entrada. (nunca se debe editar directamente el archivo de salida)
.
* ***Los comandos para ejecutar y compilar Sass:*** Hay varias formas de ejecutar y compilar Sass, cada una con sus propios comandos y herramientas. La elección del método dependerá del entorno de desarrollo y las preferencias personales del desarrollador.

## Estructura de la hoja de estilos y variables

Algunos statements contienen bloques y se definen entre un par de llaves { } , son separados mediante punto y coma ;

### Top-level statements
Son declaraciones que solo se pueden usar en la parte superior de la hoja de estilos

* Imports
* Definición de un Mixin
* Definición de una Función
* Módulos
### Universal statements
Son statements que podemos usar en cualquier parte de la hoja de estilos.

* Variables, estructuras de control y las reglas @error, @warn y @debug.
* Declaraciones CSS: Reglas de estilo, At-rules y Mixis.

### Variables
Es un espacio de memoria asignado en memoria y únicamente puede almacenar un dato.

* Las variables pueden ser declaradas en cualquier parte de la hoja de estilos.
Para asignar un valor a una variable se hace uso del simbolo $ de esta manera es posible referenciar dentro de la hoja de estilos.

***Ejemplo***

    $primary-color:#FFEFE7;
    $secundary-color:#FFDAC6;
    $tertiary-color:#BABD8D;
    $primary-text-color:#7C6A0A;
    $font-stack: 'IBM Plex Sans' , sans-serif;

    body{
        margin: 0;
        padding: 0;
    }

## Diferencias en Variables en CSS y SASS
<table>
    <thead>
        <tr>
            <th>CSS Variable</th>
            <th>Sass Variables</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                Pueden tener diferentes valores para distintos elementos
            </td>
            <td>
                Tienen un valor único correspondiente a un elemento
            </td>
        </tr>
        <tr>
            <td>Son declarativas</td>
            <td>Son imperativas (en el momento en el que actualicemos el valor de nuestra variables va a cambiar en automático)</td>
        </tr>
    </tbody>
</table>

### !default flag
Se encarga de asignar un valor a la variable si y solo si esa variable no esta definida o su valor en null.

#### Uso de selectores, scope de las variables y shadowing

El scope dentro de Sass hace referencia al contexto en el que son declaradas las variables y donde es posible hacer uso de las mismas, hay dos tipos de variables:
***Locales:***
* Declaradas dentro de un bloque { }
* Cualquier selector anidado puede acceder a las variables locales declaradas dentro del selector
***Globales***
* Todas las variables declaradas fuera de un selector son globales, esto significa que se puede acceder a ellas en cualquier parte de nuestra hoja de estilos.

***Shadowing:*** Las variables locales y globales pueden tener el mismo nombre ya que se encuentran en diferentes niveles del scope para evitar que se modificquen por error las variables globales.

***!global flag:*** Se usa en caso de querer modificar el valor global de una variable dentro del scope de una variable local.

## At Rules: CSS y nesting

* ***@use:*** importa, modulos estilos y funciones de otras hojas de estilos. la diferencia con @import es que import se encarga de hacer los estilos globales.
* ***@function:*** permite crear funciones personalizadas, sin embargo Sass cuenta con funciones ya existentes.
* ***@forward:*** Recibe como parametro una URL y nos ayuda a cargar los estilos de nuestra hoja de estilos, es muy importante hacer uso de @use para que los modulos esten disponibles en nuestra hoja de estilos.
* ***@extend:*** tiene que ver con el concepto de herencia.
* ***@at-root:*** se encarga de cargar nuestros estilos en el root del css.
* ***@include:*** nos ayuda a invocar los mixins.
* ***@error, @warn @debug:*** sirver para cuando hay un error, una advertencia o se quiere debugear, respectivamente
* ***@for, @if, @each, @while:*** tienen que ver con estructuras de control, se pueden usar dentro de una función