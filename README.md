Скрипт открывает страницы в браузере и парсит данные твитов из указанных источников по фильтру и затем отправляет их 
в телеграм. Для работы его автономно на сервере нужен xvfb (для работы окон) Во время работы скрипт собирает 
отфильтрованные твиты в файл tweets.json и урлы в файл processed_urls.json (для отслеживания дублей) 
Логи по умолчанию идут в контейнер, если нужно, можно писать их в файл app.log (в app.py можно сменить это)

Запуск:
1) отредактировать app.py (указать там chat_id, token)
2) docker build -t <имя_образа> .
3) docker run -d --name <имя_контейнера> <имя_образа>
