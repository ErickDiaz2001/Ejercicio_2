Ejercicio 2 - Interrupciones

Introducción

Este informe describe el diseño e implementación de un sistema mediante interrupciones de un timer con el cual se encienden 3 LEDs secuencialmente con un intervalo de 200ms entre cada uno. El sistema utiliza interrupciones para temporizar el encendido de los LEDs, sin emplear funciones de retardo por software.

Configuracion 

El system clock del microcontrolador se configuro a 72Mhz.

![image](https://github.com/ErickDiaz2001/Ejercicio_2/assets/169405943/86a437f6-b362-41f3-80eb-994765631e8e)

Se utilizara el timer 2, para obtener una interrupción cada 200 ms se configuro un prescaler a 7200-1 y el counter period a 2000. Ademas de habilitar la interrupcion. 

![image](https://github.com/ErickDiaz2001/Ejercicio_2/assets/169405943/25faf1ff-1dde-47eb-8416-d773bf6f66e9)

Metodología

Se utilizará una variable llamada “contador” la cual se incrementara cada 200ms medinate la interrupción del timer. Para controlar el encendido secuencial de los LEDs se utilizara condicionales if- else.

	  if (counter == 0)
	  {
		...
	  }

	  else if (counter == 1)
	  {
		...
	  }
	  else if (counter == 2)
	  {
		...
	  }

	  else if (counter > 2)
	  {
		...
	  }

Implementación y analisis del programa

![image](https://github.com/ErickDiaz2001/Ejercicio_2/assets/169405943/b8f33e36-5bca-4934-8884-506e1d88e72b)

El tiempo de encendido entre cada led es de 200 ms con un periodo total de 600 ms(verde).

Conclusiones

La implementación de un sistema para encender LEDs secuencialmente con interrupciones y sin funciones de retardo por software ofrece varias ventajas:

Eficiencia: Las interrupciones permiten un control más preciso del tiempo y un mejor aprovechamiento de los recursos del microcontrolador.
Respuesta inmediata: El sistema puede responder a eventos externos de manera inmediata sin afectar el flujo principal del programa.
