# Introducción

A continuación te proponemos un caso práctico real de lo que te vas a encontrar en tu día a día en el área de Tecnología. El objetivo del área es aportar soluciones end-to-end, incluyendo además áreas relacionadas con la cultura o la metodología.

La idea es que lo trabajes el tiempo que puedas (o que dispongas) y que nos pueda servir como un guíon en una posible entrevista técnica en la que tendrás que defender la solución propuesta u otras alternativas que creas relevantes. 

No buscamos un formato muy vistoso, buscamos contenido y fondo. Buscamos que haya debate y una conversación técnica en la que todos podamos aprender y no te sientas juzgado. Queremos hablar sobre un problema habitual en muchas compañías y cómo se trabajaría, entendiendo que puede haber  varios enfoques y cada uno con sus pros y sus contras.

No dediques mucho tiempo a dar forma a la presentación de la solución. Si quieres incluir algún diagrama o esquema, puedes hacerlo en un papel y adjuntarlo como una foto.

# Caso práctico

A continuación se describe la situación de un cliente en el momento actual. A la hora de afrontar el caso práctico debes tener en la cuenta los puntos comentados en el apartado siguiente de "Contexto del problema"

## Contexto del problema

### Organización

Nos encontramos ante una compañía del **sector asegurador**, de tamaño medio-grande, que comercializa productos tanto para el cliente particular como para otras aseguradoras o entidades bancarias. Actualmente su negocio es nacional pero se está planteando expandir el negocio tanto a clientes como compañías extranjeras.

Organizativamente, Negocio y TI están muy distantes, trabajando como si fueran cliente y proveedor. Normalmente, Negocio lanza iniciativas que son analizadas por TI para decidir si son viables técnicamente y si se van a realizar de manera interna por el equipo de desarrollo interno o bien, se derivarán a proveedores externos.



### ¿Cómo está organizado Negocio?

Dentro de la __estructura propia de Negocio__ podemos encontrar, a nivel transversal:

- Marketing: encargado de promocionar los diferentes productos de los ramos y de la información general de la compañía
- Controlling: es el responsable de coordinar los diferentes departamentos, presupuestos, etc. 
- Recursos Humanos: responsable de todo lo que tiene que ver con gestión de personas y de sus condiciones de trabajo

Después, la compañía está organizada alrededor de "ramos". En concreto: salud, automovil, hogar y productos financieros. Cada una funciona casi como una empresa independiente, sin mucha relación entre ellos. Dentro de cada ramo, encontramos replicada la siguiente estructura:

- Productos: encargado de decidir que productos se comercializan y con qué prestaciones
- Contratación y clientes: encargado de la contratación y comercialización de los productos del ramo
- Atención a cliente: encargado de proporcionar ayuda a los clientes sobre esos productos concretos. Está especializado en el ramo y productos ofertados
- Tramitaciones: encargado de gestionar las tramitaciones asociadas a los siniestros y prestaciones de ese ramo
- Peritaciones: encargado de gestionar las peritaciones de los siniestros de ese ramo
- Proveedores de servicio: dependiendo del ramo, este departamente es diferente:
  - Talleres: en el ramo de siniestros existe también un departamento encargado de gestionar la relación con los diferentes talleres
  - Clínicas y hospitales: asociado al ramo de Salud, se encarga de las relaciones con las clínicas y centros
  - Bancos y gestoras: asociado al ramo financiero, son los encargados de gestionar las diferentes relaciones con los proveedores de productos financieros.
- Replicas de los departamentos transversales de marketing y controlling.



### ¿Cómo está organizado IT?

El __departamento de IT__ es un departamento transversal para dar servicio a todos los ramos. Hace unos años, existía un IT por ramo y un IT global. Con la entrada del nuevo CIO, se realizó una reestructuración para disponer de un IT global. Dentro del departamento de IT podemos encontrar la siguiente organización:

- Sistemas: encargado de todo lo que tiene que ver con infraestructura, comunicaciones y redes
- Seguridad: encargado de la seguridad global y de aplicaciones
- Desarrollo: responsable de la construcción interna de aplicaciones, del mantenimiento o de la gestión de los diferentes proveedores que construyen nuevas aplicaciones o mantienen las existentes. También es responsable de los diferentes productos de terceros que dan soporte a ciertas necesidades de Negocio.
- Arquitectura: responsable de la arquitectura empresarial y técnica que soporte las diferentes aplicaciones solicitadas por Negocio. Hace un papel de coordinador entre Sistemas, Seguridad y Desarrollo. 



### ¿Cuál es la relación Negocio - IT?

Como se ha comentado, Negocio e IT son dos áreas totalmente independientes. Negocio determina que nuevos productos o mejoras funcionales debe implementar la compañía para seguir siendo competitivo en el mercado. No interviene en las decisiones de tecnología. La compañía se basa en iniciativas, proyectos y mantenimientos. 

#### Iniciativas y Proyectos

1) En el último trimestre de cada año, Negocio genera una serie de iniciativas y proyectos a cubrir en el siguiente año, teniendo en cuenta las necesidades actuales y los proyectos en curso en ese año. Prioriza cada iniciativa/proyecto y asigna plazo máximo para disponer de esa característica.

2) Las iniciativas son estudiadas por TI, principalmente por Desarrollo, determinando si es posible realizarlas con la tecnología existente y conocida por el departamento. Arquitectura y Sistemas también estudian esas iniciativas y proponen soluciones, riesgos, nuevos sistemas o puntos a tener en cuenta

3) Desarrollo, en caso afirmativo, realiza una estimación incial de esfuerzo y coste para realizar la iniciativa en el plazo determinado por Negocio y se lo comunica a Negocio para que puedan reservar el presupuesto. En esa estimación se incluyen nueva infraestructura, sistemas o arquitecturas. En caso de que Desarrollo estime que no es posible realizar alguna iniciativa, se lo comunica a Negocio de forma razonada.

#### Mantenimientos

En el caso de los mantenimientos, los evolutivos se trabajan de una forma similar. Negocio realiza una lista de evolutivos prioridad y lo comunica a Desarrollo para que los diferentes equipos de mantenimiento puedan realizar sus previsiones.

En el caso de los correctivos, todos los años se realiza un estudio bugs detectados para que Desarrollo realice su previsión teniendo en cuenta el tiempo medio de resolución de los mismos. Se ha detectado que el número de bugs aumenta de año en año y de la misma forma, el tiempo medio de resolución.



### ¿Cuál es la sensación de Negocio?

En el momento actual, Negocio muestra su descontento con el departamento de IT por las siguientes razones:

- Las aplicaciones son muy pobres a nivel visual, con un recursos muy reducidos y no pudiéndose ejecutar algunas en navegadores modernos debido a que algunas están realizadas en Flex (Flash). Esto es una limitación bastante grande a la hora de proporcionar aplicaciones a otras compañías y también para ofrecer productos digitales a un público joven

- Los desarrollos, a menudo, no cumplen con las especificaciones indicadas inicialmente  y necesitan una fase de pruebas muy larga antes de su puesta en producción y apertura a clientes (internos o externos)

- El número de bugs de los desarrollos es alto, aumentando la proporción cada año

- El tiempo medio de resolución de los bugs, desde su detección hasta su corrección y puesta en producción, es bastante alto, siendo de 9 jornadas. Se reclama un tiempo medio de 2 o 3 jornadas

- Negocio también indica que detecta que el rendimiento de las aplicaciones no es el deseado por ciertas áreas:

  - Tarificación en general
  - Citas en el ramo de Salud
  - Asistencia en Viaje en el área de Siniestros en fechas señaladas
  - Posición global o dashboard de usuario en el área de productos financieros.

- Hay ciertas áreas en las que se requiere mayor velocidad a la hora de ofrecer funcionalidades al usuario, como puede ser la de productos financieros o salud y otras, en las que no se necesita tal rapidez. En el momento actual, no hay diferenciación y las nuevas funcionalidades (iniciativas o mantenimientos evolutivos) siguen el mismo ritmo y plazos, perdiendo competitividad en ciertos sectores

- Los desarrollos tienen costes muy altos y no se obtienen resultados hasta que el proyecto está muy avanzado

- Realizar prototipos en plazos cortos para probar ciertas funcionalidades con algunos usuarios no es posible. Lo mismo ocurriría con testing A/B

- La venta cruzada es muy complicada ya que no existe un intercambio de información entre los diferentes ramos ni es posible determinar en tiempo real si un cliente tiene varios productos contratados

  

### ¿Qué demanda IT?

IT está de acuerdo con los puntos indicados por Negocio y lanza una serie de iniciativas para mejorar el funcionamiento, partiendo de la siguiente situación:

- Toda la infraestructura es física, teniendo que optimizar muy bien los recursos para no entrar en un sobrecoste o  consumo de recursos poco eficiente, teniendo máquinas al mínimo de su capacidad. 
- La instalación de nuevas máquinas físicas es costosa en tiempo ya que requiere su contratación a terceros, instalación en el CPD propio y mucha burocracia asociada.
- La lógica CORE en la mayoría de las ramas se encuentra en HOST. Algunos son programas y rutinas con muchos años de antigüedad
- Existen varias arquitecturas dentro de la casa:
  - HOST: como se ha comentado es la que contiene la mayoría de la lógica CORE de todos los ramos. Se intenta no añadir lógica a este modelo ya que resulta muy costoso en mantenimiento y ejecución.
  - Arquitectura v1: desarrollo totalmente en JEE (1.6), apoyándose en frameworks como Spring, versión 3.x. A nivel de base de datos se cuenta con ORACLE y accede al HOST mediante un conector (jar) que permite invocar rutinas y programas COBOL.
  - Arquitectura v2: desarrollo basado en JEE con la parte frontal, RIA, desacoplada mediante Adobe Flex que permite realizar la capa frontal de forma independiente al backend. Adobe Flex ya no dispone de soporte y las aplicaciones realizadas se compilan a Flash, por lo que no están soportadas por algunos navegadores modernos. Se instaló el bus de servicios de ORACLE (OSB) de forma que se construyan servicios web SOAP para ser consumidos por las aplicaciones frontales. La conexión con el HOST se realiza de forma similar a la Arquitectura v1, es decir mediante un conector (jar) que se incluye dentro de los servicios. 
- A nivel de desarrollo, se trabaja en grandes aplicaciones frontales, muy complejas. A nivel de backend, los desarrollos en Arquitecura v1 son totalmente monolíticos mientras que en la Arquitectura v2 se realiza una división en servicios web en la parte backend. La división la realizan los propios equipos de desarrollo.
- Siempre se trabaja en modo proyecto cerrado independientemente de que sea realizado por un proveedor externo o por personal interno. 
- A nivel de CI/CD, IT comenta que están muy limitados por diferentes razones:
  - Sólo se usa para la tarea de construcción y calidad de código mediante Sonar.
  - Los equipos usan ramas de muy larga duración y no realizan commits frecuentes.
  - Se decidió que para evitar errores, los merges con la rama master los hace únicamente Arquitectura, disponiendo de una persona dedicada a ello y que se reune con los equipos en el caso de conflictos.
  - No se utiliza de forma automática sino que el equipo es responsable de ejecutar los jobs de construcción.
  - No existen despliegues automáticos en entornos superiores a desarrollo. Para promocionar a entornos de PRE o PRO es necesario que Negocio lo autorice de forma manual ya que utiliza el entorno de PRE para realizar pruebas y no quiere un entorno inestable.
  - No existen juegos de datos de prueba, por lo que la automatización de pruebas es muy complicada
  - Algunas rutinas COBOL no pueden ser probadas de forma fiable en entornos no PRODUCTIVOS ya que los datos de los entornos COBOL son muy escasos y poco trabajados.
- A nivel de ejecución, las aplicaciones y servicios se instalan en los servidores Weblogic, estableciendo alta disponibilidad y balanceo únicamente en el entorno de PRO.



### ¿Cuál es la estrategia de la compañía?

La compañía marca una estrategia a medio plazo con los siguientes puntos:

- mejorar los canales por los que se ofrecen sus productos y poder llegar así a un público más joven
- mejorar los canales para poder ofrecer interfaces a otras compañías para que comercialicen sus productos
- mejorar los tiempos de desarrollo de soluciones y en especial los asociados a infraestructura
- disminuir el número de bugs detectados en nuevos desarrollos y mejorar el tiempo medio de resolución (incluyendo puesta en producción) a 2-3 días
- disminuir el coste asociado a los mantenimientos COBOL en un 30% migrando funcionalidades a las nuevas arquitecturas
- posibilidad de ofrecer productos digitales en modo "prototipo rápido" para ver si son aceptados por los clientes o no
- mejora de venta cruzada y posibilidad de reaccionar a situaciones que ocurren al cliente en los diferentes ramos. Por ejemplo, si el cliente contrata un producto financiero de ahorro con el objetivo de comprarse un coche, poder ofrecerle también un seguro en el momento que retira el dinero.
- rendimiento acorde a las necesidades concretas de la funcionalidad de Negocio y no del conjunto, es decir, dotar de mayor capacidad de escalado o de cómputo a aquellas partes del negocio que lo necesiten



## Cuestiones a resolver

Una vez descrito brevemente el contexto y conocida la estrategia de la compañía, nos gustaría tener un debate alrededor de las siguientes puntos:

- **Propuesta de Arquitectura end-to-end**

  Teniendo en cuenta lo comentado por Negocio y por IT, ¿qué plantearías a nivel de arquitectura (desarrollo y ejecución) para mejorar las capacidades de la compañía. Dentro de esta Arquitectura end-to-end será necesario establecer:

  - Arquitectura de desarrollo: 

    - cómo se van a realizar las aplicaciones nuevas, 
    - con qué herramientas o tecnologías
    - cómo será la convivencia con el resto de arquitecturas
    - ...
    - ...

  - Arquitectura de ejecución:

    - Entornos
    - Monitorización y control de errores (de aplicación y de máquinas)
    - ...
    - ...

  - Seguridad

  - CI/CD

  - Metodología
  
  - Roadmap: ¿cómo sería el roadmap de mejoras/cambios/etc propuestos para la organización de forma que no se pierda capacidad de Negocio?

  - ...

  - ...

    

- **Implementación**

  Como buen Arquitecto de Soluciones será necesario que lideres el proceso de transformación tecnológica mediante labores de desarrollo y de establecimiento de buenas prácticas. Por ello te pedimos que codifiques una sencilla PoC end-to-end, en la que aplicar algunos de los principios de la arquitectura. 

  El MVP debe contener cómo mínimo:

  - Una aplicación frontal en la que exista una vista que muestre un listado de pólizas. Al hacer click en una de ellas se mostrará su detalle en una vista nueva. El detalle contendrá datos relativos a la propia póliza (producto, prima,...,etc), datos del tomador (nombre, apellidos, teléfono y email) y datos del vehículo asegurado. En esa vista de detalle se permitirá únicamente la edición de los datos del tomador, persistiendo los cambios en base de datos.
  - Servicios que den soporte a la vistas y las operaciones necesarias

  

  Extras opcionales:

  - Autenticación y seguridad
  - CI/CD