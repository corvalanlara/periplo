---
layout: page
title: Sobre el viaje
---
<span id="frase"></span>

#### Objetivos:

1. Visitar la mayor cantidad posible de ciudades azules
2. Visitar la mayor cantidad posible de ciudades apodadas "Paris del Este" o "pequeña Paris"
3. Realizar doce trabajos voluntarios diferentes
4. Leer un libro de ficción en cada país visitado.

#### Condiciones:
<ol>
<li>
El viaje comienza y termina en Chile.
</li>
<li>
El viaje se realizará en dirección este.
</li>
<li>
El viaje debe incluir los siguientes países:
	<ul>
		<li>
		Colombia
		</li>
		<li>
		El Líbano
		</li>
		<li>
		India
		</li>
		<li>
		Japón
		</li>
		<li>
		Marruecos
		</li>
		<li>
		México
		</li>
		<li>
		Turquía
		</li>
		<li>
		Vietnam
		</li>
	</ul>
</li>
</ol>

#### Definición:

Del lat. *perĭplus* 'circunnavegación', y este del gr. περίπλους períplous.
<ol>
<li>
m. Viaje o recorrido, por lo común con regreso al punto de partida.
Sin.: viaje, recorrido, trayecto, peregrinaje.
</li>
<li>
m. Recorrido o trayectoria espirituales, doctrinales, ideológicos, etc., de una persona.
</li>
<li>
m. En la geografía antigua, circunnavegación.
Sin.: circunnavegación.
</li>
<li>
m. En la Antigüedad clásica, obra en que se cuenta o refiere un viaje de circunnavegación. <em>El periplo de Hannón</em>.
</li>
</ol>

[Fuente](https://dle.rae.es/periplo)

<script>
let frase = document.getElementById("frase");
let hoy = new Date();
let fecha_inicio = new Date(2024,1,16);
fecha_inicio.setHours(hoy.getHours())
fecha_inicio.setMinutes(hoy.getMinutes())
fecha_inicio.setSeconds(hoy.getSeconds())
fecha_inicio.setMilliseconds(hoy.getMilliseconds())
let dif = fecha_inicio.getTime() - hoy.getTime();
let milisegundos = dif / (1000 * 3600 * 24);
let dias;

if (Math.sign(milisegundos) == 1) {
	dias = Math.ceil(milisegundos);
} else if (Math.sign(milisegundos) == -1) {
	dias = Math.floor(milisegundos);
} else {
	dias = 0;
}

if (dias == 1) {
	frase.innerText = `El viaje comenzará mañana`
} else if (dias > 0) {
	frase.innerText = `El viaje comenzará en ${dias} días.`
} else if (dias == -1) {
	frase.innerText = `El viaje comenzó ayer`
} else if (dias < 0) {
	frase.innerText = `El viaje comenzó hace ${Math.abs(dias)} días.`
} else {
	frase.innerText = `El viaje comienza hoy.`
}
</script>
