# Go-postgres

CRUD project using golang and PosstgreSQL.

Connection string to the database is in `.env` in root directory
____

## Starting server

Server starts on `localhost:8080`

In the root directory of project run `main.go` using terminal

```cli
go run main.go
```

____

## Endpoints

### POST

Create a user

**URL**: `http://localhost:8080/api/newuser`

**Body**: `raw/json`

```json
{
    "name": "gopher",
    "age":24,
    "location":"Russia"
}
```

____

### GET

Get user by id

**URL**: `http://localhost:8080/api/user/{id}`

**Body**: `raw/json`

```json
{
    "id":1,
    "name":"gopher",
    "location":"Russia",
    "age":24
}
```


### GET

Get all users

**URL**: `http://localhost:8080/api/user`

**Body**: `raw/json`

```json
[
    {
        "id":1,
        "name":"gopher",
        "location":"Russia",
        "age":24
    },
    {
        "id":2,
        "name":"gopher 2",
        "location":"Barbados",
        "age":42
    }
]
```

____

### PUT

Update users' information

**URL**: `http://localhost:8080/api/user/{id}`

**Body**: `raw/json`

```json
{
    "name":"gopher gopher",
    "location":"Moskow, Russia",
    "age":24
}
```

***Response***

```json
{
    "id":3,
    "message":"User deleted successfully. Total rows/record affected 1"
}
```

____

### DELETE

Delete user by id

**URL**: `http://localhost:8080/api/deleteuser/{id}`

**Body**: `raw/json`

***Response***

```json
{
    "id":3,
    "message":"User deleted successfully. Total rows/record affected 1"
}
```