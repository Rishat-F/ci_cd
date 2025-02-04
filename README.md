# Учебный проект для изучения CI/CD

## Цели
Реализовать простенький проект (АПИ + frontend) со следующим поведением:
1) сначала прогоняются линтеры и юнит-тесты
2) если все норм, то далее проект разворачивается на stage, и прогоняются e2e-тесты
3) если все норм, то далее проект разворачивается на prod

## Используемые технологии
- АПИ на FastAPI
- БД sqlite3 через sqlalchemy
- frontend на React + TypeScript
- тестирование при помощи pytest + requests + playwright

## Что должно быть реализовано в АПИ
- создание новости (POST /news)
- получение новостей (GET /news)
- изменение новостей (PATCH /news)
- удаление новостей (DELETE /news)

## Что должно быть реализовано в frontend
- лента новостей с возможностью фильтрации, а также редактирования новостей

## Что из себя представляет новость
- id - идентификатор
- league - лига
- source - источник
- published_at - время и дата публикации
- parsed_at - время и дата парсинга
- title - заголовок
- description - краткое описание
- body - тело
- label - класс новости

## Архитектура проекта
АПИ и frontend должны быть представлены в виде отдельных микросервисов (docker-контейнеров).
