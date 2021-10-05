# Capítulo 1

## Uso de HTML y contenedores

Introducción

HTML es un lenguaje de marcado que utiliza etiquetas para ordenar el contenido, y que además permite enlazar el texto mediante el uso de hipervínculos

Un documento de HTML se compone de las siguientes partes esenciales

- DOCTYPE
- head
- body

Estos elementos, así como todo lo que se escribe en HTML debe ir encerrado en etiquetas, delimitadas por los símbolos "<" y ">"

```html
<!DOCTYPE html>
<html>
    <head></head>
    <body></body>
</html>
```

Las etiquetas ```<html>``` y ```</html>``` constituyen los límites del documento. La primera es una etiqueta de apertura, mientras que la segunda es una etiqueta de cierre.

Generalmente, encontraremos esta estructura, salvo por algunos casos particulares que se irán viendo con el pasar de los capítulos

Por ahora, debemos notar que las etiquetas se utilizan en pares. En este caso, las etiquetas head y body se encuentran dentro de las etiquetas html

Ahora que tenemos lo básico, comenzaremos por escribir cierto contenido dentro de las etiquetas head

```html
<head>
    <meta charset="utf-8">
    <title>Juego de Ejemplo</title>
</head>
```

La etiqueta meta nos permite declarar metadatos, que en este caso, nos permitirán usar caracteres especiales tales como ñ o letras con acentos.

Por su parte, las etiquetas title nos permiten darle un titulo al documento. Al abrir este html en un navegador, el titulo corresponde al texto que se oberva en la parte superior de la pestaña.

De aquí en adelante, solo trabajaremos en el interior de las etiquetas body, que corresponden al cuerpo del documento. Dentro de ellas, colocaremos todos los elementos que queremos que el usuario vea.

```html
<body>
    <h1>Aquí va el contenido principal</h1>
    <h2>Esto es un subtítulo</h2>
    <a href="www.google.cl">Esto es un link a google</a>
</body>
```

En este caso, hemos incorporado 3 elementos al cuerpo del documento. En primero lugar, tenemos una etiqueta h1. Estas se utilizan cuando se desea crear un título. Mientras más grande sea el número que acompaña a la h, más pequeña será la fuente del texto.

Luego, tenemos un enlace o hipervínculo, que nos permite saltar hacía otra web en un simple click. Este elemento es esencial, porque es parte de lo que define a una página web propiamente tal.

En la última versión de html, existen muchísimas etiquetas, sin embargo, con la finalidad de escribir juegos nos centraremos solo en unas pocas. La que más utilizaremos se llama div, y corresponde a un contenedor. Dicho de otra forma, es tan solo un área rectangular. Mediante el uso de algunos estilos, conseguiremos que este contenedor adquiera propiedades específicas tales como tamaños, formas, colores, bordes, animaciones, etc.

