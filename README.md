# kafka-tests
Kafka testing

Build kafka cluster using docker compose
https://www.baeldung.com/ops/kafka-docker-setup

Create Topic

`docker exec -it ubuntu_kafka_1 kafka-topics --create --topic quickstart-events --bootstrap-server 10.1.1.249:19092`

Show/describe Topic

`docker exec -it ubuntu_kafka_1 kafka-topics --describe --topic quickstart-events --bootstrap-server 10.1.1.249:19092`

Run Producer console -> type and then ctrl-c

`docker exec -it ubuntu_kafka_1 kafka-console-producer --topic quickstart-events --bootstrap-server 10.1.1.249:19092`

Consumers

Node1

`docker exec -it ubuntu_kafka_1 kafka-console-consumer --topic quickstart-events --from-beginning --bootstrap-server 10.1.1.249:19092`

Node2

`docker exec -it ubuntu_kafka_1 kafka-console-consumer --topic quickstart-events --from-beginning --bootstrap-server 10.2.1.44:29092`
