# Pipes

## Cómo usar pipes en Angular

Angular ya tiene incorporados algunos pipes de uso habitual que podemos implementar cómodamente para comenzar a experimentar con esta utilidad.

Un pipe muy útil para debugear lo que te llegan en los objetos que recibes de los servicios web es "json". Seguramente lo hayas usado ya. Dentro de un template lo puedes implementar con el carácter de tubería, indicando después de la tubería el nombre del pipe que deseas usar.

	<pre>{{users | json}}</pre>

Suponiendo que "users" es un array de objetos usuario, este pipe te mostrará la cadena de su representación JSON.

