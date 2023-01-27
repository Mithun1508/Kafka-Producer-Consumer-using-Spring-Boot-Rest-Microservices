# Kafka-Producer-using-Spring-Boot-Rest-and-Microservices
Apache Kafka is an open-source stream-processing software platform developed by LinkedIn and donated to the Apache Software Foundation, written in Scala and Java. 

# Start Zookeeper
 
bin/zookeeper-server-start.sh config/zookeeper.properties
 
# Start Kafka Server

bin/kafka-server-start.sh config/server.properties

# Create Kafka Topic

bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic Kafka_Example

# Consume from the Kafka Topic via Console
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic Kafka_Example --from-beginning

# Publish message via WebService

http://localhost:8080/kafka/trigger-object

http://localhost:8080/kafka/trigger-string

# Kafka-Consumer-using-Spring-Boot-Rest-and-Microservices

# Start Zookeeper
bin/zookeeper-server-start.sh config/zookeeper.properties

# Start Kafka Server
bin/kafka-server-start.sh config/server.properties
 
# Create Kafka Topic
bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic Kafka_Example
bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic Kafka_Example_json

# Publish to the Kafka Topic via Console
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic Kafka_Object
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic Kafka_String