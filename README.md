# Market Service

## Info
Market service is responsible of all CRUD operations that related to the markets.
## Market service Endpoints

### Create new market
```http
POST /market/
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `name` | `string` | **Required**. |
| `createdBy` | `Number` | **Required**. |


### Response

```javascript
{
  "success"  : boolean,
  "market" : {
      "balance" : number,
      "id" : number,
      "name" : string,
      "createdBy" : number
  }
}

```

### refresh endpoint
```http
POST /auth/student/refresh
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `refreshToken` | `string` | **Required**. |


### Response

```javascript
{
  "access_token"  : string,
  "refresh_token" : string,
  "type"          : string,
  "expiresIn"     : string
}
```
### logout endpoint
```http
POST /auth/student/logout
```

| Header | Value |Description |
| :--- | :--- | :--- |
| `Authorization` | `Bearer "accessToken"` | **Required**. |


### Response

```javascript
{
  "success"  : boolean,
  "message"  : string
}
```




## Teacher Authentication Endpoints

### login endpoint
```http
POST /auth/teacher/login
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `email` | `string` | **Required**. |
| `password` | `string` | **Required**. |


## Response

```javascript
{
  "access_token"  : string,
  "refresh_token" : string,
  "type"          : string,
  "expiresIn"     : string
}

```

### refresh endpoint
```http
POST /auth/teacher/refresh
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `refreshToken` | `string` | **Required**. |


### Response

```javascript
{
  "access_token"  : string,
  "refresh_token" : string,
  "type"          : string,
  "expiresIn"     : string
}
```

### logout endpoint
```http
POST /auth/teacher/logout
```

| Header | Value |Description |
| :--- | :--- | :--- |
| `Authorization` | `Bearer "accessToken"` | **Required**. |


### Response

```javascript
{
  "success"  : boolean,
  "message"  : string
}
```