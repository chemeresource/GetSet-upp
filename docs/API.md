# API Documentation

## Overview
This document provides a complete guide to the REST API for the GetSet-upp application.

## Base URL
The base URL for all API endpoints is:  `https://api.getsetupp.com/v1`

## Authentication
All API requests require authentication via an API token. The API token should be included in the headers of each request:

```
Authorization: Bearer YOUR_API_TOKEN
```

## Endpoints

### 1. **Get Items**
- **Endpoint**: `/items`
- **Method**: `GET`
- **Description**: Retrieve a list of items.

#### Request Example:
```http
GET /items HTTP/1.1
Host: api.getsetupp.com
Authorization: Bearer YOUR_API_TOKEN
```

#### Response Example:
```json
{
  "items": [
    {
      "id": 1,
      "name": "Item 1",
      "description": "Description of Item 1"
    },
    {
      "id": 2,
      "name": "Item 2",
      "description": "Description of Item 2"
    }
  ]
}
```

### 2. **Create Item**
- **Endpoint**: `/items`
- **Method**: `POST`
- **Description**: Create a new item.

#### Request Example:
```http
POST /items HTTP/1.1
Host: api.getsetupp.com
Authorization: Bearer YOUR_API_TOKEN
Content-Type: application/json

{
  "name": "New Item",
  "description": "Description of new item"
}
```

#### Response Example:
```json
{
  "id": 3,
  "name": "New Item",
  "description": "Description of new item"
}
```

### 3. **Update Item**
- **Endpoint**: `/items/{id}`
- **Method**: `PUT`
- **Description**: Update an existing item.

#### Request Example:
```http
PUT /items/1 HTTP/1.1
Host: api.getsetupp.com
Authorization: Bearer YOUR_API_TOKEN
Content-Type: application/json

{
  "name": "Updated Item",
  "description": "Updated description of item"
}
```

#### Response Example:
```json
{
  "id": 1,
  "name": "Updated Item",
  "description": "Updated description of item"
}
```

### 4. **Delete Item**
- **Endpoint**: `/items/{id}`
- **Method**: `DELETE`
- **Description**: Delete an existing item.

#### Request Example:
```http
DELETE /items/1 HTTP/1.1
Host: api.getsetupp.com
Authorization: Bearer YOUR_API_TOKEN
```

#### Response Example:
```json
{
  "message": "Item deleted successfully."
}
```

## Conclusion
This API allows for easy interaction with the GetSet-upp application to manage items efficiently. Please refer to the above documentation for usage and examples.
