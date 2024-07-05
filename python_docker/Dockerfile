# Используем легковесный базовый образ
FROM python:3.9-alpine

# Устанавливаем необходимые системные зависимости
RUN apk add --no-cache gcc musl-dev libffi-dev

WORKDIR /app

# Копируем только необходимые файлы
COPY requirements.txt /app/

# Устанавливаем зависимости
RUN pip install --no-cache-dir -r requirements.txt

# Копируем исходный код приложения
COPY app.py /app/

# Команда для запуска приложения
CMD ["python", "app.py"]
