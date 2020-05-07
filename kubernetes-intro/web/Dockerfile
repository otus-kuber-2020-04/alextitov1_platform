FROM python:3.7-alpine

RUN adduser --uid 1001 --disabled-password appuser

USER appuser

WORKDIR /app

COPY app/* /app

EXPOSE 8000

CMD python -m http.server
