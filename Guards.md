# Que es un Guard
Los Guards en Angular, son de alguna manera: middlewares que se ejecutan antes de cargar una ruta y determinan si se puede cargar dicha ruta o no. Existen 4 tipos diferentes de Guards (o combinaciones de estos) que son los siguientes:

1.  (_CanActivate_) Antes de cargar los componentes de la ruta.
2.  (_CanLoad_) Antes de cargar los recursos (assets) de la ruta.
3.  (_CanDeactivate_) Antes de intentar salir de la ruta actual (usualmente utilizado para evitar salir de una ruta, si no se han guardado los datos).
4.  (_CanActivateChild_) Antes de cargar las rutas hijas de la ruta actual.

Como middleware, estos componentes se ejecutan de manera intermedia antes de determinadas acciones y si retorna `true` la ruta seguiría su carga normal, en caso negativo, el Guard retornaría `false` y la ruta no se cargaría. Generalmente en caso de que no se cumpla la condición del Guard, se suele hacer una redirección a la ruta anterior o a una ruta definida como la interfaz de autenticación.

## ¿Por qué utilizar Guards?

Una de las ventajas de utilizarlos, es que al no cargar la ruta evitamos que los usuarios vean una interfaz a la que no tienen acceso (aunque sea por unos pocos milisegundos). Por otra parte, con estos componentes es posible estructurar el código de la aplicación de una manera más organizada y donde la lógica de la ruta está en la ruta en sí y la lógica de permisos y acceso a recursos se encuentra aislada en estos componentes.

## ¿Cómo utiliza Angular los Guards?

Empezaremos con la creación de un Guard. Para crear un Guard es posible hacerlo de manera manual, pero angular-cli provee un generador muy bueno y que de manera automática genera el Guard junto a las pruebas del mismo. Para generar el Guard solo es necesario abrir un terminal en la carpeta que se desea y ejecutar el siguiente comando:

	$ ng generate guard <guard-name>

Una vez ejecutado el comando anterior, dan a elegir cuál de los 4 tipos de Guard deseas generar y una vez seleccionado, este es creado junto a su archivo de pruebas unitarias.


