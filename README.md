# _Mobile Store API_

A Fake REST API using json-server with JWT authentication hosted on cloud service render.

Implemented End-points: login,register and products

If you want to clone this repo follow below steps:
## Install

```
$ npm install
$ npm run start-auth
```

Might need to run
```
npm audit fix
```

## How to login/register?

You can login/register by sending a POST request to

```
POST https://mobilestore-c8yg.onrender.com/auth/login
POST https://mobilestore-c8yg.onrender.com/auth/register
OR
POST https://mobilestoreapi.onrender.com/auth/login
POST https://mobilestoreapi.onrender.com/auth/login
```
with the following data or any email, password from users.json
Validation is added for existing email or blank request body in /auth/login or /auth/register endpoints.

```
{
  "email": "nilson@email.com",
  "password":"nilson"
}
```

You should receive an access token with the following format 

```
{
   "access_token": "<ACCESS_TOKEN>"
}
```

You should send this authorization with any request to the protected endpoints i.e. "/products". You can do all CRUD operation on database.json. 
Please note there is no verification / validation on request body send to database.json.
For eg. to access all products you will make a GET call to either of the endpoints("https://mobilestoreapi.onrender.com/products") with Accesstoken.
```
Authorization: Bearer <ACCESS_TOKEN>
```

Thank You\
Happy Coding,\
Learn,Code and Earn\
Stay Safe and Stay Positive :)
