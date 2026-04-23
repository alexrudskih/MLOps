# В качестве основы, берём образ continuumio/miniconda3:latest
FROM continuumio/miniconda3:latest

# Добавляем и делаем рабочей папкой /app
WORKDIR /app

# Создаём скрипт прямо внутри контейнера
RUN echo '#!/bin/bash' > /app/1.sh && \
    echo 'echo "Hello Netology"' >> /app/1.sh && \
    chmod +x /app/1.sh

# Запускаем установку пакетов python mlflow boto3 pymysql
RUN pip install mlflow boto3 pymysql

# Запускаем скрипт при старте контейнера
CMD ["/app/1.sh"]