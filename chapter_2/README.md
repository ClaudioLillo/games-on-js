# Capítulo 2

## Estilos CSS : Color, dimensiones, bordes

Introducción

CSS o Cascade Stylesheet es lenguaje que nos permite otorgar estilos a los elementos contenidos dentro de un documento HTML. Existen 3 formas de utilizarlo

1. Dentro de las etiquetas de un elemento
2. En el interior de una etiqueta ```<style>```
3. A partir de un archivo externo, con extensión .css


Por una razón práctica, solo utilizaremos la tercera opción, dado que las 2 anteriores no son de utilidad en ambientes productivos.

En primer lugar, una hoja de estilos debe ser declarada, lo que se consigue con una etiqueta link dentro del head del HTML

```html
    <head>
        <link rel="stylesheet" href="index.css">
    </head>
```

Esta línea, nos permitirá tomar los estilos directamente desde el archivo index.css

Luego, agregaremos 3 contenedores con las clases

- cuadrado
- circulo_verde
- rectangulo_azul 

```html
<body>
    <div class="cuadrado"></div>
    <div class="circulo_verde"></div>
    <div class="rectangulo_azul"></div>
</body>
```

Adicionalmente, agregaremos un texto dentro de cada uno de los contenedores. Este texto lo encerraremos en una etiqueta p, de la siguiente forma

```html
<body>
    <div class="cuadrado">
        <p>cuadrado</p>
    </div>
    <div class="circulo_verde">
        <p>círculo verde</p>
    </div>
    <div class="rectangulo_azul">
        <p>rectangulo azul</p>
    </div>
</body>
```

Nótese que al estar un elemento dentro otro, este se escribe más a la derecha. Esto sucede en forma automática en la mayoría de los editores de código tales como atom, Visual Studio Code o NotePad. Sin embargo, no sucederá con algunos más básicos como el bloc de notas de windows.


Ahora, que ya contamos con nuestros contenedores, es hora de escribir dentro de nuestro archivo index.css

En primer lugar, describiremos la clase cuadrado

```css
.cuadrado{
    width: 300px;
    height: 300px;
    border: 1px solid black;
}
```

Al declarar una clase, esta debe comenzar con un punto. Luego, los atributos de la clase van encerrados entre llaves. En este caso, se declaran 3 atributos:

- width: es el ancho del contenedor, 300 píxeles
- height: es el largo del contenedor, 300 píxeles
- border: es el borde, de 1 pixel, continuo y de color negro

Al aplicar esta clase, debemos conseguir que se muestre un cuadrado de borde negro en nuestra pantalla.

Ahora, declararemos el resto de las clases necesarias para conseguir que nuestros estilos se ajusten los nombres de los contenedores.

```css
.circulo_verde{
    width: 100px;
    height: 100px;
    background: green;
    border-radius: 50%;
}

.rectangulo_azul{
    background: blue;
    width: 200px;
    height: 100px;

}
```

Debemos entender que background es el color que toma el fondo del elemento, así que funciona como un relleno. Por otro lado, border-radius indica cuánto se deben curvar las esquinas. Al utilizar 50% conseguimos que un contenedor cuadrado se vuelva un círculo.

Por su parte, los colores pueden ser declarados en inglés, pero también pueden ser definidos en los formatos rgb, rgba y hexadecimal. Esto, lo aprenderás en la medida en que sea necesario para tus desarrollos.

Por último, pensando en la lógica de un juego, se requiere un contendor principal que contenga todos los elementos gráficos del juego. A este marco, lo llamaremos frame, y será nuestro punto de partida.

```html
<div id="frame">
            <div class="cuadrado">
                <p>cuadrado</p>
            </div>
            <div class="circulo_verde">
                <p>círculo verde</p>
            </div>
            <div class="rectangulo_azul">
                <p>rectangulo azul</p>
            </div>
        </div>
```

Dado que el frame será uno solo, no utilizaremos una clase sino un id. En css, en vez de utilizar un punto al comienzo, usamos un símbolo de numeral #

```css
#frame{
    width:800px;
    height:600px;
    border: 1px solid rgba(0,0,0,0.5);
    margin: auto;
}
```

En este caso, se utilizaron atributos adicionales como margin =  auto, lo que le indica al contendor que se posicione en el centro de todo su espacio disponible. Por otra parte, el color del borde se encuentra escrito en formato rgba.

Nótese que: 

- r = red => rojo
- g = green => verde
- b = blue => azul
- a = opacidad

Los colores se declaran como una combinación de rojo, verde y azul. Cada uno de estos debe tener valores entre 0 y 255. Por su parte, la opacidad puede tomar valores entre 0 y 1.

Por ejemplo, el color rgba(0,0,255,0.8) sería un verde con 80% de opacidad, mientras que rgba(255,0,255,1) sería violeta (combinación rojo y azul) con un 100% de opacidad.

Al aplicar los estilos del frame, esperamos conseguir un marco central, y que el resto de los elementos se encuentre en el interior de este. Aquí es donde se ubicará nuestro juego.