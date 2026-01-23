# Comprehensive Test REST API

**Version:** 1.0.0

A test REST API designed to cover most OpenAPI 3.0 specification features.
This API includes examples of all major HTTP methods, parameter types, 
authentication schemes, content types, and response patterns.


## Installation

### Prerequisites
- Dyalog APL 18.0 or later
- LINK (for loading the generated code)

### Loading the Client

```apl
]LINK.Create # ./APLSource
```

This will load all the generated client code into your active workspace.

## Quick Start

### 1. Initialize the Client

```apl
⍝ Create configuration
config ← (
    baseURL: 'https://api.testapi.example.com/v1'
    security: (
        ⍝ Configure your authentication
    )
)

⍝ Create client instance
client ← ⎕NEW Client config
```


### 2. Authentication

This API uses the following authentication methods:


#### ApiKeyAuth
- **Type:** ApiKey

API key for authentication


#### BearerAuth
- **Type:** Http

JWT bearer token


#### OAuth2
- **Type:** OAuth2


## API Endpoints


### Health


#### `GET /health`

**Operation ID:** `getHealth`

Health check endpoint

**Usage:**
```apl
⍝ Make the request (no parameters required)
response ← client.health.getHealth ()
```


---


### Users


#### `GET /users`

**Operation ID:** `listUsers`

List all users

**Usage:**
```apl
⍝ Prepare arguments
args ← (
)

⍝ Make the request
response ← client.users.listUsers args
```


**Parameters:**
- `page` (Query): Integer - Page number for pagination
- `limit` (Query): Integer - Number of items per page
- `status` (Query): String - Filter users by status
- `sort` (Query): String - Sort field and order
- `X-Request-ID` (Header): String - Unique request identifier

---


#### `POST /users`

**Operation ID:** `createUser`

Create a new user

**Usage:**
```apl
⍝ Prepare arguments
args ← (
    ⍝ Add request body parameters as needed
    ⍝ TODO (Document what the request body parameters actually are)
    ⍝ For now, check the endpoint.aplf file for this, and see what we are expecting.
    ⍝ And check the spec. That's a useful thing to always check!
)

⍝ Make the request
response ← client.users.createUser args
```


---


#### `GET /users/{userId}`

**Operation ID:** `getUserById`

Get user by ID

**Usage:**
```apl
⍝ Make the request (no parameters required)
response ← client.users.getUserById ()
```


---


#### `PUT /users/{userId}`

**Operation ID:** `updateUser`

Update user (full replace)

**Usage:**
```apl
⍝ Prepare arguments
args ← (
    ⍝ Add request body parameters as needed
    ⍝ TODO (Document what the request body parameters actually are)
    ⍝ For now, check the endpoint.aplf file for this, and see what we are expecting.
    ⍝ And check the spec. That's a useful thing to always check!
)

⍝ Make the request
response ← client.users.updateUser args
```


---


#### `PATCH /users/{userId}`

**Operation ID:** `patchUser`

Partially update user

**Usage:**
```apl
⍝ Prepare arguments
args ← (
    ⍝ Add request body parameters as needed
    ⍝ TODO (Document what the request body parameters actually are)
    ⍝ For now, check the endpoint.aplf file for this, and see what we are expecting.
    ⍝ And check the spec. That's a useful thing to always check!
)

⍝ Make the request
response ← client.users.patchUser args
```


---


#### `DELETE /users/{userId}`

**Operation ID:** `deleteUser`

Delete user

**Usage:**
```apl
⍝ Make the request (no parameters required)
response ← client.users.deleteUser ()
```


---


#### `POST /users/{userId}/avatar`

**Operation ID:** `uploadAvatar`

Upload user avatar

**Usage:**
```apl
⍝ Prepare arguments
args ← (
    ⍝ Add request body parameters as needed
    ⍝ TODO (Document what the request body parameters actually are)
    ⍝ For now, check the endpoint.aplf file for this, and see what we are expecting.
    ⍝ And check the spec. That's a useful thing to always check!
)

⍝ Make the request
response ← client.users.uploadAvatar args
```


---


#### `GET /users/{userId}/avatar`

**Operation ID:** `downloadAvatar`

Download user avatar

**Usage:**
```apl
⍝ Make the request (no parameters required)
response ← client.users.downloadAvatar ()
```


---


### Products


#### `GET /products`

**Operation ID:** `listProducts`

List products

**Usage:**
```apl
⍝ Prepare arguments
args ← (
)

⍝ Make the request
response ← client.products.listProducts args
```


**Parameters:**
- `category` (Query): Array - Filter by categories
- `minPrice` (Query): Number
- `maxPrice` (Query): Number
- `inStock` (Query): Boolean

---


#### `POST /products`

**Operation ID:** `createProduct`

Create product

**Usage:**
```apl
⍝ Prepare arguments
args ← (
    ⍝ Add request body parameters as needed
    ⍝ TODO (Document what the request body parameters actually are)
    ⍝ For now, check the endpoint.aplf file for this, and see what we are expecting.
    ⍝ And check the spec. That's a useful thing to always check!
)

⍝ Make the request
response ← client.products.createProduct args
```


---


#### `GET /products/{productId}`

**Operation ID:** `getProduct`

Get product by ID

**Usage:**
```apl
⍝ Make the request (no parameters required)
response ← client.products.getProduct ()
```


---


### Orders


#### `POST /orders`

**Operation ID:** `createOrder`

Create a new order

**Usage:**
```apl
⍝ Prepare arguments
args ← (
    ⍝ Add request body parameters as needed
    ⍝ TODO (Document what the request body parameters actually are)
    ⍝ For now, check the endpoint.aplf file for this, and see what we are expecting.
    ⍝ And check the spec. That's a useful thing to always check!
)

⍝ Make the request
response ← client.orders.createOrder args
```


---


#### `GET /orders`

**Operation ID:** `listOrders`

List orders

**Usage:**
```apl
⍝ Prepare arguments
args ← (
)

⍝ Make the request
response ← client.orders.listOrders args
```


**Parameters:**
- `status` (Query): String
- `startDate` (Query): String
- `endDate` (Query): String

---


#### `GET /orders/{orderId}`

**Operation ID:** `getOrder`

Get order by ID

**Usage:**
```apl
⍝ Make the request (no parameters required)
response ← client.orders.getOrder ()
```


---


#### `PATCH /orders/{orderId}/status`

**Operation ID:** `updateOrderStatus`

Update order status

**Usage:**
```apl
⍝ Prepare arguments
args ← (
    ⍝ Add request body parameters as needed
    ⍝ TODO (Document what the request body parameters actually are)
    ⍝ For now, check the endpoint.aplf file for this, and see what we are expecting.
    ⍝ And check the spec. That's a useful thing to always check!
)

⍝ Make the request
response ← client.orders.updateOrderStatus args
```


---


### Files


#### `POST /files/upload`

**Operation ID:** `uploadFiles`

Upload multiple files

**Usage:**
```apl
⍝ Prepare arguments
args ← (
    ⍝ Add request body parameters as needed
    ⍝ TODO (Document what the request body parameters actually are)
    ⍝ For now, check the endpoint.aplf file for this, and see what we are expecting.
    ⍝ And check the spec. That's a useful thing to always check!
)

⍝ Make the request
response ← client.files.uploadFiles args
```


---


#### `GET /files/{fileId}/download`

**Operation ID:** `downloadFile`

Download file

**Usage:**
```apl
⍝ Make the request (no parameters required)
response ← client.files.downloadFile ()
```


---


### Auth


#### `POST /auth/login`

**Operation ID:** `login`

User login

**Usage:**
```apl
⍝ Prepare arguments
args ← (
    ⍝ Add request body parameters as needed
    ⍝ TODO (Document what the request body parameters actually are)
    ⍝ For now, check the endpoint.aplf file for this, and see what we are expecting.
    ⍝ And check the spec. That's a useful thing to always check!
)

⍝ Make the request
response ← client.auth.login args
```


---


### Search


#### `GET /search`

**Operation ID:** `search`

Search across resources

**Usage:**
```apl
⍝ Prepare arguments
args ← (
    q: 'value'  ⍝ String - Search query)

⍝ Make the request
response ← client.search.search args
```


**Parameters:**
- `q` (Query) **[required]**: String - Search query
- `type` (Query): Array - Resource types to search

---


## Response Handling

All API methods return an HttpCommand response object with the following structure:

```apl
response.(
    Data        ⍝ Parsed JSON response as namespace
    HttpStatus  ⍝ HTTP status code (200, 404, etc.)
    HttpMessage ⍝ HTTP status message
    Headers     ⍝ Response headers
    ⍝ And more, see: https://dyalog.github.io/HttpCommand/latest/result-response/
)
```

**Example:**
```apl
response ← client.health.getHealth ()
⎕← 'Status: ', response.HttpStatus
⎕← 'Data: ', response.Data
```


## Error Handling

The client returns HttpCommand response objects. Check the `HttpStatus` field to determine success:

```apl
response ← client.users.getUserById (userId: 'some-id')

:If response.HttpStatus = 200
    ⍝ Success
    user ← response.Data
:Else
    ⍝ Error occurred
    ⎕← 'Error: ', response.HttpMessage
    ⎕← 'Details: ', response.Data
:EndIf
```

## Version Information

You can check the generated client version:

```apl
⎕← client.∆.Version ⍬
```

---

**Generated by [OpenAPI Dyalog Generator](https://github.com/Dyalog/OpenAPI)**
**Generated on:** 2026-01-23 19:51:08 UTC
