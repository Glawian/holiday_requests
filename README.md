# Holiday Requests
Application is developed with Django and Angular framework.

## Setup application
In the root of the repository run following commands (Linux):

```
docker-compose build - to build images
docker-compose up - start the containers (use -d to detach)
docker-compose run django python manage.py migrate
docker-compose run django python manage.py createsuperuser (if superuser is needed)
```

**Django** project will be available at [localhost:80](http://localhost:80)

**Angular** project will be available at [localhost:8080](http://localhost:8080)
