# Curso de CSS Grid Layout

# 1. Propiedades de CSS Grid Layout

## 1.1. Conceptos fundamentales sobre CSS Grid Layout

**Grid Container**: va a ser el elemento padre que va a tener puesto un nuevo tipo de display: grid. Nos permite colocar otras propiedades para manipular nuestro layaout.
**Grid Item**: Son nuestro componentes, contenido, lo que vamos a manejar. Nuestras filas o columnas que vamos a mover a nuestro gusto. Son hijos directos de grid.
**Grid Line**: Lineas divisorias horizontales y verticales.
**Grid Track**: Espacio entre dos líneas adyacentes. Filas y columnas.
**Grid Cell**: Celdas, espacio en dos filas adyacentes y 2 columnas adyacentes.
**Grid Area**: Espacio rodeado por 4 grid lines

## 1.2. Definiendo columnas
En el siguiente código vamos a definir columnas dentro de un grid.

```css
body{
    font-family: Arial;
}

.container{
    display: grid;
    grid-template-columns: 20% 50% 200px;
}
```

```html
<section class="container">
    <div class="item">contenido #1</div>
    <div class="item">contenido #2</div>
    <div class="item">contenido #3</div>
    <div class="item">contenido #4</div>
    <div class="item">contenido #5</div>
    <div class="item">contenido #6</div>
    <div class="item">contenido #7</div>
    <div class="item">contenido #8</div>
    <div class="item">contenido #9</div>
    <div class="item">contenido #10</div>
    <div class="item">contenido #11</div>
    <div class="item">contenido #12</div>
</section>
```

Resultado:

![definiendo-columnas](assets/definiendo-columnas.png)

## 1.3. Definiendo filas
Dentro de nuestros grid vamos a tener uno explicito y otro implicito
 - Grid explicito (explicit grid) es cuando nosotros definimos el numero de filas o columnas.
 - Grid implicito (implicit grid) es cuando tenemos filas o columnas que no definimos pero son parte de nuestro grid.

Ejemplo:

```css
body {
    font-family: Arial;
}

.container {
    display: grid;
    grid-template-columns: 20% 50% 200px;
    grid-template-rows: 300px 300px;

    /* grid-template: filas / columnas */
    grid-template: 300px 100px 100px / 50% 100px 100px;
}

.item {
    background-color: lightblue;
    padding: 10px;
    border: 1px solid red;
}
```

```html
<section class="container">
    <div class="item">contenido #1</div>
    <div class="item">contenido #2</div>
    <div class="item">contenido #3</div>
    <div class="item">contenido #4</div>
    <div class="item">contenido #5</div>
    <div class="item">contenido #6</div>
    <div class="item">contenido #7</div>
    <div class="item">contenido #8</div>
    <div class="item">contenido #9</div>
    <div class="item">contenido #10</div>
    <div class="item">contenido #11</div>
    <div class="item">contenido #12</div>
</section>
```

Resultado:
![](assets/definiendo-filas.png)

## 1.4. Grid identados y tipos de display
Display subgrid para heredar la configuración del grid padre (cuando se esten anidando grids).
Display inline-grid muestra el grid en una sola linea

Ejemplo:

```css
body {
    font-family: Arial;
}

.container {
    display: grid;
    grid-template-columns: 20% 50% 200px;
    grid-template-rows: 300px 300px;
    /* grid-template: filas / columnas */
    grid-template: 300px 100px 100px / 50% 100px 100px;
}

.item {
    background-color: lightblue;
    padding: 10px;
    border: 1px solid red;
}

.item:nth-of-type(4) {
    background-color: blue;
    overflow: auto;
    /* display: subgrid;  LA GRACIA DE SUB GRID ES QUE HEREDA LA CONFIGURACIÓN DEL GRID PADRE PERO AUN NO ESTA IMPLEMENTADA*/
    /* display: -moz-inline-grid; MUESTRA TODOS LOS GRID EN LINEA*/
    display: grid;
    grid-template: 50px 50px 5px / 200px 200px 200px;
}

.item .item {
    background-color: yellow;
}
```

```html
<section class="container">
    <div class="item">contenido #1</div>
    <div class="item">contenido #2</div>
    <div class="item">contenido #3</div>
    <div class="item">
        <div class="item">sub-item's #1</div>
        <div class="item">sub-item's #2</div>
        <div class="item">sub-item's #3</div>
        <div class="item">sub-item's #4</div>
        <div class="item">sub-item's #5</div>
        <div class="item">sub-item's #6</div>
    </div>
    <div class="item">contenido #5</div>
    <div class="item">contenido #6</div>
    <div class="item">contenido #7</div>
    <div class="item">contenido #8</div>
    <div class="item">contenido #9</div>
    <div class="item">contenido #10</div>
    <div class="item">contenido #11</div>
    <div class="item">contenido #12</div>
</section>
```

Resultado:

![sub-item](assets/sub-items.png)


## 1.5. Espacio entre filas y columnas
Para obtener espaciado entre las filas y columnas vamos a utilizar una propiedad llamada __grap__ ejemplo:

```css
.container {
    display: grid;
    grid-template-columns: 20% 50% 200px;
    grid-template-rows: 300px 300px;
    /* grid-template: filas / columnas */
    grid-template: 300px 100px 100px / 50% 100px 100px;
    /*  */
    /* grid-row-gap: 10px;
    grid-column-gap: 10px; */


    gap: 10px 10px; /*FILA COLUMNA*/
}
```

Resultado

![espaciado](assets/espaciado.png)

Facilmente uno puedo ocupar la propiedad margin en los item's pero ocupar margin nos va a alterar el ancho y/o alto del elemento, mientras que el grap va hacer la separación 
como corresponde, sin afectar el tamaño del item.


