## Django Kafka Microservices
This is a django project that has 3 micro serivces all communicationg together with Kafka. This project is inspired by https://github.com/mansha99/django-kafka-microservice/tree/master and a detailed blog https://medium.com/@mansha99/microservices-using-django-and-kafka-3776e8592ef3

## Project setup
```
pip3 install requirements.txt
```

## Start Kafka from docker
```
docker-compose up
```

Port may be :9093 or :9092

## Start the userservice application
```
python3 manage.py runserver
```

## Start the logservice and emailservice application in their folders
```
python3 manage.py launch_queue_listener
```


## Kafka commands

Create a topic 
```
kafka-topics.sh --create --partitions 3 --bootstrap-server localhost:9093 --topic <topic_name>
```

List all your topics
```
kafka-topics.sh --bootstrap-server=localhost:9093 --list
```

Check a particular topic details
```
kafka-topics.sh --bootstrap-server=localhost:9093 --describe --topic <topic_name>
```

Delete a topic
```
kafka-topics.sh --bootstrap-server localhost:9092 --delete --topic <topic_name>
```


List groups
```
kafka-consumer-groups.sh --list --bootstrap-server localhost:9093
```


Check details of a particular group
```
kafka-consumer-groups.sh --describe --group <group_name> --members --bootstrap-server localhost:9093
```