# CRÉDITOS.
Código desarrollado por:
[Isur Ramírez](https://github.com/JorgeIsur)
Basado en el siguiente repositorio:
https://github.com/codigo-iot/ESP32CAM_MQTT-Basic.git

# ESP32CAM_MQTT-Basic
Este repositorio contiene el programa básico para conectar el ESP32CAM a MQTT, enviar y recibir mensajes.

Puedes encontrar el curso correspondiente a este ejercicio en el siguiente enlace.

https://edu.codigoiot.com/

### Requisitos
Para que el código de este repositorio funcione, es necesario contar con lo siguiente:

- ESP32CAM AI-Thinker
- Camara OV2640
- Programador FTDI con su cable
- IDE de Arduino 1.8 o superior
- Biblioteca PubSubClient para Arduino IDE.
- Biblioteca WiFi para Arduino IDE.
- Drivers privativos de expresiff para el ESP32.
- Broker Mosquitto funcionando de forma local en el puerto 1883
  Aunque también funciona con un broker público para própositos
  de experimentación.
- NodeRed corriendo de forma local en el puerto 1880.
- Nodos Dashboard para NodeRed.
- Cuenta de desarrollador de Twitter.
- Nodos Node-red-node-twitter para NodeRed.

### Guías
Para configurar correctamente la IDE de Arduino para trabajar con el ESP32CAM, puedes consultar el siguiente enlace.

https://edu.codigoiot.com/course/view.php?id=850

Para configurar correctamente tu broker mosquitto puedes consultar el siguiente enlace.

https://edu.codigoiot.com/course/view.php?id=818

Para configurar correctamente NodeRed puedes consultar el siguiente enlace.

https://edu.codigoiot.com/course/view.php?id=817

Puedes obtener la biblioteca PubSubClient desde el siguiente enlace.

https://github.com/knolleary/pubsubclient

El flow de NodeRed publica en el tema `rikoudousennin7`, por lo que deberás configurar los nodos MQTT para conectarse a estos temas y al broker de tu elección.
El programa .ino lee en el tema `rikoudousennin7`,por lo que deberás modificar el código para conectarse a estos temas y al broker de tu elección.
### Funcionamiento

Para observar el funcionamiento de este proyecto deberás realizar lo siguiente.

1. Carga el flow ESP32CAM-monitoring-server.json en NodeRed.
2. Instalar los nodos necesarios mencionados en los requerimentos.
3. Crear una aplicación desde el developer dashboard de Twitter.
4. Obtener tus credenciales de aplicación:
	- api key
	- api secret key
	- access token
	- access token secret
5. Comprueba que el broker MQTT esté funcionando.
6. Crear un tema para publicar en el broker.
7. Carga el programa ESP32CAM-monitoring-server.ino en el ESP32CAM.
8. Visita el dashboard de NodeRed

