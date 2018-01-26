## Post-mortem SPACE HELL
Éste es el post-mortem del proyecto *SPACE HELL* por parte de Borja Cano y Roberto Alcázar.
##### Breve comentario sobre las ideas que hemos sacado al final del proyecto:

Hay que aprender a ajustar las capacidades de uno mismo con el proyecto al que se presenta. Nos hemos complicado la vida mucho por hacerlo de la forma más "correcta" posible y esa es una buena aproximación en esencia, creemos que una buena base conlleva a un producto mejor y sobre el cuál es más fácil trabajar, allanarnos el camino a nosotros mismos lo máximo posible. El problema se encuentra cuando no se estima correctamente el trabajo que va a conllevar la creación de esa infraestructura, y cuando el trabajo para facilitarnos el trabajo es más duro que el problema inicial, lo que se conoce como _Overengineering_. No nos equivoquemos, ¿creemos que hemos hecho un trabajo en vano?¿o que la ruta que llevábamos era errónea? No, no es así, esa es la que creemos la forma correcta de hacer las cosas, **¡pero!** no para un proyecto con tan corto plazo. Es de justicia decir que los mayores retrasos que se han producido han sido imprevistos de carácter personal y que escapaban de nuestro poder de actuación, y que los problemas técnicos que hemos afrontado eran de una complejidad considerable (más aún teniendo en cuenta que estábamos aprendiendo la tecnología a usar mientras la usábamos). Por todo ello estamos orgullosos de lo que hemos conseguido y tenemos la certeza que con más tiempo o mejor suerte tendríamos un producto competente, pues, sobretodo en la última semana, hemos allanado muchísimo el camino, consiguiendo que la arquitectura que días atrás era sólo un amasijo de parámetros _hardcoded_ y llamadas a funciones inexistentes ahora tenga sentido y funcione de una forma relativamente intuitiva y con bastante capacidad de ampliación. Aún con todo ello el juego **no** funciona, o no como debería, faltan funcionalidades y cualidades que le den la connotación de juego, es decir, _actualmente tenemos una aplicación, no un juego_ puesto que no hay gameplay ni objetivos ni nada que pueda darle a un usuario un significado para ejecutarla, en todo caso se podría considerar un ejercicio técnico.

 ##### A continuación una lista de las funcionalidades que faltan por implementar para poder considerarse un juego:
 - Las colisiones entre las balas del jugador y los enemigos. Aquí tenemos una implementación no funcional pues en cuanto que generamos una bala del player ésta automáticamente "colisiona" con el enemigo, o eso dice el programa al menos. Para detectar las colisiones utilizamos el método de overlap, que está probado que funciona correctamente, pues funciona con las balas del enemigo y el player. Algo del forEach no acaba de funcionar como debería o creemos que debería
 - A raíz de lo anterior no hay puntuación o paso de nivel. Aunque estén implementados otros niveles y la API para poder pasar de nivel, el acto que daría paso a ello sería la destrucción de los enemigos, por lo tanto no es algo que funcione ya que tenemos un grifo con tubería, el grifo funciona, pero no le llega el agua.
 - También en estrecha relación con lo anterior no tenemos HUD, ya que en nuestro diseño inicial teníamos pensado una HUD sencilla en la que solo se mostrase la vida y puntuación el jugador, además de un botón para abrir el menú de pausa. Aunque es algo que con el actual conocimiento que tenemos de las herramientas bastante sencillo de implementar.
 - Menús funcionales. Tenemos un menú principal, pero solo tiene un boton para iniciar el juego. Harían falta otro menú en el que elegir nivel y una tienda (se habla más en profundidad sobre ello a continuación).
 - Diferentes armas para el jugador. Hicimos una breve aproximación en la arquitectura, pero está seriamente desfasada. El jugador solo dispara un tipo de bala (puesto que es lo más básico que hemos conseguido hacer funcionar) no sería algo con mucho coste de implementación persé, pero conllevaría a la implementación de una tienda, lo cuál **si es costoso**
 - Y por último, una nivelación del juego. Actualmente tenemos valores bastantes pseudo-aleatorios con el fin de ver la funcionalidad del código, no su diversión, esto ha sido imposible por razones obvias (no se puede nivelar un juego que no existe).