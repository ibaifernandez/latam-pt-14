# Web colaborativa navideña

## La introducción

Buenas, compañeros.

Para la práctica de la que he hablado en la clase de hoy (21 de diciembre de 2022) de hacer durante Navidad de forma colectiva, considero que deberíamos tratar de hacer una web «lo más semántica posible». Es decir, una web que utilice debidamente etiquetas semánticas tales que:

- `<article>`
- `<aside>`
- `<footer>`
- `<header>`
- `<main>`
- `<nav>`
- `<section>`

He aquí un diagrama básico en la utilización de estas etiquetas

![HTML Semántico](./assets/img/html-semantico.gif)

La he sacado de [W3Schools]https://www.w3schools.com/html/html5_semantic_elements.asp, donde tenéis una mayor referencia al respecto del HTML semántico.

## La temática

Por otro lado, si bien la temática me es indiferente, diría —por simplificar— que hiciéramos una de índole navideña —por mucho que me disgusten estas fechas— por aquello de estar haciéndola en Navidad —y para que no echemos tres días en pensar sobre qué vamos a hacer la web—. «Christmas Around the World» o algo así creo que podría ser el título —no que tengamos que hacerla en inglés (aunque suele ser mejor si más tarde la queremos integrar en el portafolio), podemos llamarla «Navidad en el mundo» y ya, por ejemplo—.

## La división del trabajo (1)

Ahora bien, ¿qué sugiero? Que hagamos **todo un _site_**. Para hacer un _site_, lo único que necesitamos es... más de una página. Somos cinco, así que propongo que hagamos cuatro páginas. ¿Por qué cuatro? Porque uno de nosotros se va a ocupar de hacer las zonas «comunes»; es decir: `header`, `navegador` y `footer`.

Así pues, tendríamos —nos dividiríamos en...—:

1. Página de inicio
2. Página de «presentación»

- Puede ser, por ejemplo, la presentación de «nosotros», como equipo, haciendo la página y celebrando que el destino nos haya reunido en 4Geeks Academy.

3. Página de «contenido», en la que _verdaderamente_ hablemos de «la Navidad alrededor del mundo»
4. Página de contacto, con un formulario y tal donde puedan ponerse en contacto con nosotros.
5. Y, como digo, una 5ª persona que haga las zonas comunes.

## Los estilos

Deberíamos tener algo así como un «manual de marca».

De entrada, cuanto menos, colores (para que todos usemos los mismos) y fuentes. A tal respecto, ya he creado un CSS donde he importado un par de Google Fonts y una paleta de colores extraída de una foto de Navidad. Concretamente, de esta:

![¡Navidad!](./assets/img/navidad.jpeg)

Y, por obvio, creo que lo mejor es que utilicemos **Bootstrap** en la medida de lo posible.

Os daréis cuenta, además, que en el CSS he dejado ejemplos de uso de variables de color CSS. Creo que —en forma de comentarios— está bien explicado dentro del propio archivo CSS. De otro modo, si gustáis, os grabo un Loom para explicarlo :-)

## La estructura del proyecto

### El directorio

1. Cuatro páginas web en la raíz

   1. Inicio (index.html)
   2. Nosotros (about-us.html)
   3. Navidad (x-mas.html)
   4. Contacto (contact.html)

2. Un archivo CSS dentro de ../assets/css/

   - styles.css

3. Las imágenes las pondríamos en ../assets/img/

4. Un archivo .gitignore donde siempre pongo `.DS_Store` que es un tipo de archivo oculto que existe en todas las carpetas de Mac por defecto y que, por obvio, nada hace _existiendo_ en un _repo_.

5. Un archivo README.md que es en el que estoy consignando la información que estáis leyendo.

6. Un pequeño isotipo para que haga las veces de identidad visual del proyecto ubicado en en ../assets/img/logo junto a un archivo —logo.md— con la información pertinente al respecto de la necesidad de atribuirlo a su autor (se puede hacer en el footer, por ejemplo).

### El _repo_

El _repo_ tiene una rama _primigenia_ que es **_main_**. Y una rama **\*develop**, que es con la que habríamos de ~~jugar~~ trabajar.

### La «autoridad»

De entrada, creo haber protegido ambas ramas de modo que:

1. Se necesitan revisiones de al menos dos miembros del equipo para poder aprobar un _commit_.
2. Se necesita la revisión del «Code Owner» —que entiendo que soy yo— para hacer el _merge_.

(Aquí, la verdá, creo que me vendría bien leerme la documentación respectiva porque por las indicaciones en pantalla no es que ayuden mucho 🤷🏽‍♂️).

Creo que más o menos ya.

### El `<head>``

Todos los archivos html ya van con cierta información precargada; a saber:

#### 1. Etiquetas meta

Concretamente:

- charset
- http-equiv
- viewport
- Metainformación:
  - title
  - description
  - keywords
  - robots
  - language
  - author
- Open Graph:
  - og:title
  - og:site_name
  - og:url
  - og:description
  - og:type
  - og:image
- Twitter Card:
  - twitter:card
  - twitter:site
  - twitter:title
  - twitter:description
  - twitter:image

#### 2. Title y favicon

```
<title>Christmas Around the World</title>
<link rel="icon" type="image/x-icon" href="#">
```

#### Hojas de estilo

Ya han sido enlazadas las siguientes hojas de estilo:

- Hoja de estilos específica (ubicada en ../assets/css/)
- Bootstrap v5.1.3
- Bootstrap Icons v.1.10.2

## La división del trabajo (2)

Yojan ya hizo «la parte de abajo» de la _landing_ de hace par de clases, lo que implica un formulario. Sebastián hizo la parte del «contenido» y yo el navegador y la cabecera. Así pues, de entrada, se me ocurre que...

1. La página de contacto vaya a a **Sol** (contact.html). Por obvio, no se trata _solo_ de hacer un formulario. Emula una alguna página de contacto que te guste, que invite a contactar y que proponga diferentes formas para hacerlo, por ejemplo. Recuerda que tu página no tiene que tener navegador ni footer porque eso lo hará otro miembro del equipo.

2. **Sebastián** haga la página de inicio —pero ni el navegador ni el footer—. Eso sí, una cabecera bien atractiva y secciones que permitan navegar a las otras páginas. Puedes incluso crear mini secciones ¿—en un `aside`, por ejemplo? Que redirijan a lugares específicos de otras secciones utilizando la llamada a IDs en los href (`href="www.direccionweb.com/navidad.html#elID),

3. **Silvana** Navegador y footer. Plantéate, por ejemplo, incluir una lista de navegación a modo de mapa web. Imagina nuestra redes sociales o dispon un formulario de suscripción de los de nombre y correo electrónico. No has de hacer que funcione, solo que esté ahí. Quizás el logo del proyecto. O un submenú que llevare a páginas que no vamos a tener del tipo «Política de privacidad», «Términos y condiciones» y Preguntas Frecuentes Respondidas (FAQ). Ahí te toca practicar un poco de todo.

> Va a ser curioso resolver cómo hacer que el código de Silvana se vea en todas las páginas sin tener que copipastearlo personalmente en cada uno de nosotros en cada uno de los archivos en los que trabajemos.

4. **Yojan**, si te parece bien, haz tú el nosotros (about_us.html). Necesitarás una foto de cada uno y algún tipo de datos en función de la información que vayas a disponer en cada uno de nuestros «perfiles» —longitud de las descripciones, redes sociales,...—. Puedes hablar también un poco de 4Geeks Academy e incluso, si los profes llegan a leer esto, que puedas solicitar su información y los mentemos... ¡o incluso a los mentores! Por falta de información no va a ser ☺️

> Quizá fuere interesante forjar carpetas con archivos sencillos como .md o .txt con esa información y, junto a las imágenes, compartirlas a través de GitHub. La repetición hace la práctica 😅

5. Y por tanto yo, **Ibai**, haría el contenido.

Podéis actualizar este archivo o crear otros similares con la extensión .md en el VS Code. Podéis encontrar todo sobre estos archivos de marcado [aquí](https://www.markdownguide.org/cheat-sheet/).

## Recomendaciones finales

Recordad que aquí la parte importante es que trabajemos en nuestras propias ramas que poder volcar a **`develop`** para más tarde pasar a **`main`**. Es decir, el flujo sería:

> Mi rama > `develop` > `main`
