FROM python:3.7-slim

RUN apt-get update && apt-get install -y \
    python3-opencv \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY app/ .

EXPOSE 8080

CMD ["python", "-u", "/tensorflow.py"]
