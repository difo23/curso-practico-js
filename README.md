---
title: "Clases del Curso Práctico de JavaScript"
day: "1"
publishDate: "2021-06-24"
thumbnailImage: "../images/day-1.png"
shareText: " Description: Practica todo lo que has aprendido de JavaScript para crear una página web con diferentes ejercicios básicos de matemáticas. Publícala en GitHub Pages para comenzar con tu portafolio de web developer."
hashtags: ['learn', 'JS', 'GitHub']
draft: false

---

## Prueba de JavaScript

| Source:      | [Platzi Curso practico de js](https://platzi.com/clases/javascript-practico/) |
| ------------ | ------------------------------------------------------------ |
| **Course:**  | Curso Práctico de JavaScript                                 |
| **Teacher:** | Juan David Castro                                            |



## Notes 

## Variables y operaciones

1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve?

> Un espacio reservado de memoria donde se almacena información. :boy:

- ¿Cuál es la diferencia entre declarar e inicializar una variable?

> Declaración de una variable es simplemente darle un nombre a un espacio de memoria. Ejemplo: `var nombre;` solo estamos declarando. 
>
> Inicializar una variable consiste en asignarle valor al espacio de memoria ya declarado. Ejemplo: `nombre = 'Pedrod'`. En este caso estamos inicializado con un valor la variable declarada.
>
> Nota: Normalmente se realizan los dos procesos juntos por ejemplo `var nombre = 'Pedro';`

-  ¿Cuál es la diferencia entre sumar números y concatenar `strings`?

>  La diferencia esta con los tipos que trabajes, debes tener cuidado del tipo de datos que usas con estos operadores.  Ejemplo si  realizas la operación `1 + 1`  tendrás como resultado `2` esto se debe a que son datos del tipo `number`, pero si realizas la operación `1 + '2'` tendrás como resultado  `'12'` , cuando usas `JS` automáticamente al detectar un `string` en los operados realiza una concatenación.  

- ¿Cuál operador me permite sumar o concatenar?

>  El operador `+` se utiliza tanto para sumar y concatenar.

2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre 
- Apellido
- Nombre de usuario en `Platzi`
- Edad
- Correo electrónico
- Mayor de edad
- Dinero ahorrado
- Deudas

3️⃣ Traduce a código `JavaScript` las variables del ejemplo anterior y deja tu código en los comentarios.

```js
let name = 'string'
let last_name = 'string'
let user_name_platzi = 'string'
let age = 0 //Number
let email = 'string'
let age_major = true //Boolean
let saved_money = 0 //Number
let debts = 0 // Number
```

4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)

```js
console.log(`${name} ${ last_name} real money : ${ saved_money - depts}`)
```



## Funciones

1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función?

> Una función no es mas que un espacio de memoria con código, se le asigna un nombre para identificarlo y poder enviar datos en forma de parámetros. 

- ¿Cuándo me sirve usar una función en mi código?

> Las funciones sirven  para re -utilizar código que necesitemos repetir en nuestro programa principal. 

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?

  > Un *parámetro* representa un valor que el procedimiento espera que pase al llamarlo. La declaración del procedimiento define sus parámetros.
  >
  > Un *argumento* representa el valor que se pasa a un parámetro de procedimiento cuando se llama al procedimiento. El código de llamada proporciona los argumentos cuando llama al procedimiento.

  > Pues con esta aclaración hasta yo aprendo a distinguirlo. La fuente es [parámetros y argumentos](https://docs.microsoft.com/es-es/dotnet/visual-basic/programming-guide/language-features/procedures/differences-between-parameters-and-arguments#:~:text=Un%20argumento%20representa%20el%20valor,cuando%20se%20llama%20al%20procedimiento.&text=A%20diferencia%20de%20la%20definici%C3%B3n,m%C3%A1s%20variables%2C%20constantes%20y%20literales.)

2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```js
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```

```js
//Solved
const new_function = (name, last_name, nick_name) => {
    
    const COMPLETE_NAME = `${name} ${last_name}`
    console.log(`My name is ${COMPLETE_NAME}, but my friends call me ${nick_name}`)
}
```



## Condicionales

1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una condicional?

> Una condición es simplemente una regla o sentencia cumplir  para realizar o no, una determinada tarea. Nosotros usamos la condiciones al momento de tomar decisiones.

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?

> En ``js`` existen varias formas de crear condiciones con sus ventajas y desventajas. Las mas usadas son: 
>
> ``if..else if y else`` , el operador ternario ``(condition)? 'true': 'flase'`` y  la estructura `switch ... case y default` 
>
> En teoría estas condiciones son equivalentes, teniendo ciertas diferencias en su uso y costumbres del programador. El `operador ternario` suele usarse en condiciones simples que no tengan necesidad de muchas ramificaciones, en mi caso lo uso mucho en el render condicionado con `react`. El `switch`  para algunos programadores suele ser mala practica y prefieren usar la combinación de `if .. else` en su lugar. 

- ¿Puedo combinar funciones y condicionales?

> Por supuesto que puedes combinarlos, en esencia un programa  informático esta formado por `variables`, `operadores`, `ciclos`, `condicones`y `funciones` (otros agregarían clases y objetos ).   

2️⃣ Replica el comportamiento del siguiente código que usa la sentencia `switch` utilizando `if`, `else` y `else if`:

```js
const tipoDeSuscripcion = "basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "Expert+":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}

```



```js
const type_subs = "basic";

if(type_subs == "basic") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (type_subs == "basic") {
    
}

```



3️⃣ Replica el comportamiento de tu condicional anterior con `if`, `else` y `else if`, pero ahora solo con `if` (sin `else` ni `else if`).

> Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays y un solo condicional. 😏

## Ciclos

1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo?
- ¿Qué tipos de ciclos existen en JavaScript?
- ¿Qué es un ciclo infinito y por qué es un problema?
- ¿Puedo mezclar ciclos y condicionales?

2️⃣ Replica el comportamiento de los siguientes ciclos `for` utilizando ciclos `while`:

```js
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}
for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
```

3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> Pista: puedes usar la función [prompt](https://developer.mozilla.org/en-US/docs/Web/API/Window/prompt) de JavaScript.

## Listas

1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?
- ¿Qué es un objeto?
- ¿Cuándo es mejor usar objetos o arrays?
- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

