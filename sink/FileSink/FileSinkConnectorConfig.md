# File Sink Connector Config File

## Sink Connector

### Rest endpoints
1. `POST` localhost:8083/connectors/
````
{
    "name": "kafka_file_sink_connector",
    "config": {
        "name": "kafka_file_sink_connector",
        "connector.class": "org.apache.kafka.connect.file.FileStreamSinkConnector",
        "tasks.max": "1",
        "file": "/home/muralimanoj/myWork/kafkaconnet/sink/FileSink/targetsink.txt",
        "topics": "demotopic",
        "key.converter": "org.apache.kafka.connect.Storage.StringConverter",
        "value.converter": "org.apache.kafka.connect.Storage.StringConverter",
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
        "name": "kafka_file_sink_connector",
        "connector.class": "org.apache.kafka.connect.file.FileStreamSinkConnector",
        "tasks.max": "1",
        "file": "/home/muralimanoj/myWork/kafkaconnet/sink/FileSink/targetsink.txt",
        "topics": "demotopic",
        "key.converter": "org.apache.kafka.connect.Storage.StringConverter",
        "value.converter": "org.apache.kafka.connect.Storage.StringConverter",
        "key.converter.schemas.enable": "false",
        "value.converter.schemas.enable": "false"
}
````
