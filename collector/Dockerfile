FROM python:3.12-alpine3.23

RUN apk upgrade --no-cache && apk add --no-cache ca-certificates curl

WORKDIR /app

COPY requirements.txt .
RUN python -m pip install --no-cache-dir --upgrade pip==26.3 \
    && pip install --no-cache-dir -r requirements.txt

COPY collector.py .

ENTRYPOINT ["python", "/app/collector.py"]
CMD []
