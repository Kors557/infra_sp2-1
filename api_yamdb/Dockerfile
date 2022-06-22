FROM python:3.7-slim

<<<<<<< HEAD
WORKDIR /app

COPY requirements.txt ./

RUN pip3 install -r ./requirements.txt --no-cache-dir

COPY ./ ./

=======
# Создать директорию вашего приложения.
RUN mkdir /app

# Скопировать с локального компьютера файл зависимостей
# в директорию /app.
COPY requirements.txt /app

# Выполнить установку зависимостей внутри контейнера.
RUN pip3 install -r /app/requirements.txt --no-cache-dir

# Скопировать содержимое директории /api_yamdb c локального компьютера
# в директорию /app.
COPY ./ /app

# Сделать директорию /app рабочей директорией. 
WORKDIR /app

# Выполнить запуск сервера разработки при старте контейнера.
>>>>>>> 3fd775c7130b4ada7e600e518f68aa0b4b051b87
CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ] 