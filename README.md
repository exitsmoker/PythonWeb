Python RESTful Web Services
========

* version 1.0.0
* initializedDate 2019.10.09
* description
    `Web` `REST` `Django`
    This repository is all about this book
    
    ![](/Images/IMG_1066.jpg)

    * `Django RESTful Framework` First of all i have created virtualenv for this project. The env name's Django01 and it created Django RESTful framework folders automatically. All i had to do was type code "source ~/PythonREST/Django01/bin/activate" to activate virtualenv in bash.

    * `Model` I have created a model named Game in Django01/gamesapi/games/models.py. It's subclass of django.db.models.Model. And i had to make migrations for sync this to database using "pyhton manage.py makemigrations games", "python manage.py migrate".

    * `Serializer` It stands between the model instance and python primitive. Parser and Renderer stands between python primitive and HTTP Request, Response. And i have created it which is a subclass of serializers.Serializer in Django01/gamesapi/games/serializers.py.

    * `API view` so now we are going to return JSON expression using the Serializer we created for HTTP Request. Django-1/gamesapi/games/views.py there is JSONResponse class which is a subclass of django.http.HttpResponse class.

    * `urlpatterns` In Django01/gamesapi/games/urls.py i wrote urlpatterns to get HttpRequests.

    * `runserver` Finally we run server with "python manage.py runserver"

    * `CRUD` i have tested HTTP Requests using `curl`, `httpie`, `postman`, `pycharm` . The request was 
        * GET 127.0.0.1:8000/games/
        * GET 127.0.0.1:8000/games/3(the id value)/
        * PUT 127.0.0.1:8000/games/3/ name='something' (It's modifying)
        * DELETE 127.0.0.1:8000/games/3/ (It's deleting)
        * POST 127.0.0.1:8000/games/ name='' game_category='' played='' release_date='' (creating model instance.)