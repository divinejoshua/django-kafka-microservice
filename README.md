## Django RabbitMQ Microservices
This is a django project that has 3 micro serivces all communicationg together with Kafka. This project is inspired by https://github.com/mansha99/django-kafka-microservice/tree/master and a detailed blog https://medium.com/@mansha99/microservices-using-django-and-kafka-3776e8592ef3

## Project setup
```
pip3 install requirements.txt
```

## Start Kafka from docker
```
docker-compose up
```

## Start the userservice application
```
python3 manage.py runserver
```

## Start the logservice and emailservice application in their folders
```
python3 manage.py launch_queue_listener
```
