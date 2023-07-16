FROM python:3.10-alpine

WORKDIR /simple-flask-app

COPY requirements.txt /simple-flask-app

RUN pip install -r requirements.txt --no-cache-dir

COPY . /simple-flask-app

CMD python app.py 

