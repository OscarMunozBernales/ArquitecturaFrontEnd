# Curso de HTML y CSS

## Indice
1. Internet.
    - ¿Cómo se contruye la tecnología web?
    - Comprendamos el internet
2. Los básicos del web
    - ¿Como funciona HTML?

# 1. Internet.

## 1.1. ¿Como se contruye la tecnología web?
El **Frontend** es la parte del software que interactúa con los usuarios, en cambio, el **Backend** es la parte que no puedes ver, esta oculta porque contiene la información privada o sensible de nuestros usuarios.

**HTML** nos permite crear la estructura de la página: títulos, párrafos, menús, etc. 

**CSS** nos permite configurar los estilos del HTML, los colores, formas, posiciones, etc.

**JavaScript (JS)** se encarga de la parte funcional, nos permite conectarnos con otros servicios (como PayPal) y nos ayuda a hacer las interacciones mucho más fluidas.

Los **Compiladores** nos ayudan a construir el frontend de nuestras páginas web de forma mucho más rápida y sencilla. En vez de escribir el mismo código una y otra vez, vamos a utilizar estas herramientas para obtener estos mismos resultados de forma automatizada.

El trabajo y las operaciones del backend se pueden resumir con las siglas CRUD: __Create__, **__Read__**, __Update__ y __Delete__. Cuando el frontend se comunica con el backend, debe indicar el tipo de operación y los datos necesarios para que todo funcione correctamente.

Por ejemplo: cuando registramos un usuario, el frontend debe mandar los nombres y contraseña de este usuario para que, el backend, pueda guardar esta información en la base de datos y podamos consultarla más adelante.

## 1.2. Comprendamos el internet

Internet es un conjunto descentralizado de redes de comunicación interconectadas, en otras palabras, son dos (o más) computadoras que se conectan entre sí. Los Protocolos son un conjunto de reglas que hacen posible la comunicación entre diferentes elementos que forman parte de un sistema.

La __World Wide Web__ es un sistema de distribución de documentos (de hipertexto o hipermedia) interconectados y accesibles vía internet, mientras que, los Hipertextos son textos que contienen enlaces a otros textos.

__FTP__ es el protocolo de transferencia de archivos entre sistemas conectados a una red, así es cómo diferentes personas podemos compartir documentos entre nosotros.

Hay algunas computadoras que solo utilizamos para entregar documentos los conocemos como __servidores__, en cambio, las computadoras que solo leen y reciben estos documentos los conocemos como __clientes__. También existe el protocolo de comunicación __P2P__ (Peer to Peer) donde una misma computadora trabaja como servidor y cliente al mismo tiempo.

__La tecnología de la la información__ es la aplicación de ordenadores y equipos de telecomunicación para almacenar, recuperar, transmitir y manipular datos, con frecuencia, utilizado en el contexto de negocios o empresas.

La __Comunicación Síncrona__ es comunicación en tiempo real, por ejemplo, en aplicaciones de mensajería y video-chat. Sin embargo, también existe la __Comunicación Asíncrona__, comunicación en tiempo NO real, así funciona Gmail, puede pasar que recibamos un nuevo correo pero no lo leemos inmediatamente lo envían, por eso es comunicación asíncrona.

# Los básicos del web

## ¿Como funciona HTML?
El HTML es un **Markup Language** de ahi las siglas de HTML, HyperText Markup language.
Sistema de marcas de hipertexto, se enfoca en la diferenciación y síntesis.

La estructura básica del HTML es la siguiente:
```html
<html lang="en">
    <head>
        <!-- Etiquetas meta, script, css, etc. -->
    </head>

    <body>  
        <!-- El cuerpe de la HTML -->
    </body>

</html>
```

![estructura-basica-html](assets/estructura-html.jpg)

Las etiquetas comunes:
```html
<!-- Etiquetas -->
<h1></h1> hasta la <h6></h6>

<!-- Crear secciones o agrupar contenidos -->
<div></div>

<!-- Crear párrafos de texto -->
<p></p>
```

