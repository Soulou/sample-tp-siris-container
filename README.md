# Sample Python/Celery application

## Description

This application is composed of two components:

  * The Celery server which takes tasks and return result
  * The Flask server which runs the webserver that sends tasks to the Celery
    server and display results

It requires a redis server defined by the environment variable `REDIS_URL`
available for both processes.

It is compatible up to Python 3.6.x

## How to start the app

### Flask server

```
python app.py
```

The application will be available on http://localhost:3000

### Celery worker

```
python job.py
```

The application will start consuming jobs sent from the Flask web server

## Links

http://www.celeryproject.org
https://Redis.io
http://flask.pocoo.org
