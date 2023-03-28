FROM python:3.11.1

WORKDIR /app

COPY ./requirements.txt ./requirements.txt
RUN pip install -r requirements.txt

COPY ./web/ /app/web/web
COPY ./manage.py /app/web/manage.py

CMD [ "python3", "/app/web/manage.py", "runserver", "0.0.0.0:8000" ]
