title: BeerJS
author:
  name: Felipe Egas Neris
  email: felipe.egas.neris@hotmail.com
output: basic.html
controls: true
theme: juanbrujo/cleaver-beerjs

--

# Javascript a gran escala con clean architecture
## BeerJS octubre 2018

--

### Javascript en el 2018
¿Como soluacionamos apps medianas o grandes?
* React + redux (o mobx)
* Vue + Vuex
* Angular + ngrx
* Jquery (solo el @Keldor)

--
![bien ctm](https://media.giphy.com/media/XreQmk7ETCak0/giphy.gif)

--

### Pero esperen...

Que pasa si:
* ¿Alguno de estos frameworks cambia su licencia? (como lo intento facebook con React hace poco)
* ¿Se acabo el proyecto o ya no hay soporte?

--

![nos fuimos a la B](https://media.giphy.com/media/nrXif9YExO9EI/giphy.gif)

--

### clean architecture al rescate

![](https://cdn-images-1.medium.com/max/2000/1*biSmg94qPg58-ppug82-Ng.jpeg)

--
### Características

* Independientes de Frameworks. No estan acopladas a librerias, lo que permite utilizar estas librerías como herramientas que son fácilmente sustituibles.

* Testables. las reglas de negocio son fácilmente testables sin utilizar la interfaz de usuario, base de datos, servidor web.

* Independientes de la interfaz de usuario. La interfaz de usuario es fácilmente modificable.

* Independientes de la base de datos. Es fácil sustituir una base de datos por otra sin afectar a las reglas de negocio.

* El dominio es la parte más importante la capa de dominio es la más importante y de la que dependen todas las demás pero el dominio no depende de ninguna.

--

### Mi aproximación a clean architecture

* Entities: Este grupo contendrá los modelos de negocio y las interfaces de datos, Las Reglas de validacion de las propiedades pueden ser implementadas acá

* Interactors: Este grupo contendrá las reglas de negocios de la Aplicación

* Services: Este grupo contendrá las llamadas API ,LocalStorage, etc.

* Exposers: Este grupo expondrá nuestros Interactors para que las use la ultima capa.

--

Mucho blabla, vamos al código:

 

