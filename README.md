**Manual: Prueba de Ejecución de Aplicaciones Java con Tubería (|)**

CrearNumeros y OrdenarNumeros, utilizando el operador tubería (|) en la línea de comandos para conectar la salida de uno a la entrada del otro.


**1. Contexto de las Aplicaciones**

El trabajo asume que los dos fragmentos de código Java ya han sido guardados, compilados y empaquetados como archivos JAR ejecutables.


CrearNumeros: Genera una cantidad aleatoria de números enteros (entre 40 y 139) y los imprime en la salida estándar. El archivo ejecutable se denomina 


CrearNumeros.jar.


OrdenarNumeros: Lee enteros desde la entrada estándar hasta el final del flujo, los almacena, los ordena y los imprime. El archivo ejecutable se denomina 


OrdenarNumeros.jar.

**2. Preparación de los Archivos JAR**

Antes de la prueba, debes haber compilado el código (con javac) y empaquetado cada aplicación en su propio archivo JAR ejecutable (con el comando jar).

Asegúrate de tener listos los dos archivos JAR: 

CrearNumeros.jar (que genera los números) y OrdenarNumeros.jar (que lee y ordena).

Como ejemplo de preparación, se muestra que ambos archivos existen en el directorio 

D:\Temp.


**3. Prueba con el Operador Tubería (|)**

El operador tubería (|) es la clave para esta prueba. En la línea de comandos, este operador redirige la 

Salida Estándar (STDOUT) del programa de la izquierda para que se convierta en la Entrada Estándar (STDIN) del programa de la derecha.

**3.1. Ejecutar el Comando con Tubería**

Abre la terminal o símbolo del sistema y ejecuta la siguiente instrucción:


java -jar CrearNumeros.jar | java -jar OrdenarNumeros.jar
3.2. Explicación del Proceso
java -jar CrearNumeros.jar: Se inicia el primer programa. Este genera una serie de números aleatorios y los envía a su salida estándar.


| (Tubería): Intercepta la salida de CrearNumeros.jar.

java -jar OrdenarNumeros.jar: Se inicia el segundo programa. Este lee los números interceptados a través de su entrada estándar (usando, por ejemplo, 

br.readLine()), los almacena en un ArrayList, los ordena (Collections.sort(coleccion);) y luego debería imprimirlos ordenados.



3.3. Verificar la Salida
La terminal mostrará la lista de números generados, pero 

ordenados de forma ascendente, confirmando que ambos programas se comunicaron correctamente a través del operador tubería.
