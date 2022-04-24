Esta Aplicación incuple los 5 principios SOLID:

1.- Principio de responsabilidad única:
	La clase File tiene muchos métodos diferentes como convertWavToMp3() que no corresponden a lo que debería hacer la clase únicamente para cumplir
	con el principio pudiéndose dividir en clases hijas.
	Para arreglar esto simplemente tendríamos que crear nuevas clases especializadas en cada cosa en concreto.

2.- Principio de sutitución de Liskov:
	Las clases File y Directory no pueden lanzar métodos con excepciones más restrictivas que la clase padre.

3.- Principio de segregación de interfaces:
	Hay métodos como serpos y read que no se usan y se deberían de crear nuevas interfaces a partir FileSystemItem.
	Además todos los métodos están en una misma interfaz, para cumplir con el principio tendríamos que crear nuevas interfaces más específicas.

4.- Principio de abierto/cerrado:
	La mayoría de atributos y clases son no son privados lo que provoca que al mínimo cambio
	que queramos implementar afecte al resultado de la ejecución de la aplicación y clases adyacentes.

5.- Principio de Inversión de dependencias:
	Muchas clases e interfaces están en el mismo paquete, deberíamos abstraer las interfaces del
	paquete files que contiene las clases, creando así un nuevo paquete exclusivo para las interfaces.

