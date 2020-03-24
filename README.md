# Polimorfismo

Modificación del ejercicio planteado en la web:

### [Polimorfismo en Java -Interface- (Parte II), con ejemplos](https://jarroba.com/polimorfismo-en-java-interface-parte-ii-con-ejemplos/)

He movido la carpeta Polimorfismo a la carpeta Main para que funcione el código.

He modificado el código del método main() para crear objetos de la clase correspondiente en lugar de la clase SeleccionFutbol:

```java
	public static void main(String[] args) {
	//SeleccionFutbol delBosque = new Entrenador(1, "Vicente", "Del Bosque", 60, 28489);
	//SeleccionFutbol iniesta = new Futbolista(2, "Andres", "Iniesta", 29, 6, "Interior Derecho");
	//SeleccionFutbol raulMartinez = new Masajista(3, "Raúl", "Martinez", 41, "Licenciado en Fisioterapia", 18);

	Entrenador delBosque = new Entrenador(1, "Vicente", "Del Bosque", 60, 28489);
	Futbolista iniesta = new Futbolista(2, "Andres", "Iniesta", 29, 6, "Interior Derecho");
	Masajista raulMartinez = new Masajista(3, "Raúl", "Martinez", 41, "Licenciado en Fisioterapia", 18);
	
	integrantes.add(delBosque);
	integrantes.add(iniesta);
	integrantes.add(raulMartinez);
	. . .
```


El ejercicio funciona correctamente, no hace falta crear objetos de la clase SeleccionFutbol para añadirlos al ArrayList:

`public static ArrayList<SeleccionFutbol> integrantes = new ArrayList<SeleccionFutbol>();`

Se pueden añadir al ArrayList si los objetos son de las clases hijas de SeleccionFutbol: Entrenador, Futbolista y Masajista.

No hace falta hacer la conversión al llamar a los métodos propios de cada clase hija:

```java
// PLANIFICAR ENTRENAMIENTO
//((Entrenador) delBosque).planificarEntrenamiento();
delBosque.planificarEntrenamiento();

// ENTREVISTA
//((Futbolista) iniesta).entrevista();
iniesta.entrevista();

// MASAJE
//((Masajista) raulMartinez).darMasaje();
raulMartinez.darMasaje();
```

