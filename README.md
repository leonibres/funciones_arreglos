
# Trabajando con Funciones en JavaScript

En esta clase, aprenderemos cómo trabajar con funciones en JavaScript. Las funciones son fundamentales en la programación y ya hemos estado usando algunas a lo largo del curso, como `console.log()`.

## Definición de Funciones

Vamos a crear nuestra propia función. Empezaremos con la palabra reservada `function`. Aquí hay un ejemplo básico:

~~~~
function greet() {
    console.log("Hola Mundo");
}
greet();
~~~~

### Características:
- **Definición**: Usamos la palabra reservada `function` seguida del nombre de la función y paréntesis.
- **Llamada**: Para ejecutar la función, simplemente llamamos su nombre seguido de paréntesis, como `greet()`.

## Funciones con Argumentos

Podemos hacer nuestras funciones más flexibles aceptando argumentos:

~~~~
function greet(name) {
    console.log(`Hola ${name}`);
}
greet("Fernando");
~~~~

### Características:
- **Argumentos**: Los argumentos se definen dentro de los paréntesis en la definición de la función.
- **Uso**: Los argumentos pueden ser usados dentro de la función para personalizar su comportamiento.

### Valores por Defecto

Podemos asignar valores por defecto a los argumentos:

~~~~
function greet(name = "Mundo") {
    console.log(`Hola ${name}`);
}
greet();         // Imprime "Hola Mundo"
greet("Juan");   // Imprime "Hola Juan"
~~~~

### Variables y Alcance

Los nombres de las variables en la definición de los argumentos son independientes de las variables en el ámbito global:

~~~~
let firstName = "Juan";
function greet(name) {
    console.log(`Hola ${name}`);
}
greet(firstName);  // Imprime "Hola Juan"
~~~~

## Ejemplo Completo

Vamos a ver un ejemplo completo utilizando lo aprendido:

~~~~
function greet(name = "Mundo") {
    console.log(`Hola ${name}`);
}

// Llamadas a la función
greet();         // Imprime "Hola Mundo"
greet("Pedro");  // Imprime "Hola Pedro"
greet("María");  // Imprime "Hola María"

// Usando variables
let firstName = "Ana";
greet(firstName); // Imprime "Hola Ana"
~~~~

## Ciclo Infinito con Funciones (Ejemplo de Precaución)

Usar funciones dentro de ciclos puede llevar a comportamientos inesperados si no se maneja correctamente:

~~~~
function greet(name = "Mundo") {
    console.log(`Hola ${name}`);
}

// Ciclo infinito (¡No ejecutar esto sin precaución!)
while (true) {
    greet();
}
~~~~

### Nota:
- **Control del Ciclo**: Para detener un ciclo infinito, en la terminal de comandos puedes usar `Ctrl + C`.

## Resumen

- **Definición de Funciones**: `function nombreDeFuncion() { }`
- **Argumentos y Valores por Defecto**: Permiten hacer las funciones más flexibles y reutilizables.
- **Alcance de Variables**: Entender cómo las variables dentro de las funciones son independientes de las globales.
- **Precauciones**: Cuidado con los ciclos infinitos y el uso adecuado de las funciones.

En la próxima clase, seguiremos creando más funciones y explorando sus capacidades en JavaScript.



