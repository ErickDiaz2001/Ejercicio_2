Ejercicio 2 - Interrupciones

Introducción

Este informe describe el diseño e implementación de un sistema mediante interrupciones de un timer con el cual se encienden 3 LEDs secuencialmente con un intervalo de 200ms entre cada uno. El sistema utiliza interrupciones para temporizar el encendido de los LEDs, sin emplear funciones de retardo por software.

Configuracion 

El system clock del microcontrolador se configuro a 72Mhz.


Se utilizara el timer 2, para obtener una interrupción cada 200 ms se configuro un prescaler a 7200-1 y el counter period a 2000. Ademas de habilitar la interrupcion. 

![image](https://github.com/ErickDiaz2001/Ejercicio_2/assets/169405943/252d5ede-e2b4-4de1-84ea-6366427aaf6c)

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

![image](https://github.com/ErickDiaz2001/Ejercicio_2/assets/169405943/cf796b99-9a38-42e0-ad5d-2571d53845da)

El tiempo de encendido entre cada led es de 200 ms con un periodo total de 600 ms(verde).

Conclusiones

La implementación de un sistema para encender LEDs secuencialmente con interrupciones y sin funciones de retardo por software ofrece varias ventajas:

Eficiencia: Las interrupciones permiten un control más preciso del tiempo y un mejor aprovechamiento de los recursos del microcontrolador.
Respuesta inmediata: El sistema puede responder a eventos externos de manera inmediata sin afectar el flujo principal del programa.
