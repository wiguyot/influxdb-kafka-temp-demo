FROM python:3.11-slim

WORKDIR /app

RUN apt-get update && apt-get install -y netcat-openbsd && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY producer.py .
COPY wait-for-kafka.sh .
RUN chmod +x wait-for-kafka.sh

CMD ["./wait-for-kafka.sh"]
