# Яндекс.Практикум
  
## Дипломная работа v1.0.0
 
## News-Explorer

### Краткая информация о проекте

Разработка сервиса по поиску новостей

### Ссылки

- Бэкенд проекта доступен по адресам:
- [api.igrek-news.ml](https://api.igrek-news.ml)
  - [www.api.igrek-news.ml](https://www.api.igrek-news.ml)
  - [130.193.48.139](http://130.193.48.139/)

### ПО для выполнения задания:

<li>
Git
<li>
Node.js
<li>
MongoDB
<li>
NPM-пакеты:

eslint, eslint-config-airbnb-base, eslint-plugin-import, express, mongoose, body-parser, validator, bcryptjs, jsonwebtoken, dotenv, helmet celebrate joi winston express-winston
  

### Инструкция по сборке:
- бекенд на сервере запускается командой **pm2 start app.js**
- при отправке запросов через **Postman** в заголовок **authorization** нужно записать схему аутентификации (используем **Bearer**) и токен через пробел: 

  - **POST/signup** создаёт пользователя. В теле POST-запроса на создание пользователя передается JSON-объект с тремя полями: **name**, **email**, **password**
  - **POST/signin** производит авторизацию пользователя. Если успешно - токен возвращается в ответе и записыватеся в cookie с включенной опцией httpOnly. В теле POST-запроса на создание пользователя передается JSON-объект с двумя полями: **email**, **password**
  
  - **GET /users/me**  возвращает информацию о пользователе (email и имя)
  - **GET/articles** возвращает все сохранённые пользователем статьи
  - **POST /articles** создаёт статью с переданными в теле данными **keyword**, **title**, **text**, **date**, **source**, **link** и **image**
  - **DELETE /articles/articleId** удаляет сохранённую статью по _id
 
  
### Итоги этапа по разработке бэкенда:

- создан бесплатный удаленный сервер на базе [Яндекс Облако](https://cloud.yandex.ru). К серверу привязаны домен и субдомены
- на сервере развернут бэкенд проекта News-Explorer
- сервер отвечает на запросы
- ошибки сервера обрабатываются централизовано
