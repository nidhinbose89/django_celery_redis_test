# To start all the services -- keep this terminal running so that we can see the log
>> docker-compose up

# To test the celery task -- In another terminal
>> docker exec -it django bash
>> python manage.py shell
>> from my_app.tasks import add
>>> add.delay(2,2)
<AsyncResult: ...fe3...>
