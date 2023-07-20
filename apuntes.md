En react también puedes definir una hoja de estilos específica para un componente, se les llama módulos
Usualmente no se modifica el index.html ni el main.jsx, sino donde mas se trabaja es el app.jsx

### JSX - JavaScript Syntax Extension

- Es una extensión del lenguaje desarrollada por Facebook para React
- Parece JS, pero muestra código de HTML y básicamente es un lenguaje de Templates que muestra HTML pero tiene todas las funciones de JavaScript.
  Una vez compilado son archivos JS con funciones y objetos.

  **Reglas en JSX**

- A diferencia de HTML que no es estricto, en JSX si un elemento de HTML tiene una etiqueta de apertura, deberás tener también la de cierre.
- Las etiquetas de solo apertura como < link > < img > o < input > deberán finalizar con />
- Cada componente debe de tener un return
- En este return debe haber máximo un elemento en el nivel más alto

En react puedes retornar un fragment que es solo esto <></>.

Antes del return se puede escribir funciones y condicionales, un lugar util para validar tus datos antes de mostrarlos, después de ello solo expresiones que se encierra con {} y dentro también puede ser ternarios.

### Muchas formas de escribir CSS en react

Hay muchas formas:

- CSS Plano
- Framework CSS
- Módulos CSS
- Componentes
- SASS
- Styled Components

### Que son los hooks

- React cuenta con una API muy sencilla que te permite crear todo tipo de aplicaciones por medio de algo llamado Hooks.
- Los Hooks se dividen en básicos y Adicionales

### Categorías de Hooks

- useEffect, useState, useContext
- Luego el resto como useReducer, useMemo, useRef

También puedes crear tus propios hooks, de esta forma podrás seperar tu código en funciones reutilizables y sacar todo el beneficio que React ofrece.

### useState

- Básicamente es el estado de tu apliación.
- El Estado es una variable con información relevante, algunas veces el state pertenece a un componente en específico o a veces deseas compartirlo a lo largo de diferentes componentes.
- El state es creado con la función useState()
### React reacciona en base al State
- Cada que tu state cambia, tu aplicación de React va a renderizar y actualizar con esos cambios.

### Reglas de los Hooks
- Los Hooks se colocan en la parte superior de tus componentes de React(justo despues de la función del componente).
- No se deben de colocar dentro de condicionales, y tampoco después de un return

### Eventos en React
- Muy similar a como lo maneja JavaScript
- Los eventos son camelCase, en lugar de onchange es onChange

### Props en React
Es una forma de pasar variables o funciones de un componente a otro.
- El State o funciones que crees de tus componentes, solo estarán disponibles en ese componente.
- Una forma de evitar duplicar código y reutilizar esas variables.
- Los props se pasan del padre al hijo, nunca se pueden pasar del hijo al padre.

- Si tienes un state que se va a pasar por diferentes componentes, lo mejor es colocarlo en el archivo principal.
- Cada nivel de componentes deberá tomar y pasar el Prop hacia otros componentes, tecnologías como Redux o Context evitan tener que hacerlo de esta forma.

### useEffect
- Después de useState es el más utilizado.
- Siempre es un callback, que se ejecuta cuando un state cambia o cuando el componente esta listo.
- Es el sustituo de componentDidMount() y componentDidUpdate()
### Usos
- Al ejecutarse automáticamente cuando el componente esta listo, es un excelente lugar para colocar código para consultar una API o LocalStorage
- Debido a que le podemos pasar una dependencia y estar escuchando por los cambios que suceden en una variable, puede actualizar el componente cuando ese cambio suceda.
- Si el array esta vacio, significa que solo se va a ejecutar una vez(ojo).
