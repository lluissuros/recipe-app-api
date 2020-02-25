# recipe-app-api
recipe api with django from udemy course https://www.udemy.com/course/django-python-advanced/




# django-docker notes
docker-compose build
docker-compose up  <-- start app, run command, start development server
docker-compose down  <-- remove ALL existing containers

docker-compose run app sh -c "django-admin.py startproject app ."

run tests:
sudo docker-compose run app sh -c "python manage.py test"
sudo docker-compose run --rm app sh -c "python manage.py test && flake8"


create a new core app in our django project:
sudo docker-compose run app sh -c "python manage.py startapp core" 

every time we make a change on the model (/model, settings.py)
sudo docker-compose run --rm app sh -c "python manage.py makemigrations core" 


sudo docker-compose run app sh -c "python manage.py createsuperuser" 

''create user app
docker-compose run --rm app sh -c "python manage.py startapp user"
docker-compose run --rm app sh -c "python manage.py startapp recipe"

