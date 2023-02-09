/home/docker-blog
docker run -v "$PWD":/code djangotest django-admin startproject mysite .
docker run -v "$PWD":/code -d -p 8000:8000 djangotest python manage.py runserver 0.0.0.0:8000
docker run --rm -v "$PWD":/code  -p 8000:8000 djangotest python manage.py runserver 0.0.0.0:8000

http://localhost:8000/

git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:dataanalytics2020/docker_django_project.git
git push -u origin main