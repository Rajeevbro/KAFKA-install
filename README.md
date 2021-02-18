# KAFKA-install

## Helpful command for running KAFKA
- starting Zookeeper
```Terminal 
  zookeeper-server-start.bat C:\kafka\kafka_2.13-2.7.0\config\zookeeper.properties
  ```
  
  - starting kafka:
  ```kafka-server-start.bat C:\kafka\kafka_2.13-2.7.0\config\server.properties
  ```
  
  - getting broker id or locating broker id
  ```zookeeper-shell.bat localhost:2181 ls /brokers/ids
  ```
  - creating topic (example:test)
  ```kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test
  ```
  - Running kafka producer
  ```kafka-console-producer.bat --broker-list localhost:9092 --topic test
  ```
  - Running kafka consumer
  -``` kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test --from-beginning
  ```

