# Tema 1: Introducción

### 2. Requisitos de las aplicaciones multimedia en red
Las aplicaciones multimedia tienen como características:
- Necesidad de ancho de banda. Una tráfico inelástico o elástico para la transferencia de paquetes.
- Fiabilidad en la transferencia de datos. Evaluación si es necesario que lleguen o no todos los paquetes.
- Requisitos de tiempo acotado. Aplicaicones como telefonia IP, requiere que el tiempo transcurrido entre el envío y la recepción de un paquete sea inferior a un umbral estricto.

### 3.1. Servicios de transporte en TCP/IP

Como sabemos, el modelo OSI está dividido en diferentes capas. La diapositiva 10 tiene los diferentes protocolos de las diferentes capas.
- Protocolo HTTP: Permite la descarga de ficheros o subida de estos. No guarda el estado para que el servidor no ocupe mucha memoria. Para ello se inventaron las cookies, que es la asignación de un número guardado en el server para identificar algo. Como novedad Google quiere implementar una sustitución de las cookies llamado sandbox.
- Protocolo DNS: Solicita la IP de un dominio.
- Router con caché dns, que guardan la dirección IP de los dominios utilizados en la red local. Es un ejemplo de edge computing.

Los principales protocolos en la capa de transporte son UDP y TCP.

#### 3.1.1. TCP

Servicio orientado a conexión (requiere una fase de establecimiento y otra de cierre de la conexión) Es un transporte fiable y ordenado, pero no ofrece garantía del retardo de recepción d elos datos transmitidos.

#### 3.1.2. UDP

Es un servicio no orientado a conexión (como cuando enviamos una postal), por lo que no es fiable ya que pueden perderse paquetes sin ningún tipo de realimentación. Permite una tasa de transmisión fija.

### 4. Definiciones de Calidad de Servicio (QoS)

Es el efecto colectivo del rendimiento del servicio dado, que determina el grado de satisfacción de un usuario del servicio. Por lo tanto es subjetivo, pero comprobado con valores de parámetros objetivos.

Sin embargo, según quien la mida hay distintos tipos:
- **QoS planificada**. La que el proveedor intenta ofrecer.
- **QoS conseguida**. La que realmente se proporciona.
- **QoS percibida por el usuario**. La calidad percibida por un usuario de forma diferente a la QoS conseguida medida por el proveedor.
- **QoS inferida**. Es la calidad que determina el proveedor del servicio como resultado de estudios sobre la opinión de los usuarios y su correspondencia con la QoS conseguida.

#### 4.1.1. Tasa de transferencia (throughtput)
Cantidad de digitos binarios que la red es capaz de aceptar y entregar la red por unidad de tiempo.

- CBR (Tasa de bits contante)
- VBR (Tasa de bits variable). En esta hay tasa de bits pico que hay que evaluarlos para añadir más bits en ese pico para la transferencia.

Se utiliza el término tasa de transferencia ya que ancho de banda es más referido a la capacidad de la red y no a los datos enviados.

##### *Nota*:

Supuesto jugador de esports, se pasó de adsl a fibra óptica. Esto es porque jugaba en un servidor chino, ya que tenía retardos. Esto es debido a la velocidad de propagación. Ejemplo: No importa el ancho del carril, si no a que velocidad va. Diferencia entre velocidad de propagación y de transferencia.

#### 4.1.2. Retardo extremo a extremo
Componentes:
- Retardo de acceso (tiempo transcurrido hasta que el medio puede aceptar la transmisión del vloque dde datos)
- Tiempo de transmisión (tiempo requerido en transmitir todos los bits del bloque de datos)
- Tiempo de propagación (tiempo transcurrido entre la transmisión de un bit y su llegada al otro extremo de un enlace)
Tiempo de ida y vuelta (RTT). Medición del envío de paquetes ya que para ello hay que enviar y recibir el paquete para medir el tiempo con el reloj del mismo ordenador, ya que el tiempo de un ordenador a otro puede variar.
#### 4.1.3. Variación de retardo (jitter)
Es la diferencia de retardo entre paquetes. Esto puede ocurrir por el tiempo de acceso al medio, de espera en control de flujo y el tiempo de espera en cola.
