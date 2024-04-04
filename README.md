# Описание проекта
Проект Kittygram - это веб-приложение для обмена фотографиями котиков. Он позволяет пользователям загружать, просматривать и комментировать фотографии котиков. Проект создан для любителей этих пушистых созданий, чтобы они могли делиться своими фотографиями и получать положительные эмоции от просмотра фотографий других пользователей.

## Инструкция по запуску проекта
```
git clone git@github.com:Imuntouchable/kittygram_final.git
cd kittygram
sudo docker compose -f docker-compose.production.yml pull
sudo docker compose -f docker-compose.production.yml down
sudo docker compose -f docker-compose.production.yml up -d
sudo docker compose -f docker-compose.production.yml exec backend python manage.py migrate
sudo docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic
sudo docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /backend_static/static/
```
## Примеры запросов к API
Примеры запросов к API будут доступны после запуска проекта. Вы можете использовать инструменты для отправки HTTP-запросов, такие как Postman или curl, чтобы взаимодействовать с API проекта.
![image](https://github.com/Imuntouchable/kittygram_final/assets/127663804/e20297ee-1f0e-4f4d-a90b-34b586f83d1c)


![image](https://github.com/Imuntouchable/kittygram_final/assets/127663804/5fe36665-b058-4193-a14d-08cb0ccc4f95)

## Используемые технологии:

Python
Django
Nginx
Docker
DockerHub
REST API
JavaScript
CSS
HTML

#  Как работать с репозиторием финального задания

## Что нужно сделать

Настроить запуск проекта Kittygram в контейнерах и CI/CD с помощью GitHub Actions

## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.

## Автор
Автор: Тогузов А. А.
