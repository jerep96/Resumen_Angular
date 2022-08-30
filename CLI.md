# CLI
Angular CLI es un Command Line Interface (interfaz en línea de comandos, en español), desarrollada por los equipos de Angular. Este CLI permite crear proyectos en los que el CLI podrá añadir archivos y más exactamente, entidades Angular. Será posible añadir módulos, componentes, servicios o directivas en una línea de comandos.

Pero esto no es todo. Un proyecto creado con Angular CLI se configura por defecto para funcionar con muchas tareas transversales que implica una aplicación web TypeScript. Aquí hablamos de bundling de las fuentes, de minificación, así como de herramientas que permiten probar su aplicación o incluso desplegarla.

El bundling es la operación que consiste en poner en común las diferentes partes de la aplicación con el objetivo de formar un único paquete final: un bundle. El objetivo de la minificación es reducir el tamaño del código fuente, renombrando las variables y funciones por nombres más cortos, sin que esto tenga un impacto sobre el funcionamiento del código.

### Ng Serve

	ng serve

Ng serve nos permite ejecutar un servidor. Nuestra aplicación es accesible mediante un navegador en localhost y el puerto por defecto 4200.

### Ng generate

	ng generate

Nos sirve para generar elementos angular. Podemos crear clases, módulos, componentes, servicios, guards, Interfaces, pipes etc.

### Ng test

	ng test

Se usan para ejecutar los tests.

### Ng build

	ng build

Una aplicación no es muy útil si no la podemos desplegar a los usuarios, así que ng build nos ayuda en eso.

Al escribir ng build se nos crea una carpeta dist con lo compilado de nuestra aplicación.
La idea es que ng build también nos permite hacer más cosas enfocadas a desplegar en producción:

- Minify/uglify
- Tree Shaking
- Compilación anticipada

Hace el minify uglify, es decir, reduce el tamaño del código, quitando los espacios en blanco y acortando el nombre de las variables.
Realiza Tree Shaking que es una técnica para eliminar el código inaccesible.
Precompila el código de forma que el cliente no tenga que bajarse el compilador cuando visita la web