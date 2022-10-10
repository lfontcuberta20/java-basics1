```java
    byte b0 = 122; byte b1 = 14;
    int suma = b0 + b1;
    System.out.printf("Resultado %d%n",suma)
    System.out.println("Resultado " + ((Object)suma).getClass().getSimpleName());

```
Resultado 136
Resultado Integer

**Respuesta**\n
El Resultado es un número fuera de la variable byte entonces tendría que ser un tipo int
