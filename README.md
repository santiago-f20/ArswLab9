# ArswLab9

- ¿Cuáles son los tipos de balanceadores de carga en Azure y en qué se diferencian?, ¿Qué es SKU, qué tipos hay y en qué se diferencian?, ¿Por qué el balanceador de carga necesita una IP pública?
RTA: 
•	Balanceador de carga público puede proporcionar conexiones de salida para máquinas virtuales dentro de la red virtual. Estas conexiones se realizan mediante la traducción de sus direcciones IP privadas a direcciones IP públicas
•	Balanceador de carga interna se usa cuando se necesitan direcciones IP privadas solo en el front-end. Los equilibradores de carga internos se usan para equilibrar la carga del tráfico dentro de una red virtual. 
SKU son la combinación de una familia de máquinas virtuales y una especificación de hardware determinada, existen 3 tipos Básico, Estándar y Puerta de enlace

- ¿Cuál es el propósito del Backend Pool?
RTA: El backend pool es un componente crítico del load balancer. El backend pool es el grupo de recursos cuyo propposito es atender el tráfico para una regla de equilibrio de carga determinada.

- ¿Cuál es el propósito del Health Probe?
RTA: El proposito de Health Probe es proveer informes detallados de preparación, análisis de costos, y herramientas de planificación y asi determinar si una instancia del backend pool está en buen estado y puede recibir tráfico.

- Cuál es el propósito de la Load Balancing Rule? ¿Qué tipos de sesión persistente existen, por qué esto es importante y cómo puede afectar la escalabilidad del sistema?.
RTA: El propósito de la Load Balancing Rule es definir cómo se distribuye el tráfico entrante a todas las instancias dentro del grupo de back-end. Esta asigna una configuración de IP y un puerto front-end determinados a varias direcciones IP y puertos de back-end. Las reglas de Load Balancer son solo para el tráfico entrante.
Existen 2 tipos de sesión persistente:
•	Dirección IP de cliente (tupla de 2 elementos): especifica que la misma instancia de back-end controlará las solicitudes sucesivas de la misma dirección IP de cliente.
•	Dirección IP y protocolo de cliente (tupla de 3 elementos): especifica que la misma instancia de back-end controlará las solicitudes sucesivas de la combinación de la misma dirección IP y el mismo protocolo de cliente.


- ¿Qué es una Virtual Network? ¿Qué es una Subnet? ¿Para qué sirven los address space y address range?
RTA: Virtual Network son el tipo de redes que desplegamos en la nube, esta representa una red con todas sus características relacionadas tal y como si se tratase de una red física
Las subredes le permiten segmentar la red virtual en una o más subredes y asignar una parte del espacio de direcciones de la red virtual a cada subred.
Address space hace referencia al espacio de direcciones IP privado que se debe especificar haciendo uso de direcciones públicas y privadas, esto se formaliza cuando se crea una red virtual
Address range: El espacio de direcciones de una red virtual se compone de uno o más rangos de direcciones que no se superponen para el uso sobre la red virtual.


- ¿Qué son las Availability Zone y por qué seleccionamos 3 diferentes zonas?. ¿Qué significa que una IP sea zone-redundant?
RTA: Las regiones y zonas de disponibilidad de Azure están diseñadas para lograr la confiabilidad de sus cargas de trabajo críticas para el negocio. Azure mantiene múltiples geografías. Estas demarcaciones discretas definen la recuperación ante desastres y los límites de residencia de datos en una o varias regiones de Azure.  Las zonas de disponibilidad están diseñadas para que, si una zona se ve afectada, las dos zonas restantes admitan los servicios regionales, la capacidad y la alta disponibilidad.

- ¿Cuál es el propósito del Network Security Group?
RTA: Un Network Security Group es un firewall a nivel de red con un conjunto de reglas que gestiona permitiendo o denegando el tráfico de red tanto de entrada como de salida a los recursos de Azure que tengamos desplegados.
