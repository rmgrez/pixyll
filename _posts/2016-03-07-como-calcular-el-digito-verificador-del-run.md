---
layout:     post
title:      Cómo calcular el dígito verificador del RUN
date:       2016-03-07 05:34:00
summary:
categories: rut
---

¿Han visto o han sido partícipes alguna vez del “Juego del Teléfono”? Como muchos ya saben (más que un juego, pareciera ser un experimento), este consiste en reunir a un grupo de personas, en la que uno le transmite un mensaje al oído del más cercano y éste último le pasa el mismo mensaje al siguiente participante, y así se repite el proceso hasta llegar al último individuo.

Finalmente, si el último participante dice en voz alta el mensaje, todos se darán cuenta que es muy distinto al mensaje original.

Si lo aplicamos a la informática, <strong>¿qué pasaría si ocurre esto con la información? ¿Qué pasaría si al enviar una imagen a otra persona, ésta llega distinta? ¿Qué pasaría si cuando me depositan los 15 millones de sueldo a mi Cuenta Rut, el sistema se equivoca y en realidad me llegan 15 mil pesos?</strong>

La comunicación entre varios computadores genera un movimiento enorme de datos, y en cualquier momento estos datos podrían corromperse y cambiar un 0 a un 1 y desatar la 3ª Guerra Mundial. Esta corrupción de datos puede deberse a interferencia, ruido o corte de comunicación, etc.

Es por esto que se han ideado múltiples métodos de detección y corrección de errores, pero hoy, nos centraremos en uno muy simple y que lo ocupamos día a día.

### El Dígito Verificador o Código de Control

Este dígito utilizado para errores de información, errores de tipeo o para mayor seguridad. Podemos encontrarlo en códigos de barras, tarjetas de crédito, códigos bancarios, códigos de identificación personal (como es el RUN) e inclusive la Placa Patente Única de automóviles (PPU). En el caso del RUT y PPU el digito verificador, además de lo mencionado anteriormente, se utiliza para evitar fraudes y engaños de suplantación de identidad.

### Rol Único Tributario

Cada persona inscrita en el Registro Civil tiene su propio RUN, número único e irrepetible que nos sirve como un método de identificación. Este consta de un número de 8 dígitos + un digito verificador que puede ir de 0 a 9 o una K.

<p><strong>¿Qué brujería ocupan las intranet de universidades o páginas bancarias que me dicen cuando mi número RUT es incorrecto?</strong></p>

<p>En Chile el dígito verificador es único para cada RUT, éste se calcula con un algoritmo muy sencillo, conocido como <strong>“módulo 11”</strong>.</p>

<p>Veamos el siguiente ejemplo:</p>

<p>Imagínense que mi RUT es el siguiente:</p>

<p>12.678.579-?</p>

<p>Se procede a tomar los números que componen el RUN de derecha a izquierda, y se multiplica cada dígito por los números que componen la serie numérica 2, 3, 4, 5, 6, y 7. Si se ha llegado al octavo número, se reinicia la serie a 2 nuevamente. Para el ejemplo esto se aplicaría así:</p>

<ul>
<li>9 x 2 = 18</li>
<li>7 x 3 = 21</li>
<li>5 x 4 = 20</li>
<li>8 x 5 = 40</li>
<li>7 x 6 = 42</li>
<li>6 x 7 = 42</li>
<li>2 x 2 = 4</li>
<li>1 x 3 = 3</li>
</ul>

<p>Sumamos todos los resultados y nos arroja: 190
A este número le aplicamos “módulo 11”, es decir, lo que resta al dividirlo por 11.</p>

<p>190:11= 17.2727272727</p>

<p>Quitando la parte decimal.</p>

<p>17 x 11 = 187, y para llegar a 190 faltan 3</p>

<p>Finalmente a 11 le restamos el resultado anterior: 11 – 3 = 8</p>

<p>El resultado anterior corresponde al dígito verificador, a menos que el resultado sea 11 el dígito será 0 y si es 10 el dígito será K.</p>

<p>Así nuestro RUT vendría a ser: 12.678.579-8</p>

<p>Aplicando el mismo método, se puede averiguar el dígito verificador de la placa patente de nuestros vehículos, ya sea la nueva o la antigua PPU. <a href="http://www.srcei.cl/Manuales/ValidacionPatentes.pdf" target="_blank">Aquí hay un detalle</a> con el valor asignado a cada letra de la patente.</p>

<p>
	<a href="http://www.biobiochile.cl/2016/03/07/para-que-sirve-y-como-se-calcula-el-digito-verificador-de-nuestro-rut.shtml" target="_blank">source</a>
</p>