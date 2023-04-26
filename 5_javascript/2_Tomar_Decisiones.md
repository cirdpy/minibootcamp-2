---
title: Tomar Decisiones
has_children: false
parent: Introducción a JavaScript
nav_order: 2
---

# Conceptos básicos de JavaScript: tomar decisiones

Tomar decisiones y controlar el orden en que se ejecuta tu código hace que el mismo sea reutilizable y robusto. Esta sección cubre la sintaxis para controlar el flujo de datos en JavaScript y su importancia cuando se usa con tipos de datos booleanos.


# Un breve resumen sobre los valores booleanos

Los booleanos pueden tener solo dos valores: `true` o `false`. Los booleanos ayudan a tomar decisiones sobre qué líneas de código deben ejecutarse cuando se cumplen ciertas condiciones.

Establecé tu booleano en verdadero o falso de esta manera:

```javascript
let mTrueBool = true
let mFalseBool = false
```

✅ Los booleanos llevan el nombre del matemático, filósofo y lógico inglés George Boole. (1815–1864).

## Operadores de comparación y valores booleanos

Los operadores se utilizan para evaluar las condiciones haciendo comparaciones que crearán un valor booleano. La siguiente es una lista de operadores que se utilizan con frecuencia.

| Símbolo | Descripción                                                                                                                                                                  | Ejemplo            |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------ |
| `>`     | **Mayor que**: compara dos valores y devuelve el tipo de datos booleano `true` si el valor del lado izquierdo es mayor que el del lado derecho                                    | `6 > 5 // true`    |
| `>=`    | **Mayor o igual que**: compara dos valores y devuelve el tipo de datos booleano `true` si el valor del lado izquierdo es mayor o igual que el del lado derecho               | `6 >= 5 // true`   |
| `<`     | **Menor que**: compara dos valores y devuelve el tipo de datos booleano `true` si el valor del lado izquierdo es menor que el del derecho                                    | `6 < 5 // false`   |
| `<=`    | **Menor o igual que**: compara dos valores y devuelve el tipo de datos booleano `true` si el valor del lado izquierdo es menor o igual que el del lado derecho               | `6 <= 5 // false`  |
| `===`   | **Igualdad estricta**: compara dos valores y devuelve el tipo de datos booleano `true` si los valores de la derecha y la izquierda son iguales Y son del mismo tipo de datos | `5 === 6 // false` |
| `!==`   | **Desigualdad**: compara dos valores y devuelve el valor booleano opuesto de lo que devolvería un operador de igualdad estricta                                              | `5 !== 6 // true`  |

✅ Comprobá tus conocimientos escribiendo algunas comparaciones en la consola de tu navegador. ¿Te sorprende algún dato devuelto?

---

# Declaración If

La sentencia `if` ejecutará código entre sus bloques si la condición es verdadera.

```javascript
if (condicion){
    //La condición era verdadera. Se ejecutará el código de este bloque.
}
```

Los operadores lógicos se utilizan a menudo para formar la condición.

```javascript
let miDinero;
let precioLaptop;

if (miDinero >= precioLaptop){
    //La condición era verdadera. Se ejecutará el código de este bloque.
    console.log("¡Conseguí una nueva laptop!");
}
```

---

# Declaración If..Else

La declaración `else` ejecutará el código entre sus bloques cuando la condición sea falsa. Es opcional con una declaración `if`.

```javascript
let miDinero;
let precioLaptop;

if (miDinero >= precioLaptop){
    //La condición era verdadera. Se ejecutará el código de este bloque.
    console.log("¡Conseguí una nueva laptop!");
}
else {
    //La condición era falsa. Se ejecutará el código de este bloque.
    console.log("¡No puedo pagarlo, todavía!");
}
```

✅ Probá tu comprensión de este código y del siguiente código ejecutándolo en una consola de navegador. Cambiá los valores de las variables miDinero y precioLaptop para cambiar el `console.log()` devuelto.

---

# Operadores lógicos y booleanos

Las decisiones pueden requerir más de una comparación y se pueden unir con operadores lógicos para producir un valor booleano.

| Símbolo | Descripción                                                                                                  | Ejemplo                                                                           |
| ------- | ------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- |
| `&&`    | **AND lógico**: compara dos expresiones booleanas. Devuelve verdadero **solo** si ambos lados son verdaderos | `(5 > 6) && (5 < 6 ) //Un lado es falso, el otro es verdadero. Devuelve falso`    |
| `||`    | **OR lógico**: compara dos expresiones booleanas. Devuelve verdadero si al menos un lado es verdadero        | `(5 > 6) || (5 < 6) //Un lado es falso, el otro es verdadero. Devuelve verdadero` |
| `!`     | **NOT lógico**: Devuelve el valor opuesto de una expresión booleana                                          | `!(5 > 6) // 5 no es mayor que 6, pero "!" devolverá verdadero`                   |

## Condiciones y decisiones con operadores lógicos

Los operadores lógicos se pueden utilizar para formar condiciones en sentencias if..else.

```javascript
let miDinero;
let precioLaptop;
let precioConDescuento = precioLaptop - (precioLaptop * .20) //Precio del portátil al 20% de descuento

if (miDinero >= precioLaptop || miDinero >= precioConDescuento){
    //La condición era verdadera. Se ejecutará el código de este bloque.
    console.log("¡Conseguiste una nueva laptop!");
}
else {
    //La condición era falsa. Se ejecutará el código de este bloque.
    console.log("¡No puedo pagarlo, todavía!");
}
```

## Operador de negación

Hasta ahora has visto como puedes usar una instrucción `if...else` para crear lógica condicional. Cualquier cosa que entre en un `if` debe evaluarse como verdadero / falso. Utilizando el operador `!` podés _negar_ la expresión. Se vería así:


```javascript
if (!condicion) {
  // se ejecuta si la condición es falsa
} else {
  // se ejecuta si la condición es verdadera
}
```

## Expresiones ternarias

`If...else` no es la única forma de expresar la lógica de decisión. También podés usar algo llamado operador ternario. La sintaxis tiene el siguiente aspecto:

```javascript
let variable = condicion ? <retorna esto si es verdadero> : <retorna esto si es falso>`
```

A continuación se muestra un ejemplo más tangible:

```javascript
let primerNumero = 20;
let segundoNumero = 10
let mayor = primerNumero > segundoNumero ? primerNumero : segundoNumero;
```

✅ Tomate un minuto para leer este código varias veces. ¿Entendés cómo trabajan estos operadores?

Lo anterior establece que
- si `primerNumero` es mayor que `segundoNumero`
- luego asigna `primerNumero` a `mayor`
- de lo contrario, asigna `segundoNumero`.

La expresión ternaria es solo una forma compacta de escribir el siguiente código:

```javascript
let mayor;
if (primerNumero > segundoNumero) {
  mayor = primerNumero;
} else {
  mayor = segundoNumero;
}
```

🚀 Desafío: creá un programa que se escriba primero con operadores lógicos y luego volvé a escribirlo utilizando una expresión ternaria. ¿Cuál es tu sintaxis preferida?

---

# Revisión y autoestudio

Más información sobre los muchos operadores disponibles para el usuario [en MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators){:target="_blank"}.


## Tarea - Operadores

### Instrucciones

Para practicar los conceptos aprendidos, vamos a aplicarlos en un pequeño programa para conocer si el mayor de una serie de numeros.

### La tarea

Dadas las siguientes tres variables, escribí un programa que imprima en la consola cual es el número más grande.

```javascript
let num1 = 1;
let num2 = 2;
let num3 = 3;
```

> SUGERENCIA, podés empezar escribiendo un programa que determine cual es el mas grande entre las variables `num1` y `num2`, dejando de lado la tercera variable por ahora. Si esto funciona correctamente, modificá el código para considerar el tercer numero.

### Rúbrica

| Criterios | Ejemplar | Adecuado | Necesita mejorar |
| -------- | ------------------------------ | ----------------------------- | ------------------------------- |
| | Se presenta la solución completa | Se presenta solución parcial (comparando dos numeros) | Se presenta solución con errores |
