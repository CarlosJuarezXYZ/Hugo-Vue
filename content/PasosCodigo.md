---
title: "Pasos para el Codigo"
date: 2020-08-06T14:54:39-05:00
draft: false
---


La librería en este caso la estamos descargando de un CDN donde se almacena todo el código Javascript (podemos descargarla en nuestro equipo sin problema):

  ``` html
   <script src="https://cdn.jsdelivr.net/npm/vue"></script> 
   ```    

Una vez importado el framework podemos crear un objeto de la clase Vue y le pasamos como pámetro un objeto literal con dos atributos llamados 'el' y 'data':

  ``` javascript
  var app = new Vue({
    el:'#aplicacion',
    data:{
      mensaje: 'hola mundo Vue'
    }
  })
 ```

Esos nombres para los atributos no son un capricho, el atributo 'el' hace referencia al 'id' de un elemento HTML definido previamente:

```html

  <div id="aplicacion">{{mensaje}}</div>

```

El atributo 'data' es otro objeto literal que definimos un nombre arbitrario llamada 'mensaje' y su valor es un string:

``` javascript

    data:{
      mensaje: 'hola mundo Vue'
    }

``` 

Dentro del elemento HTML div hemos dispuesto entre dobles llaves el nombre del atributo 'mensaje' definido en el objeto 'app' de la clase Vue. El valor se extrae de la propiedad 'data':

``` javascript

{{mensaje}}

```
Este concepto de recuperar datos del modelo y mostrarlos en la vista con las dobles llaves se llama interpolación.

Cuando cargamos la página HTML en el navegador podemos comprobar que dentro del div se remplaza la expresión {{mensaje}} por el valor almacenado en la propiedad 'mensaje'.

Ese proceso de modificar el contenido de página lo hace el framework Vue en forma transparente gracias al objeto "app" de la clase Vue que creamos, lo logra ya que le pasamos la referencia del id del 'div' y dentro del div definimos la expresión.