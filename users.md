# Users

## POST /user/register

request body
```json
{
  "name": string
  "username": string
  "password": string
  "email": string
}
```

Response Body (Success)
```json
{
  "status_code": 201
  "message": "User registered successfully"
}
```

Response Body (Failed)
```json
{
  "status_code": 400
  "message": "Some data cannot be empty", "username already taken"
}
```

## POST /user/login

body
```json
{
    "username": string
    "password": string
}
```

Response Body (Success)
```json
{
  "status_code": 201
  "messsage": "Login successfully"
}
```

Response Body (Failed)
```json
{
  "status_code": 404
  "message": "Username or password is wrong"
}
```

## DELETE /user/logout

Response Body (Success)
```json
{
  "status_code": 200
  "message": "Logout successfully"
}
```

Response Body (Failed) :

```json
{
  "status_code": 401
  "errors" : "Unauthorized user"
}
```
