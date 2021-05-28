# Kafka Command Line

## Consumer
***
### Consumer Groups

````
./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --describe --all-groups
````

### __Data in __consumer_offsets__

````
./kafka-console-consumer.sh --formatter "kafka.coordinator.group.GroupMetadataManager\$OffsetsMessageFormatter" --bootstrap-server kafka:9092 --topic __consumer_offsets
````

## Data Dump

````
./kafka-dump-log.sh --print-data-log --files /home/muralimanoj/Desktop/kafkaDataLogs/data/cluster1/broker1/connect-configs-0/00000000000000000000.log
````

## Connect
***
### print data of connect-offsets
```
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --from-beginning --property print.key=true --topic connect-offsets
```
