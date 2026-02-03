# Cifrados y Criptografía
## Parte 01: Investigación de Cifrado: Cifrado de Vigenère

### Cifrado elegido: Cifrado de Vigenère

El cifrado de Vigenère es un método de cifrado por sustitución polialfabética que utiliza una serie de diferentes alfabetos de cifrado basados en las letras de una palabra clave. Fue inventado en el siglo XVI y es conocido por su resistencia a los ataques de frecuencia, lo que lo hace más seguro que los cifrados monoalfabéticos simples.

### Ejemplo de aplicación
Supongamos que queremos cifrar el mensaje "ATTACKATDAWN" utilizando la palabra clave "LEMON".

1. Repetimos la palabra clave para que coincida con la longitud del mensaje:
   - Mensaje: ATTACKATDAWN
   - Clave:   LEMONLEMONLE

2. Asignamos valores numéricos a las letras (A=0, B=1, ..., Z=25):

    - Mensaje: 0 19 19 0 2 10 0 19 3 0 22 13
    - Clave:   11 4 12 14 13 11 4 12 14 13 11 4

3. Sumamos los valores correspondientes del mensaje y la clave, y tomamos el resultado módulo 26:

    - Cifrado: (0+11)%26=11, (19+4)%26=23, (19+12)%26=5, (0+14)%26=14, (2+13)%26=15, (10+11)%26=21, (0+4)%26=4, (19+12)%26=5, (3+14)%26=17, (0+13)%26=13, (22+11)%26=7, (13+4)%26=17
    - Cifrado: 11 23 5 14 15 21 4 5 17 13 7 17

4. Convertimos los valores cifrados de nuevo a letras:
    - Cifrado: LXFOPVEFRNHR
Por lo tanto, el mensaje cifrado es "LXFOPVEFRNHR".

### Ventajas
1. **Seguridad Mejorada**: A diferencia de los cifrados monoalfabéticos, el cifrado de Vigenère es más resistente a los ataques de frecuencia debido a su uso de múltiples alfabetos de cifrado.
2. **Simplicidad**: Aunque es más seguro que los cifrados simples, el cifrado de Vigenère sigue siendo relativamente fácil de entender y aplicar.
3. **Historia y Relevancia**: El cifrado de Vigenère tiene una rica historia en la criptografía y ha sido utilizado en diversas aplicaciones a lo largo del tiempo, lo que lo hace interesante desde una perspectiva histórica.

### Vulnerabilidades
1. **Ataques de Kasiski y Friedman**: Estos métodos pueden ser utilizados para determinar la longitud de la clave, lo que facilita la ruptura del cifrado.
2. **Clave Repetitiva**: Si la clave es corta y se repite con frecuencia, puede ser vulnerable a ataques de fuerza bruta.

## Parte 02: Implementación de Funciones de Criptografía

[Ver las funciones implementadas](part2_encryption.ipynb)
