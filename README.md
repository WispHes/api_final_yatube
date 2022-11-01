# ЯП - Спринт 9 - Проект «API для Yatube».
### Технологии
Python 3.7, Django 2.2, DRF, JWT + Djoser
### Запуск проекта в dev-режиме
- Клонировать репозиторий и перейти в него в командной строке.
```bash
git clone https://github.com/WispHes/api_final_yatube.git
```
- Установите виртуальное окружение c версии Python 3.7 :
```bash
py -3.7 -m venv venv
```
- Активируйте виртуальное окружение :
```bash
venv/Scripts/activate
```
- Далее установите зависимости из файла requirements.txt:
```bash
pip install -r requirements.txt
```
- Перейдите в дерикторию yatube_api и выполните миграции:
```bash
python manage.py migrate
```
- После требуется создать суперпользователя:
```bash
python manage.py createsuperuser
```
- Чтобы запустить проект используйте команду:
```bash
python manage.py runserver
```
### Примеры запросов к API

1. Получение публикаций:
Получить список всех публикаций вы можете сделав GET запрос по адрессу /api/v1/posts/
При верном запросе мы получим примерно следующий ответ:
```bash
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {}
  ]
}
```


2. Создание публикации:
Добавление новой публикации в коллекцию публикаций, делается путем POST запроса по адрессу /api/v1/posts/, передав обязательные параметры
```bash
{
  "text": "string",
  "image": "string",
  "group": 0
}
```

3. Удаление публикации:
Удалить публикации вы можете по id поста, сделав DELETE запрос по адрессу /api/v1/posts/{id}/
При верном запросе мы получим следующий ответ:
```bash
  {
    "detail": "Страница не найдена."
  }
```
