# fake-api-7tech

Первичная установка
$ npm install json-sever --save
$ npm install faker --save
$ npm install jsonwebtoken --save

Запуск без авторизации
npm run start
Запуск с авторизацией
npm run start-auth

Получение токена(можете добавить свои лог/пасс в файле users.json)
curl --location --request POST 'http://localhost:3000/auth/login' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email": "obivankenobi@gmail.com",
    "password": "ivan"
}'

Пример запроса:
curl --location --request GET 'http://localhost:3000/products?_page=1' \
--header 'Authorization: Bearer <token>'
