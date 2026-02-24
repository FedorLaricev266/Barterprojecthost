# Развёртывание (хостинг)

## 1) Подготовка базы данных MySQL
Создайте БД и пользователя, затем заполните переменные окружения (см. `.env.example`).

## 2) Локальный запуск
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
uvicorn Barter.app.main:app --reload
```

## 3) Что уже подготовлено
- поддержка переменных окружения для БД и SECRET_KEY;
- запуск на `0.0.0.0` и через переменную `PORT`;
- `Procfile` (подходит для многих PaaS);
- `Dockerfile` (для Docker/VPS);
- исправлен `requirements.txt` (UTF-8).

## 4) Переменные окружения
Скопируйте `.env.example` в `.env` и задайте свои значения. На хостинге переменные обычно задаются в панели проекта.
