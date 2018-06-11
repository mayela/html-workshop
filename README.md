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

### Etiquetas descontinuadas

|Etiqueta | Descripción |
|--- | ---|
|\<acronym> | Define un acrónimo|
|\<applet> | Define un applet |
|\<basefont> 	Define un fuente base para la página |
|\<big> | Define texto grande |
|\<center> | Define texto centrado |
|\<dir> | Define una lista de un directorio |
|\<font> | Define text font, size, and color |
|\<frame> | Define un frame |
|\<frameset> | Define un conjunto de frames |
|\<isindex> | Define un campo input |
|\<noframes> | Define una sección no frame |

### Etiquetas nuevas


### Encabezados

* \<h1>Encabezado 1\</h1>
* \<h2>Encabezado 2\</h2>
* \<h3>Encabezado 3\</h3>
* \<h4>Encabezado 4\</h4>
* \<h5>Encabezado 5\</h5>
* \<h6>Encabezado 6\</h6>

Los motores de búsqueda usan los encabezados para indexar la estructura y contenido de tu página web. Para aplicar estilos a los encabezados usa CSS.

### Párrafos

* <p>Define un párrafo</p>
* <br> Inserts a single line break
* <pre>Define un texto preformateado</pre>

### Etiquetas para definir secciones

* _div_
* _section_
* _footer_
* _header_

### Etiquetas para definir elementos multimedia

* _img_
* _audio_
* _video_
* _canvas_
* _svg_

### Etiquetas para formulario

* _form_
* _input_

#### Form

El elemento _form_ que define un formulario puede tener atributos entre los que destacan:

* _action_: Define la acción a realizar cuando el formulario sea enviado. Si el atributo no es definido entonces la acción se establece a la página actual.
* _target_: Especifica si el resultado enviado debe de abrirse en una nueva página o en la página actual.
* _method_: Especifica el método HTTP que será usado para enviar los datos del formulario.

> * El método por default es GET, sin embargo cuando este método es usado los datos del formulario son visibles en la barra de dirección.
> * La longitud máxima de una URL es de 300 caracteres.
> * Nunca uses GET para datos sensibles.
> * GET es bueno para datos no sensibles, como los _query params_ en una búsqueda.

## Proyecto: Portafolio

Crearemos un portafolio para búsqueda laboral, empezaremos primero creando los _wire frames_ de nuestra página web.

La página de galería será donde mostremos los proyectos más importantes que hemos realizado.

![](images/gallery.png)

A continuación la página donde hablamos un poco más sobre nosotros.

![](images/about.png)

Finalmente la página donde mostraremos nuestros datos de contacto.

![](images/contact.png)



