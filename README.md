# Fundamentos de HTML

HTML es un lenguaje de marcado y es usado para decirle al navegador que desplegar al visitar una página web. Consiste en una serie de etiquetas que representan elementos que usas para _marcar_ diferentes partes del contenido, dicho de otra manera, las etiquetas son los bloques que conforman u página web.
Una página web es una serie de elementos HTML anidados.

## Versiones de HTML

| Versión | Año |
| --- | --- |
| HTML | 1991 |
| HTML 2.0 | 1995 |
| HTML 3.0 | 1997 |
| HTML 4.0 | 1999 |
| XHTML | 2000 |
| HTML5 | 2014 |


## Estructura básica de un documento HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Dentro de esta etiqueta se encuentran meta datos del documento en si-->
  </head>
  <body>
    <!-- Etiquetas que definen el contenido que el usuario verá-->
  </body>
</html> 
```

![Estrucutura HTML versión gráfica](http://images.slideplayer.com/25/8067990/slides/slide_8.jpg)

## Composición de una etiqueta HTML

La composición general de una etiqueta se da de la siguiente manera:

```html
<etiqueta atributo1="valor1" atributo2="valor2">Contenido</etiqueta>
```

![](https://mdn.mozillademos.org/files/11913/htmlexp.png)

Aunque para algunos elementos, llamados _elementos vacíos_, la composición cambia a:

```html
<etiqueta atributo1="valor1" atributo2="valor2">
```

Como podrán observar la etiqueta no tiene cierre, esto es por que no _encapsula_ ningún contenido.

### Tipo de elementos de marcado

1. Elementos de marcado de estructura: Indican el propósito del contenido. Estos elementos no denotan ningún render en especial. Ejemplo \<h2>Subtítulo\</h2>.
2. Elementos de marcado de presentación: Indican la apariencia del contenido sin importar el contenido en si mismo. Ejemplo \<b>Hola Mundo\</b>.
3. Elementos de marcado de hipertexto: Indican partes de un documento que se dirigen a otros documentos. Ejemplo, \<a href="https:www.google.com">Google\</a>.

### Atributos

La mayoría de los atributos son pares nombrados separados por un signo de =. Añaden información adicional a los elementos HTML, siempre son colocados en la etiqueta de apretura. Los atributos más usados son los siguientes:

* id: Define un identificador único para el elemento dentro del documento HTML.
* class: Provee una forma de clasificar elementos.
* href: usado en la etiqueta _a_ para definir un enlace a otro documento.
* src: usado en la etiqueta _img_ para definir la ruta de la imagen a utilizar.
* disabled: especifica que un elemento está deshabilitado.

![](https://mdn.mozillademos.org/files/11915/htmlatributos.png)

## Etiquetas

![](https://html.com/wp-content/uploads/html5_cheat_sheet_tags.png)

### Etiquetas descontinuadas

|Etiqueta | Descripción |
|--- | ---|
|\<acronym> | Define un acrónimo|
|\<applet> | Define un applet |
|\<basefont> | Define un fuente base para la página |
|\<big> | Define texto grande |
|\<center> | Define texto centrado |
|\<dir> | Define una lista de un directorio |
|\<font> | Define text font, size, and color |
|\<frame> | Define un frame |
|\<frameset> | Define un conjunto de frames |
|\<isindex> | Define un campo input |
|\<noframes> | Define una sección no frame |

### Etiquetas activas

#### Etiqueta _head_

El elemento _head_ es un contenedor para los metadatos. Los metadatos no son desplegados el usuario. Las etiquetas siguientes definen metadatos:

| Etiqueta| Descripción |
|--- | ---|
| title| Indica el título del documento.Sus etiquetas son: \<title> y \</title> (ambas obligatorias). Crea una caja: Está definido como: Elemento de contenido de cabecera.|
| style | Es el elemento encargado de indicar la información de estilos. |
| meta |Son tipicamente usados para especificar la descripcion de la pagina, teclado , autor del documento, ultima modificacion y otros metadatos,los metadatos no seran mostrados en la pagina, pero la maquina lo analiza|
| link | Permite realizar la carga y establecer la relacion existente entre el documento web actual y un recurso externo.Esta etiqueta es normalmente utilizada para realizar la carga de hojas de estilos para el documento web. |
| script| El elemento HTML _script_ se utiliza para insertar o hacer referencia a un script ejecutable dentro de un documento HTML o XHTML.|
| base | Especifica la dirección URL base que se utilizará para todas las direcciones URL relativas contenidas dentro de un documento. Sólo puede haber un elemento \<base> en un documento.|


#### Encabezados

* \<h1>Encabezado 1\</h1>
* \<h2>Encabezado 2\</h2>
* \<h3>Encabezado 3\</h3>
* \<h4>Encabezado 4\</h4>
* \<h5>Encabezado 5\</h5>
* \<h6>Encabezado 6\</h6>

Los motores de búsqueda usan los encabezados para indexar la estructura y contenido de tu página web. Para aplicar estilos a los encabezados usa CSS.

#### Párrafos

* \<p>Define un párrafo\</p>
* \<br> Inserts a single line break
* \<pre>Define un texto preformateado\</pre>

#### Etiquetas para definir secciones de contenido

* _div_
* _section_
* _footer_
* _header_

#### Etiquetas para definir elementos multimedia

* _img_
* _audio_
* _video_
* _canvas_
* _svg_

#### Etiquetas para formulario

* _form_
* _label_
* _input_

##### Form

El elemento _form_ que define un formulario puede tener atributos entre los que destacan:

* _action_: Define la acción a realizar cuando el formulario sea enviado. Si el atributo no es definido entonces la acción se establece a la página actual.
* _target_: Especifica si el resultado enviado debe de abrirse en una nueva página o en la página actual.
* _method_: Especifica el método HTTP que será usado para enviar los datos del formulario.

> * El método por default es GET, sin embargo cuando este método es usado los datos del formulario son visibles en la barra de dirección.
> * La longitud máxima de una URL es de 300 caracteres.
> * Nunca uses GET para datos sensibles.
> * GET es bueno para datos no sensibles, como los _query params_ en una búsqueda.

##### Label

El elemento label representa una etiqueta que puede ser asociada a un control de formulario, y que se supone provee una descripción corta para éste. Los navegadores pueden enlazar ambos elementos permitiendo que los usuarios establezcan el enfoque sobre el control al hacer clic en su etiqueta.

Existen dos formas de asociar a un elemento label con un control: insertando al texto de la etiqueta y al control dentro de label; o haciendo que coincidan los valores del atributo id en el control y del atributo for en label.

![Forma uno de asociar el label e input](images/label-input1.png)

![Forma dos de asociar el label e input](images/label-input2.png)

##### Input

> Para el método POST cada elemento _input_ debe de tener el atributo **name** respectivo, si no es así el dato del _input_ no séra enviado.

###### Tipos de elemento input

|Tipo | Descripción |
| --- | --- |
| button| Crea un botón en el que se puede hacer click sin ningún valor por defecto. |
| checkbox| Permite insertar un vector o arrray de valores. |
| color| Permite al usuario seleccionar un color.  |
| date| Permite al usuario proporcionar una fecha. |
| datetime| Permite ingresar hora y fecha (hora, minuto, segundo, fracción de segundo) basado en la zona horaria UTC. |
| datetime-local | Se escoge una fecha y hora sin la zona horaria  |
| email|el tipo de entrada tiene que ser un email |
| file|define un campo de archivo y lo selecciona y pone un boton para ver los archivos subidos|
| hidden|oculta un campo de entrada de datos al usuario aunque la informacion es enviada cuando el formulario es presentada  |
| image|el tipo de entrada es una imagen y envia coordenadas X y Y del clic que activo el boton de imagen|
| month|  En un atribtuo type, representa un campo para la entrada de un mes. En los navegadores que soportan el mecanismo, estos campos pueden estar representados por controles que permiten a los usuarios cambiar su valor de manera gráfica (como, por ejemplo, un calendario), en lugar de tener que ingresarlo directamente como una cadena.|
| number| Este elemento valida automáticamente que los valores introducidos sean numéricos sin necesidad de scripts adicionales, toda la validación la realiza el propio navegador|
| password|El buscador generará un campo para escribir, y cambiar la contraseña. Los datos que introduzca el usuario serán mostrardos como asteriscos, estos carácteres puede variar dependiendo del buscador. |
| radio|En un atributo type, representa una opción que pertenece a un grupo en el que no más de una opción puede ser seleccionada al mismo tiempo. Estos grupos están normalmente conformados por un número de botones de opción, todos compartiendo el mismo valor en el atributo name. |
| range| permite que el usuario especifique un valor numérico comprendido entre un valor mínimo y máximo. El valor exacto, sin embargo, no se considera importante. Se repesenta típicamente como un "tirador" o un control deslizante en lugar de un campo de texto como otros tipos de \<input>. Como este tipo de widget es bastante inmpreciso, no debe utilizarse normalmente a menos que el valor exacto del control no sea importante. |
| reset|Permite agregar un boton con la funcionalidad de limpiar cualquier formulario o valor asignado. |
| search|Permite agregar campos donde se podria recibir texto para busquedas. |
| submit| Permite agregar botones que al ser presionados intentan enviar los datos capturados en cualquier campo input hacia el servidor. |
| tel| Permite agregar un campo que valida que se hayan introducido caracteres numericos cuando se requiera solicitar un numero telefonico. |
| text| Permite crear campos simples para captura de texto. |
| time | Define el control para ingresar una hora (sin zona horaria)|
| url |Define un campo para ingresar una URL|
| week | Define un control de semana y año (sin zona horaria)|

## Atributos globales

https://www.w3schools.com/tags/ref_standardattributes.asp

## Atributos de eventos

https://www.w3schools.com/tags/ref_eventattributes.asp

## Maquetación WEB

La maquetación web es el proceso en el que el prototipo gráfico también denominado «layout» (con los requisitos estructurales y estéticos definidos y aprobados en un análisis inicial) pasa a transformase en código html, css y js (estándares web) para que los navegadores puedan interpretarlo correctamente.


# Fundamentos de CSS

## ¿Qué es CSS?

Cascading Style Sheets (CSS), traducido literalmente al español, como Hojas de estilo en cascada, es un lenguaje para especificar cómo los documentos se presentan a los usuarios.

CSS ayuda a mantener la información de contenido de un documento separado de los detalles de como mostrarlo. Los detalles de como se muestra el documento son conocidos como estilos. Si mantienes los estilos separados del contenido puedes:

* Evitar duplicación
* Hacer el mantenimiento más simple
* Usar el mismo contenido con diferentes estilos para diferentes propositos.

## ¿Cómo CSS afecta a mi documento HTML?

Los navegadores web aplican _reglas CSS_ a un documento HTML, esto modifica la forma en que el documento HTML es desplegado. Una regla CSS está formada por:

* Un conjunto de propiedad cuyos valores actualizan la forma en como el contenido HTML es desplegado.
* Un selector el cual _selecciona_ el elemento al que le serán aplicadas los valores de las propiedades.

Cuando un navegador web despliega un documento, este debe combinar el contenido del documento con la información de estilos. Este proceso consta de dos pasos:

1. El navegador convierte el HTML y CSS en el DOM(Document object model). El _DOM_ representa el documento en la memoria de la computadora. Este combina el contenido del documento con sus estilos.

2. El navegador despliega el contenido del _DOM_.

![](https://mdn.mozillademos.org/files/11781/rendering.svg)

## Selectores

Los selectores son usados para definir el contenido HTML al que le quremmos aplicar estilos en nuestra página web. Existen distintos tipos de selectores:

* Selectores simples: selecciona uno o más elementos basados en su tipo de elemento, clase o id.
* Selectores de atributo: selecciona uno o más elementos basados en su atributos.
    - **Ejemplo 1:** a[href="http://ejemplo.com"] {
      propiedad: valor;} : selecciona las etiquetas "a" que contengan el hipervínculo citado.
    - **Ejemplo 2:** a[href$=".mx"] {propiedad: valor;} : selecciona las etiquetas "a" que contengan un hipervínculo cuyo dominio sea el especificado.
* Pseudo-clases: selecciona uno o más elementos que se encuentran en algún estado(por ejemplo _hover_).
* Pseudo-elementos: selecciona uno o más partes de contenido que se encuentran en cierta posición en relación a otro elemento, por ejemplo la primera palabra de un párrafo.

  ```css
   p::first-line {
    color: blue;   
   } /*La primera linea de los  parrafos seran azules*/```
   
* Combinadores: En este caso no son selectores en si, si no son una forma de combinar dos o más selectores en una forma mucho más específica, por ejemplo, los párrafos que son _descendientes_ directos de divs o que están inmediantamente después de un elemento _h_.

|Combinaciones |Selecciona |
| --- | --- |
| Combinadores | Tenemos varias maneras para seleccionar unos elementos respecto a su relación con otros. Estas relaciones se expresan mediante combinaciones de la siguiente forma (A y B representan cualquiera de los selectores vistos hasta ahora):|
| A, B |Cualquier elemento seleccionado por A y/o B (ver Varios selectores en una regla, más adelante).|
| A B | Cualquier elemento seleccionado por B descendiente de un elemento seleccionado por A (o sea, un hijo, un hijo de otro hijo, etc.).|
|A > B| Cualquier elemento seleccionado por B descendiente de un elemento seleccionado por A (o sea, un hijo, un hijo de otro hijo, etc.).|
|A + B| Cualquier elemento seleccionado por B y es el siguiente hermano de un elemento seleccionado por A (o sea, el siguiente hijo del mismo padre).|
|A ~ B| Cualquier elemento seleccionado por B y es uno de los siguientes hermanos del elemento seleccionado por A (uno de los siguientes hermanos del mismo padre).|
Ejemplo : 
h1, h2, h3, h4, h5, h6 {
  font-family: helvetica, 'sans serif';
}

p, li {
  font-size: 1.6em;
}

* Selectores múltiples: La idea de estos selectores es usar el mismo conjunto de declaraciones para varios selectores separados por comas.

![](https://mdn.mozillademos.org/files/3668/css%20syntax%20-%20ruleset.png)

## CSS valores y unidades

* Valores numéricos: para especificar ancho, tamaño de borde o fuente, cuantas veces correr una animación, etc.
* Porcentajes: También pueden ser usados para especificar ancho, tamaño, pero relativo a la altura y ancho del contenedor padre 
* Colores: para especificar 

## Modelo de caja

El modelo de caja es la manera en que se representan todos los elementos html en una página. Cada elemento genera una caja, el comportamiento de esa caja depende de su clasificación: si es de línea o de bloque.

A todas las cajas se les puede aplicar las siguientes propiedades: width, height, padding, margin, border, background. Lo particular de este concepto es que por defecto el width se refiere al ancho del contenido de un elemento (no al ancho total, de borde a borde). 

![](http://www.laurachuburu.com.ar/images/tutoriales/css/modelo-de-caja.png)

## Proyecto: Portafolio

Crearemos un portafolio para búsqueda laboral, empezaremos primero creando los _wire frames_ de nuestra página web.

La página de galería será donde mostremos los proyectos más importantes que hemos realizado.

![](images/gallery.png)

A continuación la página donde hablamos un poco más sobre nosotros.

![](images/about.png)

Finalmente la página donde mostraremos nuestros datos de contacto.

![](images/contact.png)


## Referencias

* https://www.w3schools.com/html/html_forms.asp
* https://www.tutorialspoint.com/html5/html5_deprecated_tags.htm
* https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/HTML_basics
* https://en.wikipedia.org/wiki/HTML
* https://www.w3schools.com/html/html5_semantic_elements.asp
* https://www.tutorialspoint.com/html5/html5_new_tags.htm
* https://developer.mozilla.org/es/docs/Web/HTML/Elemento/input
* https://www.fundeu.es/escribireninternet/edicion-y-maquetacion-de-documentos-web/
* http://htmlcheatsheet.com/
* http://www.laurachuburu.com.ar/tutoriales/modelo-de-caja.php
* https://devcode.la/tutoriales/modelo-caja-css/
* https://developer.mozilla.org/es/docs/Learn/CSS/Introduction_to_CSS/Modelo_cajas
* https://developer.mozilla.org/es/docs/Web/CSS/CSS_Grid_Layout/Conceptos_B%C3%A1sicos_del_Posicionamiento_con_Rejillas
* https://fonts.google.com/
* https://www.materialpalette.com/
* https://developer.mozilla.org/es/docs/Web/CSS/Como_iniciar/Que_es_CSS
* https://developer.mozilla.org/es/docs/Web/CSS/Como_iniciar/Por_que_usar_CSS
* https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/How_CSS_works
* https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Selectors
* https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Simple_selectors
* https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Attribute_selectors
* https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Pseudo-classes_and_pseudo-elements
* https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Combinators_and_multiple_selectors
* https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Values_and_units


