The command from book `docker-compose exec web pipenv install psycopg2-binary==2.8.5` may throw an error. Use 
`docker-compose exec web pipenv --python /usr/bin/python3 install psycopg2-binary==2.8.3`

After this since the image is cached. You need to force rebuilt
`
$ docker-compose down
$ docker-compose up -d --build
`

Link-> https://stackoverflow.com/questions/62070332/installing-psycopg-binary-on-docker-pipenv-got-the-error-does-not-found-python

