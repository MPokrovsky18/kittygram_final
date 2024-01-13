#  Как работать с репозиторием финального задания

[![Build Status](https://github.com/MPokrovsky18/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/{YOUR_USERNAME}/{YOUR_REPOSITORY}/actions/workflows/main.yml)

## Автор

- **Максим Покровский**
  - GitHub: [@MPokrovsky18](https://github.com/MPokrovsky18)

## Ссылка на репозиторий

[https://github.com/MPokrovsky18/kittygram_final](https://github.com/MPokrovsky18/kittygram_final)

## Описание

Проект **Kittygram Final** - это блог для любителей кошек, предоставляющий уютное место для хозяев кошек, где они могут делиться фотографиями своих пушистых друзей.

## Стек

- **Фронтенд:** React
- **Бэкенд:** Django, Django REST Framework
- **База данных:** PostgreSQL
- **Другие технологии:** Docker, Gunicorn, pytest

## Развертывание

1. Установите Docker и Docker Compose на вашем сервере.
2. Склонируйте репозиторий: `git clone https://github.com/MPokrovsky18/kittygram_final.git`.
3. Перейдите в директорию проекта: `cd kittygram_final`.
4. Создайте файл `.env` на основе примера `.env.example` и заполните необходимые переменные окружения.
5. Запустите приложение с помощью Docker Compose: `docker-compose -f docker-compose.production.yml up -d`.

## Примеры запросов к API

1. **Получение списка всех кошек:**
   ```http
   GET /api/cats/
   ```

2. **Получение конкретной кошки по идентификатору:**
   ```http
   GET /api/cats/{id}/
   ```

3. **Регистрация нового пользователя:**
   ```http
   POST /api/auth/users/
   ```

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