# Running Instructions
### To run all services in background (detached mode)
```
docker-compose up -d
```
### To run the KsqlDB server
```
docker exec -it ksqldb-server ksql http://localhost:8088
```
### To create a topic
```
docker exec -it broker kafka-topics --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic demo-topic
```
### To check ksqldb-server logs
```
docker logs ksqldb-server
```
### To stop all services without losing data
```
docker-compose stop
```
### To tear down all services (delete all data)
```
docker-compose down
```
