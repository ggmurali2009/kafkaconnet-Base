# MQTT Config File

## Source Connector

### Rest endpoints   
1. `POST` localhost:8083/connectors/
````
{
    "name": "mqtt_kafka_source",
    "config": {
        "name": "mqtt_kafka_source",
        "connector.class": "org.apache.camel.kafkaconnector.pahomqtt5.CamelPahomqtt5SourceConnector",
        "mqtt.server.uri": "tcp://127.0.0.1:1883",
        "tasks.max": "1",
        "mqtt.topics" :"mqtttopic",
        "kafka.topic" : "kafkatopic",
        "connect.mqtt.client.id": "mqtt_client_1",
        "mqtt.service.quality":1,
        "key.converter": "org.apache.kafka.connect.json.JsonConverter",
        "value.converter": "org.apache.kafka.connect.json.JsonConverter",
        "key.converter.schemas.enable": "false",
        "value.converter.schemas.enable": "false"
    }
}
````

2.
`PUT` <`host:port`>/connectors/<`name_of_the_connector`>/config

Example:

`PUT` localhost:8083/connectors/mqtt_kafka_source/config

````
{
    "name": "mqtt_kafka_source",
    "connector.class": "com.murali.kafka.connectors.MqttSourceConnector",
    "mqtt.server.uri": "tcp://127.0.0.1:1883",
    "tasks.max": "3",
    "mqtt.topics": "mqtttopic",
    "kafka.topic": "kafkatopic",
    "connect.mqtt.client.id": "mqtt_client_1",
    "mqtt.service.quality": 1,
    "key.converter": "org.apache.kafka.connect.json.JsonConverter",
    "value.converter": "org.apache.kafka.connect.json.JsonConverter",
    "key.converter.schemas.enable": "false",
    "value.converter.schemas.enable": "false"
}
````


