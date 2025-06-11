# NInivan

Sistema de repositorio para los parlantes de  cobro
Respositorio de primeras pruebas
Ejemplos de las estructuras de paquetes a enviar


## Topic

Los topicos de los endpoint se definen de la siguiente manera:
    zk/order/GID_zk@@@{SERIAL_NUMBRE}/

Ejemplo de un topioc para el numero de serie 2801678000032:
    
    zk/order/GID_zk@@@2801678000032/


## Comandos de los end point

Los endopoint aceptan basicamente 2 comandos:
  * Actualizacion
  * Operacion

Estructura de los comandos aceptados por los endpoints son siempre en formato json.

### Actualizacion

El comando de actualizaicone tiene los siguientes paramentros :
  Intanceid
  BrokerUrl
  BrokerPort
  AccessKey
  SecretKey
  GroupId
  rootTopic
  qos
  ClearSession
  KeepAliveInterval

Ejemplo del comando enviado segun la definicion del comando :
{
  "Intanceid":"",
  "BrokerUrl":"8.148.4.222",
  "BrokerPort":"1883",
  "AccessKey":"admin_zk_pub",
  "SecretKey":"Hy1xQxEOuOpZ/oMyJ49VJL09kj4=",
  "GroupId":"1",
  "rootTopic":"${RootTopic}/order/${GroupId@@@DeviceSn}",
  "qos":"1",
  "ClearSession":"false",
  "KeepAliveInterval":"60"
}

---

### Operacion

Para registrar una operacion el paquete a envir es el siguiente:

{"type":"transOrder","amount":"1523.00","order":"694228410000101","paymentChannel":"WXZF","transTime":"2024-08-01 00:00:00"}

{"amount":"1523.00","order":"694228410000101","paymentChannel":"WXZF","transTime":"2024-08-01 00:00:00"}

ejemplo que funicon desde mqttexplorer
mesaje:{
  "amount": "3521",
  "orderid": "69422841002201118",
  "paymentChannel": "WXZF",
  "transTime": "2024-08-09 16:18:00"
}

el ultmo orederid termino en 49

ejemplo que funicon desde mqttexplorer
mesaje:{
  "amount": "987654",
  "orderid": "00084100220110188",
  "paymentChannel": "WXZF",
  "transTime": "2024-08-27 20:21:00"
}


## Listado de los dispoditivos por numero de serie

Dispositivos IOT:
SN:   2801678000032
IMEI: 862635060001013

SN:   2801678000031
IMEI: 862635060000742

Servidor gratuito para probar
mqtt://ninivan:X7RG37FTGoPDb4Dn@ninivan.cloud.shiftr.io
dominio: ninivan.cloud.shiftr.io
Broker:  broker.shiftr.io
port:    1883