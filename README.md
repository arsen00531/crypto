```
 __   _______          _   _ _____  ______ _____ 
 \ \ / /_   _|   /\   | \ | |  __ \|  ____/ ____|
  \ V /  | |    /  \  |  \| | |  | | |__ | |     
   > <   | |   / /\ \ | . ` | |  | |  __|| |     
  / . \ _| |_ / ____ \| |\  | |__| | |___| |____ 
 /_/ \_\_____/_/    \_\_| \_|_____/|______\_____|
```
# Настройка и запуск бота с аукционами в телеграм
### Окружение
 - Python 3.12
 - Mysql 8.3.0
 - UNIX based system
### Первый запуск
Для запуска понадобится установить и запустить MySQL сервер с официального сайта, при установке необходимо задать пароль для root пользователя.


После запуска необходимо будет подключиться к серверу (любым удобным способом, например терминал или dbeaver) и создать новую базу данных (через терминал:
```CREATE DATABASE [ИМЯ_БД];```)

После этого необходимо создать файл `config.yaml` в папке `bot/app/data/` со следующей структурой:
```
ANTISNIPER: 0 # Не трогать
CURRENCY: $ # Не трогать
DATABASE: auction-db # [ИМЯ_БД] из пункта выше
HELP: help.mp4 # Название видео для помощи в папке static
HOST: localhost # хост базы данных, если просто на локальной машине, то оставить
LOGO: logo.jpeg # Название файла с логотипом в папке static
LOOSE_NOTIFICATION: true # Не трогать
PASSWORD: root # пароль от  базы данных
SETTINGS:
  en: 'Auction rules

    English'
  ru: "\u041F\u0440\u0430\u0432\u0438\u043B\u0430 \u0430\u0443\u043A\u0446\u0438\u043E\
    \u043D\u0430\n\u041D\u0430 \u0440\u0443\u0441\u0441\u043A\u043E\u043C"
STEP: 1,5,10,50,100,200 # Не трогать
USER: root # пользователь в базе данных, не трогать
WIN_NOTIFICATION: true # Не трогать
bot_token: 123:adsfkKL # API токен для бота 
```
 - bot_token - получить в телеграмм боте botfather
 - user - пользователь в базе данных, проще оставить root
 - password - пароль от пользователя (пароль от root пользователя)
 - host - на каком хосте находится сервер базы данных, если всё на одном компьютере, то будет localhost
 - database - созданная база данных
## Запускать `main.py`
## После первичной настройки можно просто всегда запускать только `main.py`