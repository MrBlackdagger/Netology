FROM continuumio/miniconda3:latest

RUN pip install mlflow boto3

WORKDIR /app

COPY 1.sh /app

RUN chmod +x 1.sh

CMD ["1.sh", "app"]
