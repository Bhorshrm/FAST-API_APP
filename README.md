# Asynchronous Tasks with FastAPI and Celery

The main aim of this project is to learn how to handle background processes with FastAPI, Celery, and Docker.
It aims to demonstrate the asynchronous nature of Celery that allows client to serve non-blocking requests from the user even if a computaionally intensive background process is waiting in the queue.


## Want to use this project?

Spin up the containers:

```sh
$ docker-compose up -d --build
```

Open your browser to [http://localhost:8004](http://localhost:8004) to view the app or to [http://localhost:5556](http://localhost:5556) to view the Flower dashboard.

Trigger a new task:

```sh
$ curl http://localhost:8004/tasks -H "Content-Type: application/json" --data '{"type": 0}'
```

Check the status:

```sh
$ curl http://localhost:8004/tasks/<TASK_ID>
```
