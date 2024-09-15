# PayeTonQawa-API-service-clients
**MSPR 4**

Utilisation de go (golang). Utilisation du framework Gin pour la partie REST API.


## Utilisation

### Build and run

1. docker build -t service-clients .
2. docker run -p 8089:8080 service-clients
3. open a terminal an use the curl commands bellow

### Requetes CRUD

#### Create user

```sh
curl -X POST http://localhost:8089/users \
-H "Content-Type: application/json" \
-d '{"id":"1", "username":"john_doe", "email":"john@example.com"}'
```


#### Read user

Get a list of all users

```sh
curl -X GET http://localhost:8089/users
```


#### Update user

using user with id 1 as an example:

```sh
curl -X PUT http://localhost:8089/users/1 -H "Content-Type: application/json" -d '{
  "id": "1",
  "username": "<updated_username>",
  "email": "<updated_email>"
}'
```

#### Delete user

```sh
curl -X DELETE http://localhost:8089/users/1
```


