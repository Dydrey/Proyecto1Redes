# Ejecutar el proyecto:

- Para ejecutar el proyecto, basta con abrir una terminal dentro de la carpeta raíz del mismo y ejecutar el siguiente comando:

 docker-compose up

## Pruebas realizadas:

- Las pruebas realizadas fueron manuales, con el fin de combrobar la creación de la red y la comunicación entre los contenedores

 - Para verificar que la red se creara, se ejecutaba el comando:
  
  docker network ls
  docker network inspect <nombre de la red>

 - Para verificar la comunicación entre los contenedores, se ejecutaba lo siguiente:

  docker exec -it <nombre del contenedor>
       ping <ip de otro contendor>
  
# Conclusiones y recomendaciones

## Recomendaciones:

1. Utilizar contenedores creados desde 0 con Ubuntu o Alpine, la documentación de los contenedores ya construidos no suele ser muy precisa.

2. Tratar de aislar los contenedores de la red del host para que esta no interfiera en las configuraciones de la red lan.

3. Se recomienda utilizar Ubuntu 18, tanto para la virtualización con Docker como para la creación de las imagenes, puesto que muchos de los modulos son más estables en esta versión.

4. Si se utilizan imágenes ya existentes en Docker hub se recomienda leer la documentación y asegurarse que la implementación tenga el comportamiento que se necesita para su uso.

5. Se recomienda utilizar herramientas para comprobar el funcionamiento de los contenedores, como ping o nslookup.

6. Se recomienda la creación de contenedores efímeros (que el contenedor se puede detener y destruir, luego reconstruir y reemplazar con una instalación y configuración mínimas absolutas).

7. Al iniciar este proyecto se recomienda tener conocimientos básicos o investigar sobre la herramienta Docker, esto facilitará la curva de aprendizaje presente en el proyecto.

8. Se recomienda el uso de una maquina virtual para realizar las configuraciones necesarias de la red, esto para evitar desconfigurar las opciones de red del sistema en la maquina fisica.

9. Se recomienda hacer un uso adecuado de la memoria tanto de la computadora como de la maquina virtual, ya que la mala administración de estas puede afectar el rendimiento y ralentizar el proceso del proyecto.

10. Ir poco a poco creando y conectando los contenedores y probando que su funcionamiento sea el esparado, antes de seguir integrando más funcionalidad a la red.

## Conclusiones:

1. Mucha de la documentación encontrada no era del todo clara y a la hora de replicar guías, incluso de las páginas oficiales, estas contenian errores.

2. La virtualización de conetenedores mediante docker suele ser un proceso bastante complejo, y la generación de documentos tipo Dockerfile se hace bastante pesada debido a que muchas de las guías están pensadas para ser ejecutadas directamente en terminal.

3. Al utilizar imagenes basadas en linux, ubuntu en nuestro caso, con funcionalidades minimas, era necesario instalar las herramientas complementarias para poder utilizar ciertos comandos.

4. Por la misma razón anterior, muchas veces al intentar correr algún comando, fallaban funciones en bibliotecas del sistema o de otros modulos, lo cual hacía muy dificil poder dar con el error.

5. El uso de docker-compose ayuda a automatizar la ejecución de comandos y los reduce a ejecutar un par de lineas en terminal, lo cual permite estandarizar la ejecución de ciertos proyectos.

6. La creación de contenedores ayuda a simular de forma más precisa una situación más real, donde tengo diversas maquinas prestando diferentes servicios.

7. La curva de aprendizaje para el uso de docker pudo haber sido un factor importante en el desarrollo del proyecto, la creación y el manejo de lo Dockerfiles fue un proceso complicado de entender.

8. Consideramos que el uso de otro ambiente o programa más enfocado en el desarrollo de la red como tal pudo haber ayudado más en el entendimiento de la creación de las redes..

9. A pesar de que se entendía los conceptos y el funcionamiento de cada una de las partes que se tenía que configurar en la red, no se logró la implementación de estos por las complicaciones con archivos que no se encontraban dentro de las imágenes de Ubuntu.

10. Aunque las imagenes de linux utilizadas podían carecer de funcionalidades importantes, el uso de imagenes básicas facilita el aprovechamiento de recursos que hace la maquina al utilizar los contendores, además de ser más configurables.

11. A pesar de haber mucha información y documentación sobre Docker en internet, no toda era compatible con sí misma, ya que muchas veces un comando no funcionaba y requería realizar más investigación para poder resolver el problema y poder continuar con la ejecución.
