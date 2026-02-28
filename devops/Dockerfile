FROM python:3.11-slim

WORKDIR /app

# Instalar dependencias del sistema necesarias para psycopg2
RUN apt-get update && apt-get install -y gcc libpq-dev && rm -rf /var/lib/apt/lists/*

COPY requirements.txt /app
RUN pip install --upgrade pip && pip install -r requirements.txt

COPY src /app/src
WORKDIR /app/src

CMD ["python", "app.py"]
