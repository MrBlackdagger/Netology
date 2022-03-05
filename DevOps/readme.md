FROM continuumio/miniconda3:latest

WORKDIR /app

COPY ./1.sh /app

RUN chmod +x 1.sh

RUN apt-get install python && apt-get install mlflow && apt-get install boto3 && apt-get install pymysql

CMD ./1.sh
