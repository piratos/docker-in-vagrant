FROM ubuntu:16.04

MAINTAINER Sayf Eddine HAMMEMI "sayf.eddine.hammemi@gmail.com"

RUN apt-get update -y && \
    apt-get install -y python-pip python-dev apache2

COPY ./app/requirements.txt /app/requirements.txt

WORKDIR /app

RUN pip install -r requirements.txt

COPY ./app /app

EXPOSE 80

ENTRYPOINT ["python"]

CMD ["flask_app.py"]
