# Sistema de Cifrado - Legado de Al-Kindi

---

##  Índice
1. [Introducción](#introducción)
2. [Objetivo](#objetivo)
3. [Desarrollo Técnico](#desarrollo-técnico)
4. [Documentación del Programa](#documentación-del-programa)
5. [Conclusión](#conclusión)
6. [Bibliografía](#bibliografía)

---

##  Introducción
El criptoanálisis moderno tiene sus raíces en el trabajo de **Abū Yūsuf Yaʻqūb ibn Isḥāq al-Kindī** (siglo IX). Su obra *Risalah fi Istikhraj al-Mu'amma* (Manuscrito sobre el desciframiento de mensajes criptográficos) introdujo el **análisis de frecuencias**. 

Al-Kindi demostró que en cualquier lenguaje natural, la distribución de letras no es uniforme. En los sistemas de encriptación simple como **César** (sustitución por desplazamiento) y **Atbash** (sustitución por espejo):
* Los patrones estadísticos del lenguaje se mantienen intactos.
* La utilización de estos métodos hoy es **inviable** para la protección de datos reales debido a la facilidad de ataques de fuerza bruta (solo 25 combinaciones en César A-Z) y ataques estadísticos que rompen el código en milisegundos.

---

## Objetivo
Desarrollar un entorno web capaz de procesar cifrados César y Atbash sobre un conjunto dinámico basado en el código ASCII, permitiendo la manipulación del módulo matemático para comprender la flexibilidad de los algoritmos de sustitución.

---

##  Desarrollo Técnico

### Especificaciones del Sistema
* **Base:** Estándar ASCII (95 caracteres imprimibles).
* **Módulos Soportados:** Dinámico (Configurable por el usuario).
* **Lenguajes:** HTML5, CSS3 (Google Fonts: Orbitron), JavaScript ES6.

### Lógica Matemática
El sistema implementa la aritmética modular para garantizar que el cifrado se mantenga dentro del conjunto de caracteres definido:

$$C = (P + s) \pmod{M}$$

Donde:
* $C$: Carácter cifrado.
* $P$: Posición del carácter original.
* $s$: Desplazamiento (Shift).
* $M$: Módulo (Tamaño del conjunto seleccionado).

---

##  Documentación del Programa 


### Instrucciones de Uso
1.  **Selección de Conjunto:** Haga clic en el campo "Conjunto de Caracteres" para elegir entre ASCII (95), Alfabeto (26) o Numérico (10).
2.  **Configuración del Módulo:** El módulo $M$ se ajustará automáticamente al largo del conjunto, pero puede ser modificado manualmente.
3.  **Proceso:** Ingrese el texto, seleccione el método (César o Atbash) y presione Cifrar/Descifrar.

---

##  Conclusión
Este proyecto evidencia que la robustez de un sistema no reside solo en el algoritmo, sino en el tamaño del espacio de claves y la entropía del mensaje. Aunque César y Atbash son pilares históricos, el análisis de frecuencias de Al-Kindi los convirtió en herramientas puramente didácticas en la era de la computación cuántica y el cifrado AES.

---

##  Bibliografía
1.  **Al-Kindi** (801–873). *On Deciphering Cryptographic Messages*.
2.  **Singh, S.** (1999). *The Code Book*. Editorial Fourth Estate.
3.  **Standard ASCII** - *Manual de Referencia Técnica de IBM*.
