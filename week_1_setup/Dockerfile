FROM python:3.10

RUN apt-get update && \
    apt-get install -y wget build-essential libpq-dev && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN pip install pandas sqlalchemy psycopg2

WORKDIR /app
COPY data_ingest.py data_ingest.py

ENTRYPOINT ["python", "data_ingest.py"]
