# Приложение для голосования

Простое  приложение, работающее в нескольких контейнерах Docker.

Предварительные требования

Docker

Docker compose


Как запустить приложение


git clone https://github.com/your-username/example-voting-app.git

Замените your-username на ваш GitHub-username.



Перейдите в директорию проекта:

cd example-voting-app



Запустите приложение:

docker-compose up -d



Доступ к приложению:



Голосование: http://localhost:8080


Результаты: http://localhost:8081

## Архитектура

![Architecture diagram](architecture.png)

Фронтенд-веб-приложение на Python (/vote), позволяющее голосовать между двумя вариантами

Redis (https://hub.docker.com/_/redis/), собирающий новые голоса

.NET-воркер (/worker/), который обрабатывает голоса и сохраняет их в…

Postgres (https://hub.docker.com/_/postgres/) с Docker volume для хранения данных

Веб-приложение на Node.js (/result), показывающее результаты голосования в реальном времени
