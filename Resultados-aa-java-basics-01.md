## Ejercicio 1

```java
    byte b0 = 122; byte b1 = 14;
    int suma = b0 + b1;
    System.out.printf("Resultado %d%n",suma)
    System.out.println("Tipo " + ((Object)suma).getClass().getSimpleName());

```
Resultado 136

Tipo Integer

### Respuesta

El Resultado es un número fuera de la variable byte entonces tendría que ser un tipo int. Si lo hacemos sin poner una variable tendremos una salida de tipo integer igualmente.

## Ejercicio 2

```java
    char c = 'a';
    int n = c;
    System.out.printf("Resultado %d%n", n);
    System.out.println("Tipo " + ((Object)n).getClass().getSimpleName());
```
Resultado 97

Tipo Integer

### Respuesta

El Resultado es un número asignado a la letra 'a' en una tabla de código de cáracteres Unicode.

```java
    char c = 'a';
    short s = (short)c;
    System.out.printf("Resultado %d%n", n);
    System.out.println("Tipo " + ((Object)n).getClass().getSimpleName());
```
Resultado 97

Tipo Short

### Respuesta

En mi ejemplo aparecen los resultados gracias al casting que le hice al short. Aunqué no se especifique en la práctica. Pero hacerlo me hizo entender que, los carácter tipo char no se traducen a short por ello tenemos que hacer un casting. 

## Ejercicio 3

### Respuesta

Me adelanté al intentar probar algunas cosas, entonces, básicamente como dije en el ejercicio anterior estamos haciendo un casting y con ello forzamos que traduzca el tipo de dato. Y este dato será cortado ya que ocupa menos bits, ya que hemos visto que el tipo char no se traduze directamente a short.

## Ejercicio 4

```java
    short s = (short)32000;
    System.out.printf("Resultado %d%n", s);
    short p = (short)35000;
    System.out.printf("Resultado %d%n", p);
```
Resultado 32000

Resultado -30536

### Respuesta

El resultado de 32000 se imprime correctamente, ya que está dentro del dominio del tipo de dato short. Pero por otro lado el 35000 no está dentro del domínio, entonces lo que ocurre es que cuando se llega al límite empieza a contar de nuevo con los números que restan.

## Ejercicio 5

```java
    var v = 5.0;
    System.out.println("Tipo " + ((Object)v).getClass().getSimpleName());
    var v0 = 5;
    System.out.println("Tipo " + ((Object)v0).getClass().getSimpleName());
```
Tipo Double

Tipo Integer

### Respuesta

Por defecto los números no enteros serán guardados con el tipo de dato de Double, aunque podríamos hacerlo de tipo float para ocupar menos espacio. Y los números enteros por defecto son guardados con el tipo de dato Integer.

```java
...
var v1 = v + v0;
System.out.printf("Resultado %f%n", v1);
System.out.println("Tipo " + ((Object)v1).getClass().getSimpleName());
```
...
Resultado 10.000000
Tipo Double

### Respuesta

Como double es un tipo de dato que ocupa más espacio, el integer se adapta a él y así no estaremos borrando los datos del double en la suma. Entonces el tipo de dato resultante es double.

## Ejercicio 8

```java
    char c = 'a';
    int c1 = 1;
    System.out.printf("Resultado %c y %d%n", c, c1);
```
Resultado a y 1

### Respuesta

Por lo que analizé no podemos poner dos tipos de datos en secuéncia en la misma línea. La solución es básicamente separar ambas variables, y además ponerle a la variable c1 su tipo de dato.

## Ejercicio 9

```java
    var h = 4 * 4f + (4.0 + 4);
    float f = h;
    System.out.printf("Resultado %f%n", f);
```
|   float f = h;

incompatible types: possible lossy conversion from double to float

### Respuesta

Básicamente, no podemos transformar un tipo de dato double a float sin tener hacer un casting. Entonces resultó en un error. Para resolvero hacemos un casting y forzar que el dato double pase a ser float.

### Solución

```java
    var h = 4 * 4f + (4.0 + 4);
    float f = (float)h;
    System.out.printf("Resultado %f%n", f);
```
Resultado 24.000000

## Ejercicio 10

```java
    byte b0 = 4, b1 = -4, b2 = 12;
    boolean bol1 = b0 == b2 / 3;
    System.out.printf("Resultado %b %n", bol1);
```
Resultado true

```java
    byte b0 = 4, b1 = -4, b2 = 12;
    boolean bol2 = b0 + b1;
    System.out.printf("Resultado %b %n", bol2);
```
|   boolean bol2 = b0 + b1;
incompatible types: int cannot be converted to boolean

```java
    byte b0 = 4, b1 = -4, b2 = 12;
    boolean bol3 = b0 + b1 > b2;
    System.out.printf("Resultado %b %n", bol3);
```
Resultado false

### Respuesta

En el primer boolean el resultado es true, ya que el resultado de b2 dividido entre 3 es igual a 4, que es el valor de b0. Y ya que la equación declara que los dos valores són iguales y realmente lo son, pues el resultado es true.

En el segundo boolean la equación no declara nada entonces solo resulta en un error.

Y por úlitmo el tercer boolean declara que la suma de b0 y b1,(= 0) es mayor que b2(que es 12). Y esto no corresponde con una respuesta correcta entonces es falso.
