
 ![SpringBootProducerConsumer](https://user-images.githubusercontent.com/93249038/215004921-8fabb442-c1ff-4ba8-a35e-ab2c918bbf22.jpg)

# 1) Kafka-Producer-using-Spring-Boot-Rest-and-Microservices
Apache Kafka is an open-source stream-processing software platform developed by LinkedIn and donated to the Apache Software Foundation, written in Scala and Java. 

# Working 
  
  A client that consumes records from a Kafka cluster. This client transparently handles the failure of Kafka brokers, and transparently adapts as topic partitions it fetches migrate within the cluster. This client also interacts with the broker to allow groups of consumers to load balance consumption using consumer groups.

 
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

# 2) Kafka-Consumer-using-Spring-Boot-Rest-and-Microservices

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
