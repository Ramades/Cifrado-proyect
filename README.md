# Sistema de Cifrado - Legado de Al-Kindi

---

**UNIVERSIDAD AUTÓNOMA DE Aguascalientes ** 

**Departamento de Ciencias Básicas** 
**Seguridad en Sistemas**
**Estudiante:** Angel Ramses Martinez Herrera - 264153  
**Catedrático:** Mtro. Arturo Ocampo Silva  
**Fecha:** 20/02/2026

---

## Índice
1. [Introducción](#introducción)
2. [Objetivo](#objetivo)
3. [Desarrollo Técnico](#desarrollo-técnico)
4. [Documentación del Programa](#documentación-del-programa)
5. [Conclusión](#conclusión)
6. [Bibliografía](#bibliografía)

## Introducción
El origen del criptoanálisis científico se remonta al siglo IX con el polímata árabe **Abū Yūsuf Yaʻqūb ibn Isḥāq al-Kindī**, considerado el padre de la ruptura de códigos. En su tratado *Risalah fi Istikhraj al-Mu'amma* (Manuscrito sobre el desciframiento de mensajes criptográficos), Al-Kindi revolucionó la seguridad de la información al describir por primera vez la técnica del **análisis de frecuencias**. 

### El Aporte de Al-Kindi al Hackeo de Sistemas
Antes de Al-Kindi, se creía que un mensaje cifrado mediante sustitución simple era virtualmente inexpugnable. Él demostró que en cualquier lenguaje natural, la distribución de caracteres no es aleatoria. Al observar que ciertas letras aparecen con una frecuencia predecible (como la 'e' y la 'a' en español), Al-Kindi probó que si el criptoanalista conoce el idioma original, puede correlacionar las letras más frecuentes del texto cifrado con las del lenguaje común. 

Este descubrimiento proporcionó la primera "llave maestra" para hackear sistemas de encriptación, permitiendo que cualquier cifrado de sustitución monoalfabética fuera vulnerable a un atacante con suficientes datos y paciencia.



### Inviabilidad de César y Atbash en la Actualidad
En el contexto de la seguridad informática contemporánea, los cifrados César y Atbash han quedado relegados exclusivamente a fines educativos o recreativos debido a dos factores críticos:

1. **Vulnerabilidad Estadística:** Como estos métodos solo intercambian un carácter por otro de forma fija (sustitución simple), mantienen intacta la estructura estadística del mensaje original. Un atacante moderno puede automatizar un análisis de frecuencias y romper el código en fracciones de segundo.

2. **Espacio de Claves Reducido:**
   * El **Cifrado César** tiene un espacio de claves extremadamente pequeño (normalmente 25 en un alfabeto estándar). Esto permite realizar un ataque de **fuerza bruta** probando todas las combinaciones posibles de manera instantánea.
   * El **Cifrado Atbash** ni siquiera utiliza una clave secreta; su lógica es fija y pública (espejo del alfabeto), por lo que no ofrece ninguna seguridad real, solo una ofuscación básica.



En la era del procesamiento masivo de datos, donde la potencia de cálculo se mide en teraflops, estos algoritmos no ofrecen resistencia alguna. La protección de datos reales hoy exige algoritmos de sustitución polialfabética o sistemas asimétricos donde la relación entre el texto plano y el cifrado sea matemáticamente compleja y no lineal.
## Objetivo
Desarrollar un entorno web capaz de procesar cifrados César y Atbash sobre un conjunto dinámico basado en el código ASCII, permitiendo la manipulación del módulo matemático para comprender la flexibilidad de los algoritmos de sustitución.

## Desarrollo Técnico

### Especificaciones del Sistema
* **Base:** Estándar ASCII (95 caracteres imprimibles).
* **Módulos Soportados:** Dinámico (Configurable por el usuario).
* **Lenguajes:** HTML5, CSS3 (Google Fonts: Orbitron), JavaScript ES6.

### Cifrado César
Es un método de sustitución monoalfabética donde cada letra del texto original es reemplazada por otra que se encuentra un número fijo de posiciones (desplazamiento) más adelante en el alfabeto. En este proyecto, el desplazamiento es dinámico y se aplica sobre el módulo seleccionado.



### Cifrado Atbash
Es un tipo particular de cifrado por sustitución de origen hebreo. Consiste en invertir el alfabeto, de modo que la primera letra se sustituye por la última, la segunda por la penúltima, y así sucesivamente. Matemáticamente, es una función involutiva (aplicar el cifrado dos veces devuelve el texto original).



### Lógica Matemática
El sistema implementa la aritmética modular para garantizar que el cifrado se mantenga dentro del conjunto de caracteres definido:

Para el cifrado César:
$$C = (P + s) \pmod{M}$$

Para el cifrado Atbash:
$$C = (M - 1 - P) \pmod{M}$$

Donde:
* $C$: Carácter cifrado.
* $P$: Posición del carácter original.
* $s$: Desplazamiento (Shift).
* $M$: Módulo (Tamaño del conjunto seleccionado).

---

## Documentación del Programa 
La aplicación web de cifrado está disponible en: https://ramades.github.io/Cifrado-proyect/

La documentación técnica detallada se encuentra en: https://ramades.github.io/Cifrado-proyect/documentacion.html

### Instrucciones de Uso
1. **Selección de Conjunto:** Haga clic en el campo "Conjunto de Caracteres" para elegir entre ASCII (95), Alfabeto (26) o Numérico (10).
2. **Configuración del Módulo:** El módulo $M$ se ajustará automáticamente al largo del conjunto, pero puede ser modificado manualmente.
3. **Proceso:** Ingrese el texto, seleccione el método (César o Atbash) y presione Cifrar/Descifrar.

## Conclusión
El presente proyecto ofrece una incursión fundamental en los pilares de la criptografía. Es evidente que algoritmos como César y Atbash, aunque revolucionarios en su contexto histórico, resultan obsoletos frente a las capacidades de procesamiento actuales. Hoy en día, la seguridad de la información descansa sobre modelos matemáticos de una complejidad exponencialmente mayor, como los sistemas asimétricos y de curva elíptica.

Sin embargo, la historia de la criptografía nos enseña que la seguridad es una carrera armamentista perpetua: lo que hoy consideramos inquebrantable, mañana será vulnerable ante el avance de la computación cuántica y el aumento de la capacidad de cómputo global. El desarrollo de este software no solo ha sido un ejercicio de programación, sino una lección sobre la naturaleza efímera de la privacidad. Este proyecto resalta que, sin importar la complejidad del algoritmo, el eslabón más fuerte siempre será el entendimiento profundo de la lógica que protege nuestros datos.

## Bibliografía
1. **Al-Kindi** (801–873). *On Deciphering Cryptographic Messages*.
2. **Singh, S.** (1999). *The Code Book*. Editorial Fourth Estate.
3. **Standard ASCII** - *Manual de Referencia Técnica de IBM*.
4. **López Farjeat, L. X.** (2008). Al-Kindī. Philosophica: Enciclopedia filosófica on line.
5. **Cifrado César**. Wikipedia, la enciclopedia libre. https://es.wikipedia.org/wiki/Cifrado_César
6. **Cifrado Atbash**. dCode.fr. https://www.dcode.fr/cifrado-atbash
