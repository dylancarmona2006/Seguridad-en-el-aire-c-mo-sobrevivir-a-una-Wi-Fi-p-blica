# Seguridad-en-el-aire-c-mo-sobrevivir-a-una-Wi-Fi-p-blica
# Informe de Auditoría de Red Wi-Fi Insegura

## Introducción

En esta práctica se realizó un análisis de tráfico web con el objetivo de identificar los riesgos asociados al uso de conexiones HTTP en una red Wi-Fi pública.

El objetivo principal fue comprender qué información puede quedar expuesta durante una conexión HTTP y analizar cómo una VPN puede ayudar a proteger el tráfico y la privacidad del usuario.

## Sitio analizado

El sitio web analizado fue:

**http://neverssl.com**

El sitio utiliza el protocolo HTTP, lo que permite observar las características de una comunicación que no utiliza HTTPS.

## Evidencia observada

Mediante las herramientas de desarrollador del navegador, en la sección **Network (Red)**, se analizó la solicitud realizada al sitio.

Los principales datos observados fueron:

* **URL solicitada:** http://neverssl.com
* **Método HTTP:** GET
* **Host:** neverssl.com
* **Protocolo utilizado:** HTTP
* **Headers:** encabezados enviados por el navegador, como User-Agent, Accept y otros datos relacionados con la solicitud.

Estos elementos permiten identificar información relacionada con la comunicación entre el navegador y el servidor.

## Análisis del protocolo

### 1. ¿Qué protocolo utiliza el sitio?

El sitio utiliza **HTTP (Hypertext Transfer Protocol)**.

HTTP no proporciona cifrado TLS para proteger la comunicación entre el navegador y el servidor. Por esta razón, el tráfico HTTP puede presentar mayores riesgos de exposición cuando se utiliza dentro de una red pública.

HTTPS, en cambio, utiliza cifrado mediante TLS para proteger la comunicación entre el navegador y el servidor.

## Información que puede observarse durante la solicitud

Durante una solicitud HTTP pueden observarse diferentes elementos relacionados con la comunicación, entre ellos:

* Host.
* URL solicitada.
* Método HTTP, como GET.
* Headers enviados por el navegador.
* User-Agent.
* Tipo de contenido solicitado.
* Información relacionada con la solicitud y la respuesta.

Esta información puede proporcionar detalles sobre la comunicación realizada por el dispositivo.

## Riesgos de utilizar HTTP en una Wi-Fi pública

Utilizar HTTP desde una red Wi-Fi pública puede representar diferentes riesgos de seguridad.

Un atacante que consiga interceptar el tráfico podría observar información que no esté protegida mediante cifrado. También pueden existir riesgos de ataques de intermediario (Man-in-the-Middle), en los que un atacante intenta colocarse entre el dispositivo del usuario y el servidor.

Entre los principales riesgos se encuentran:

* Intercepción del tráfico.
* Exposición de información transmitida mediante HTTP.
* Posible modificación del tráfico.
* Exposición de información relacionada con los sitios visitados.
* Riesgo de ataques Man-in-the-Middle.
* Riesgo de conectarse accidentalmente a redes Wi-Fi falsas o redes gemelas maliciosas (Evil Twin).

Por estas razones, es recomendable utilizar conexiones HTTPS y evitar introducir información sensible cuando una conexión no esté adecuadamente protegida.

## ¿Cómo ayuda una VPN?

Una VPN (Virtual Private Network) crea un **túnel seguro y cifrado** entre el dispositivo del usuario y el servidor VPN.

Antes de atravesar la red pública, el tráfico se **encapsula y cifra** dentro de este túnel. Esto dificulta que otras personas conectadas a la misma red puedan observar directamente el contenido protegido de las comunicaciones.

La VPN proporciona una capa adicional de protección al utilizar redes Wi-Fi públicas porque ayuda a proteger el tráfico entre el dispositivo y el servidor VPN.

Sin embargo, una VPN no convierte automáticamente un sitio HTTP en HTTPS. Por ello, es importante continuar utilizando sitios web que empleen HTTPS y mantener buenas prácticas de seguridad.

## 3 Reglas de Oro para utilizar redes Wi-Fi públicas

### Regla 1: Utilizar HTTPS

Comprobar que los sitios web donde se introducen contraseñas, datos personales o información sensible utilicen HTTPS. Evitar enviar información importante mediante conexiones HTTP.

### Regla 2: Utilizar una VPN

Cuando se utilicen redes Wi-Fi públicas, utilizar una VPN confiable para crear un túnel cifrado y proteger el tráfico frente a posibles observadores de la red.

### Regla 3: Evitar redes desconocidas

No conectarse a redes Wi-Fi desconocidas o sospechosas. Siempre que sea posible, verificar el nombre oficial de la red con el establecimiento para evitar redes falsas o ataques Evil Twin.

## Conclusión

El análisis realizado permitió comprender los riesgos asociados al uso del protocolo HTTP en una red Wi-Fi pública.

Una conexión HTTP puede dejar expuesta información relacionada con la comunicación y puede ser más vulnerable a la interceptación que una conexión protegida mediante HTTPS.

El uso de HTTPS, una VPN y buenas prácticas de seguridad permite reducir los riesgos al utilizar redes públicas. La seguridad depende de utilizar conexiones protegidas, mantener los dispositivos actualizados y evitar redes o sitios web sospechosos.
