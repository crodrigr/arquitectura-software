# Arquitectura de software

<br>

## 1. ¿Qué es la arquitectura de software?

***No existe un consenso para definir con exactitud que es la arquitectura de software, por el contrario, existe diversas publicaciones donde se dan definiciones diferentes, lo que hace complicado decir con exactitud que es la arquitectura de software.***


![image](https://github.com/crodrigr/arquitectura-software/assets/31961588/f64def9c-eb56-43fd-8b3d-15d3138f5242)

#### [¿Qué es la arquitectura de software? :movie_camera:](https://www.youtube.com/watch?v=7ukajubprdE&list=PLFHx3afTdaY0hvX2NXRxMVM3j5sk-3aE3&index=2)

<br>


## 2. ¿Qué son los patrones de diseño?

![image](https://github.com/crodrigr/arquitectura-software/assets/31961588/b1670697-fe6f-4538-8588-29741f2788b2)


#### [¿Qué son los patrones de diseño? :movie_camera:](https://www.youtube.com/watch?v=pk-lawTRbmg)

![image](https://github.com/crodrigr/arquitectura-software/assets/31961588/584adfd8-0e99-47ff-b728-7a5d0655fe8f)

**Patrones de diseño y patrones arquitectónicos**

![image](https://github.com/crodrigr/arquitectura-software/assets/31961588/a1926874-7e0c-4f35-bb59-eaa8c749eb65)

#### [¿Cuál es la iferencia entre patrones de diseño y patrones arquitectónicos :movie_camera:](https://www.youtube.com/watch?v=VyMRGf0Dji4&list=PLFHx3afTdaY3pAFWNUEJRCeiIw4raCi3U&index=9)
#### [¿Para qué sirven los Patrones de Arquitectura? :movie_camera:](https://www.youtube.com/watch?v=87lBMvk75eM&list=PLFHx3afTdaY0KR3h_NVjoWajr2OLRiqPv)

### 2.1 ¿Cómo diferenciar un patrón arquitectónico?

Los patrones arquitectónicos son fáciles de reconocer debido a que tiene un impacto global sobre la aplicación, e incluso, el patrón rige la forma de trabajar o
comunicarse con otros componentes, es por ello que a cualquier cambio que se realice sobre ellos tendrá un impacto directo sobre el componente, e incluso, podría tener afectaciones con los componentes relacionados.

Un ejemplo típico de un patrón arquitectónico es el denominado “Arquitectura en 3 capas”, el cual consiste en separar la aplicación 3 capas diferentes, las cuales corresponden a la capa de presentación, capa de negocio y capa de datos:

**Arquitectura en tres capas**

![image](https://github.com/crodrigr/arquitectura-software/assets/31961588/a4a09ebc-94fc-46b7-aa5a-016ed21a2059)

En la imagen anterior podemos apreciar un componte que implementa la arquitectura de 3 capas, dicho patrón arquitectónico tiene la finalidad de separar la aplicación por capas, con la finalidad de que cada capa realiza una tarea específica. La capa de presentación tiene la tarea de generar las vistas, la capa de negocio tiene la responsabilidad de implementar la lógica de negocio, cómo implementar las operaciones, realizar cálculos, validaciones, etc, por último, la capa de datos tiene la responsabilidad de interactuar con la base de datos, como
guardar, actualizar o recuperar información de la base de datos.

Cuando el usuario entra a la aplicación, lo hará a través de la capa de presentación, pero a medida que interactúe con la aplicación, este requerirá ir a la capa de negocio para consumir los datos, finalmente la capa de datos es la que realizará las consultas a la base de datos.

Dicho lo anterior, si alguna de las 3 capas falla, tendremos una falla total de la aplicación, ya que, si la capa de presentación falla, entonces el usuario no podrá ver nada, si la capa de negocios falla, entonces la aplicación no podrá guardar o solicitar información a la base de datos y finalmente, si la capa de datos falla, entonces no podremos recuperar ni actualizar información de la base de datos. En cualquiera de los casos, en usuario quedará inhabilitado para usar la aplicación,tendiendo con ello una falla total de la aplicación.

Por otra parte, si decidimos cambiar el patrón arquitectónico una vez que la aplicación ha sido construida, tendremos un impacto mayor, pues tendremos que modificar todas las vistas para ya no usar la capa de negocios, la capa de negocio tendrá que cambiar para ya no acceder a la capa de datos, y la capa de datos quizás tenga que cambiar para adaptarse al nuevo patrón arquitectónico, sea como sea, la aplicación tendrá un fuerte impacto. Además del impacto que tendrá el componente, hay patrones que su modificación podría impactar a otros componentes, incluso, compontes externos que están fuera de nuestro dominio, lo que complicaría aún más las cosas.

<br>


## 3. ¿Qué son los estilos arquitectónicos?

El último término que deberemos aprender por ahora son los estilos arquitectónicos, los cuales también son diferentes a los patrones arquitectónicos. Para comprender que es un estilo arquitectónico, es necesario regresarnos un poco a la arquitectura tradicional (construcción), para ellos, un estilo arquitectónico es un método específico de construcción, caracterizado por las características que lo hacen notable y se distingue por las características que hacen que un edificio u otra estructura sea notable o históricamente identificable.

En el software aplica exactamente igual, pues un estilo arquitectónico determina las características que debe tener un componente que utilice ese estilo, lo cual hace que sea fácilmente reconocible. De la misma forma que podemos determinar a qué periodo de la historia pertenece una construcción al observar sus características físicas, materiales o método de construcción, en el software podemos determinar que estilo de arquitectura sigue un componente al observar sus características. Entonces, ¿Qué son los estilos arquitectónicos?, veamos algunas definiciones:

![image](https://github.com/crodrigr/arquitectura-software/assets/31961588/c5622123-24e6-4b4e-abcf-43d94e89d4de)

![image](https://github.com/crodrigr/arquitectura-software/assets/31961588/72ccf8cb-272e-4d74-8ec2-085d95d68274)

![image](https://github.com/crodrigr/arquitectura-software/assets/31961588/dd92ffe5-4d89-4891-bbec-3a44f1272b94)

#### [Estilos de arquitecura de software :movie_camera:](https://www.youtube.com/watch?v=PK9TTcTosTw)


### 3.1 La relación entre patrones de diseño, arquitectónicos y estilos arquitectónicos

Para una gran mayoría de los arquitectos, incluso experimentados, les es complicado diferenciar con exactitud que es un patrón de diseño, un patrón arquitectónico y un estilo arquitectónico, debido principalmente a que, como ya vimos, no existe definiciones concretas de cada uno, además, existe una línea muy delgada que separa a estos tres conceptos.

Para comprender mejor estos conceptos será necesario de apoyarnos de la siguiente imagen:


![image](https://github.com/crodrigr/arquitectura-software/assets/31961588/ded4fc19-ef72-4c8f-bf8b-edff99344e78)

**La relación entre patrones de diseño, patrones arquitectónicos y estilos arquitectónicos**

Como podemos ver en la imagen, los estilos arquitectónicos son los de más alto nivel, y sirve como base para implementar muchos de los patrones arquitectónicos que conocemos, de la misma forma, un patrón arquitectónico puede ser implementado utilizando uno o más patrones de diseño. De esta forma, tenemos que los patrones de diseño son el tipo de patrón más específico y que centra en resolver como las clases se crean, estructura, relacionan y se comportan en tiempo de ejecución, por otra parte, los patrones arquitectónicos se enfocan en los componentes y como se relacionan entre sí, finalmente, los estilos arquitectónicos son marcos de referencia mediante los cuales es posible basarse para crear aplicaciones que compartan ciertas características.

Aun con esta explicación, siempre existe una especial confusión entre los patrones arquitectónicos y los estilos arquitectónicos, es por ello que debemos de recordar que un patrón arquitectónico existe para resolver un problema recurrente, mientras que los estilos arquitectónicos no existen para resolver un problema concreto, si no que más bien sirve para nombrar un diseño arquitectónico recurrente.

![image](https://github.com/crodrigr/arquitectura-software/assets/31961588/309959a9-bbb2-4d22-b80c-a8a74315b5da)

A pesar de que estos 3 conceptos tengan un propósito diferente (aunque relacionado), es importante que cualquier arquitecto de software entienda la diferencia, pues confundirlos puede ser un error grave, es por ello que en este libro nos centraremos en aprender de lleno los principales estilos y patrones arquitectónicos, dejando de lado los patrones de diseño, pues asumimos que a
estas alturas ya los dominas.
