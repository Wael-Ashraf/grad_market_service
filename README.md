# Market Service

## Info
Market service is responsible of all CRUD operations that related to the markets.
## Market Service Endpoints

### Get all markets
```http
GET /markets/
```

### Response

```javascript
{
  "success"  : boolean,
  "market" : array
}

```

### Create new market
```http
POST /markets/
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
      "createdBy" : number,
      "updatedAt" : date,
      "createdAt" : date
  }
}

```

### Delete Market
```http
DELETE /markets/:id/destroy
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `id` | `number` | **Required in url**. |


### Response

```javascript
{
    "success": boolean,
    "message": message
}
```
### Update Market
```http
PUT markets/:id/update
```

| Header | Value |Description |
| :--- | :--- | :--- |
| `name` | `string` | **Required**. |


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