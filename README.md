# Control_relevado_de_esfuerzos
Automatización de un proceso de relevado de esfuerzos.

![Relevado](https://github.com/alejandro3141592/Control_relevado_de_esfuerzos/blob/main/Relevado.png)

## Mi papel en el proyecto

Considero que este fue uno de los proyectos que más pusieron a prueba mis habilidades, dado que éstos fueron los circuitos más complicados que he tenido que diseñar desde cero, es decir, no solo me encargué de diseñar la PCB, si no que también tuve que hacer los cálculos y consideraciones pertinenetes para hacer tres circuitos electrónicos que cumplieran ciertas tareas específicas.

El primero de ellos, y el más sencillo, fue el circuito de potencia, pues este solo realizaba una regulación de voltaje, convirtiendo 24V DC, en 12V DC y en 5V DC, el diseño del mismo se puede encontrar [aquí.](https://github.com/alejandro3141592/Control_relevado_de_esfuerzos/blob/main/PlacaPotenciaRelevado.pdsprj)

Luego, está un [circuito](https://github.com/alejandro3141592/Control_relevado_de_esfuerzos/blob/main/AcondicionamientoPlaca.pdsprj) de acondicionamiento de señal, el cual transforma una señal analógica de un sensor de temperatura tipo K, a una señal más amplia para que la lectura del PLC fuera más precisa.

Finalmente, diseñé una placa encargada de ayudar a realizar el Control DC del calentamiento y enfriamiento del sistema. Considero que fue el circuito más complicado, porque consideré que se iba a usar una fuente de soldadura externa que suministra hasta 40A, por lo que no se podé hacer el suministro directo del PLC al sistema. Entonces, se ocuparon algunos sistemas de seguridad, incprporando un optoacplador lineal, un amplificador de instrumentación y un MOSFET de alta potencia, para lograr hacer la retroalimentación del sistema. El circuito se puede acceder mediante el siguiente [enlace.](https://github.com/alejandro3141592/Control_relevado_de_esfuerzos/blob/main/ContolDCRELVADOPlaca.pdsprj)

Además, con lo que respecta a la parte de programación, otro logro importante fue que pude realizar la conexión del PLC, a la nube de Amazon AWS, por lo que se pudo crear una base de datos en la nube monitoreada en tiempo real, utilizando [este código](https://github.com/alejandro3141592/Control_relevado_de_esfuerzos/blob/main/AWSRelevadoEsfuerzosV2%20(2).py) en Python.
