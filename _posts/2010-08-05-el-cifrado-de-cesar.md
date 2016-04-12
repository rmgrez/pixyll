---
layout:     post
title:      El cifrado de César
date:       2010-08-05 09:04:23
summary:    
categories: ciencia
---

A pesar de ser uno de los métodos criptográficos más simples -hoy lo descubriría un niño-, permitió al emperador romano proteger sus mensajes de miradas no autorizadas.

A pesar de ser uno de los métodos criptográficos más simples, el “cifrado de César” permitió a Julio César proteger sus mensajes importantes de las miradas no autorizadas. <strong>Consiste en substituir cada letra del mensaje por otra que se encuentre un número fijo de posiciones más adelante en el alfabeto</strong>, y aunque hoy puede ser “descifrado” hasta por un niño, hace 2000 años -en un mundo en el que pocas personas sabían leer y escribir- este mecanismo era considerado lo suficientemente seguro como para confiar en el la seguridad de un estado.
<br>

![desk](https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/ROT13_table_with_example.svg/475px-ROT13_table_with_example.svg.png)

<p align="center">El ROT 13 es el Cifrado de César con un desplazamiento de trece lugares.</p>
<br>
Es innegable que el mundo moderno tiene muchos más secretos para resguardar de las miradas indiscretas que el de hace 2000 años. Esta situación, en la que a menudo una empresa posee procesos o la “receta” para preparar compuestos que valen miles de millones de euros, ha llevado al desarrollo de mecanismos automatizados que permiten a cualquiera -incluidos gobiernos, empresas y particulares- mantener a salvo sus documentos importantes, aún cuando el potencial enemigo también posea formidables herramientas para intentar violar las protecciones que se pongan en práctica.
Cayo Julio César, el líder militar y político que gobernó la República Romana poco antes de la Era Cristiana, no tenía a su disposición nada más avanzado que un lápiz y papel (o pluma y papiro), pero aún así fue capaz de poner a punto un sistema de cifrado que, para el estado del desarrollo tecnológico de la época, fue completamente exitoso: el cifrado de César.

## ¿En qué consiste este sistema? 

Simplemente, se trata de crear un texto difícil de leer -el texto “cifrado”- realizando una serie de cambios sencillos en el texto original. El cifrado de César suele llamarse también “cifrado por desplazamiento” o “desplazamiento de César”, debido a que los cambios que se efectúan consisten únicamente en reemplazar cada letra del texto original por otra que se encuentra un número fijo de posiciones más adelante en el alfabeto.
Aunque puede aplicarse con desplazamientos de cualquier valor, Julio César solía utilizar un desplazamiento de tres posiciones en casi todos sus mensajes. De esa forma, cada letra A del texto original era sustituida por una D -porque se encuentra 3 lugares a la derecha de la A-, cada B se reemplazaba por una E, y así sucesivamente. Cuando la letra a reemplazar estaba lo suficientemente cerca del final del alfabeto como para que su reemplazo “cayera” fuera de éste (por ejemplo, la Y o la Z), se comenzaba nuevamente por el principio, como si el alfabeto fuese “circular”, continuando con la A, B, C, etc. luego de la X, Y, Z.</p>

## Secretos de estado

Para codificar un mensaje bastaba con buscar cada letra del mensaje original en la tabla anterior y escribir la letra correspondiente del alfabeto cifrado. A la hora de decodificar el texto, se utilizaba la misma tabla pero buscando cada letra del texto codificado en el alfabeto original. Sencillo, pero -para la época en que se utilizaba- lo suficientemente seguro como para que el estado confiase en el para mantener a salvo sus secretos.

Obviamente, su efectividad se basaba en la incapacidad de la mayoría de los contemporáneos de César para leer o escribir. Hoy día, un cifrado como este sería rápidamente descubierto. En realidad, el cifrado de César puede ser atacado por el método de la “fuerza bruta”, simplemente tomando un trozo del texto y probar, uno a uno, todos los desplazamientos posibles que permita el alfabeto utilizado (unos 25 ó 30, en general). Cuando se obtiene un texto que tiene sentido, se aplica ese desplazamiento al resto del documento y asunto resuelto. El segundo sistema, más refinado, consiste en analizar la frecuencia con las que aparece cada letra en un idioma determinado. Supongamos que el texto está en español y que necesitamos decodificarlo. Simplemente, buscamos alguna tabla que muestre la frecuencia con la que aparece cada letra -por ejemplo, más del 13% de las letras de un texto lo suficientemente largo en español es una “E”- y contar las veces que cada letra aparece en el texto codificado. Si algún carácter aparece un 13% o 14% de las veces, seguramente es una “E”. Desplazando el resto de las letras un mismo número de posiciones tendríamos el texto decodificado. Puede parecer complicado, pero es realmente simple.

## Cifrado Vigenère

En la actualidad no se emplea ningún sistema semejante, salvo en juegos o por los niños. Pero a pesar de su sencillez, el cifrado del César suele formar parte de otros sistemas más complejos (como el cifrado Vigenère) o se lo emplea en foros de Internet para ocultar de miradas casuales el final de un chiste, la solución a un acertijo o algún texto ofensivo. En este contexto, el algoritmo más utilizado es el denominado ROT13, que no es otra cosa que el cifrado de César con un desplazamiento de 13 lugares.

Alguna vez se ha dicho que ROT13 es “el equivalente moderno del sistemas empleados en las revistas que imprimían boca abajo las respuestas de los pasatiempos”. El método ideado por César puede mejorarse de varias maneras. Una de las más habituales, popularizada alrededor del año 1500, consiste en desplazar un número diferente de posiciones cada letra, dando lugar al denominado “cifrado Vigenère”. El valor de cada desplazamiento se define usando una palabra clave repetitiva. Si la palabra clave fuera escogida al azar y tan larga como el mensaje el sistema resultante sería, en teoría, indescifrable. ¿Te animas a inventar tu propio sistema de cifrado?. [vía <a href="http://www.abc.es/20100705/ciencia/cifrado-cesar-201007051841.html" target="_blank">abc</a>]
