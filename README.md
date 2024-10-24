{
    "openapi": "3.0.1",
    "info": {
        "title": "BankWeb API",
        "version": "v1"
    },
    "paths": {
        "/api/Admin/Transactions": {
            "get": {
                "tags": [
                    "Admin"
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/TransactionRespDataTableResp"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/Admin/GetAllUsers": {
            "get": {
                "tags": [
                    "Admin"
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/AdminUserInfoRespDataTableResp"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/AdminStore/GetAllPurchases": {
            "get": {
                "tags": [
                    "AdminStore"
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "type": "array",
                                    "items": {
                                        "type": "array",
                                        "items": {
                                            "$ref": "#/components/schemas/PurcahseHistoryItemResp"
                                        }
                                    }
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/AdminStore/GetStoreItems": {
            "get": {
                "tags": [
                    "AdminStore"
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "type": "array",
                                    "items": {
                                        "$ref": "#/components/schemas/StoreItem"
                                    }
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/AdminStore/Create": {
            "post": {
                "tags": [
                    "AdminStore"
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/StoreItem"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/StoreItem"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/StoreItem"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/EmptyResult"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/AdminStore/Get/{id}": {
            "get": {
                "tags": [
                    "AdminStore"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "required": true,
                        "schema": {
                            "type": "integer",
                            "format": "int32"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/StoreItem"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/AdminStore/Edit/{id}": {
            "post": {
                "tags": [
                    "AdminStore"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "required": true,
                        "schema": {
                            "type": "integer",
                            "format": "int32"
                        }
                    }
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/StoreItem"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/StoreItem"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/StoreItem"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/StoreItem"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/AdminStore/DeleteStoreItem": {
            "post": {
                "tags": [
                    "AdminStore"
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/StoreItem"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/StoreItem"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/StoreItem"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/EmptyResult"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/Auth/Login": {
            "post": {
                "tags": [
                    "Auth"
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/UserModel"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    }
                }
            }
        },
        "/api/Auth/Logout": {
            "get": {
                "tags": [
                    "Auth"
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/EmptyResult"
                                }
                            }
                        }
                    }
                }
            }
        },
        "/api/Auth/Register": {
            "post": {
                "tags": [
                    "Auth"
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/EmptyResult"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    }
                }
            }
        },
        "/api/Auth/PasswordRecovery": {
            "post": {
                "tags": [
                    "Auth"
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/EmptyResult"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    }
                }
            }
        },
        "/api/Auth/Recover": {
            "post": {
                "tags": [
                    "Auth"
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/EmptyResult"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    }
                }
            }
        },
        "/api/ContactUs/ContactUs": {
            "post": {
                "tags": [
                    "ContactUs"
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/UserModel"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/EmptyResult"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    }
                }
            }
        },
        "/api/PortalSearch/Index": {
            "get": {
                "tags": [
                    "PortalSearch"
                ],
                "parameters": [
                    {
                        "name": "searchString",
                        "in": "query",
                        "schema": {
                            "type": "string",
                            "nullable": true
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success"
                    }
                }
            }
        },
        "/api/Search/FindUser": {
            "get": {
                "tags": [
                    "Search"
                ],
                "parameters": [
                    {
                        "name": "term",
                        "in": "query",
                        "schema": {
                            "type": "string",
                            "nullable": true
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "type": "array",
                                    "items": {
                                        "type": "string"
                                    }
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/Store/GetStoreItems": {
            "get": {
                "tags": [
                    "Store"
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "type": "array",
                                    "items": {
                                        "$ref": "#/components/schemas/StoreItem"
                                    }
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/Store/GetHistory": {
            "get": {
                "tags": [
                    "Store"
                ],
                "parameters": [
                    {
                        "name": "username",
                        "in": "query",
                        "schema": {
                            "type": "string",
                            "nullable": true
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "type": "array",
                                    "items": {
                                        "$ref": "#/components/schemas/PurcahseHistoryItemResp"
                                    }
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/Store/BuyProduct": {
            "post": {
                "tags": [
                    "Store"
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/BuyProductReq"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/BuyProductReq"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/BuyProductReq"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/EmptyResult"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/Transaction/Get/{id}": {
            "get": {
                "tags": [
                    "Transaction"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "required": true,
                        "schema": {
                            "type": "integer",
                            "format": "int32"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/TransactionDBModel"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            }
        },
        "/api/Transaction/GetTransactions": {
            "get": {
                "tags": [
                    "Transaction"
                ],
                "parameters": [
                    {
                        "name": "start",
                        "in": "query",
                        "schema": {
                            "type": "integer",
                            "format": "int32"
                        }
                    },
                    {
                        "name": "length",
                        "in": "query",
                        "schema": {
                            "type": "integer",
                            "format": "int32"
                        }
                    },
                    {
                        "name": "search[value]",
                        "in": "query",
                        "schema": {
                            "type": "string",
                            "nullable": true
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/TransactionRespDataTableResp"
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/Transaction/GetTransactionHistory": {
            "get": {
                "tags": [
                    "Transaction"
                ],
                "parameters": [
                    {
                        "name": "userName",
                        "in": "query",
                        "schema": {
                            "type": "string",
                            "nullable": true
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "type": "array",
                                    "items": {
                                        "$ref": "#/components/schemas/TransactionResp"
                                    }
                                }
                            }
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/Transaction/Create": {
            "post": {
                "tags": [
                    "Transaction"
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/TransactionDBModel"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/TransactionDBModel"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/TransactionDBModel"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/EmptyResult"
                                }
                            }
                        }
                    },
                    "400": {
                        "description": "Bad Request"
                    },
                    "401": {
                        "description": "Unauthorized"
                    }
                }
            }
        },
        "/api/User/ProfileImage": {
            "get": {
                "tags": [
                    "User"
                ],
                "parameters": [
                    {
                        "name": "user",
                        "in": "query",
                        "schema": {
                            "type": "string",
                            "nullable": true
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success"
                    }
                }
            },
            "post": {
                "tags": [
                    "User"
                ],
                "requestBody": {
                    "content": {
                        "application/json": {
                            "schema": {
                                "$ref": "#/components/schemas/NewImageModel"
                            }
                        },
                        "text/json": {
                            "schema": {
                                "$ref": "#/components/schemas/NewImageModel"
                            }
                        },
                        "application/*+json": {
                            "schema": {
                                "$ref": "#/components/schemas/NewImageModel"
                            }
                        }
                    }
                },
                "responses": {
                    "200": {
                        "description": "Success"
                    }
                }
            }
        },
        "/api/User/GetAvailableFunds": {
            "get": {
                "tags": [
                    "User"
                ],
                "parameters": [
                    {
                        "name": "user",
                        "in": "query",
                        "schema": {
                            "type": "string",
                            "nullable": true
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "Success",
                        "content": {
                            "application/json": {
                                "schema": {
                                    "$ref": "#/components/schemas/AccountBalanceResp"
                                }
                            }
                        }
                    }
                }
            }
        }
    },
    "components": {
        "schemas": {
            "TransactionResp": {
                "type": "object",
                "properties": {
                    "id": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "senderId": {
                        "type": "string",
                        "nullable": true
                    },
                    "receiverId": {
                        "type": "string",
                        "nullable": true
                    },
                    "dateTime": {
                        "type": "string",
                        "nullable": true
                    },
                    "reason": {
                        "type": "string",
                        "nullable": true
                    },
                    "amount": {
                        "type": "number",
                        "format": "double"
                    },
                    "reference": {
                        "type": "string",
                        "nullable": true
                    },
                    "senderName": {
                        "type": "string",
                        "nullable": true
                    },
                    "senderSurname": {
                        "type": "string",
                        "nullable": true
                    },
                    "receiverName": {
                        "type": "string",
                        "nullable": true
                    },
                    "receiverSurname": {
                        "type": "string",
                        "nullable": true
                    }
                }
            },
            "TransactionRespDataTableResp": {
                "type": "object",
                "properties": {
                    "recordsTotal": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "recordsFiltered": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "data": {
                        "type": "array",
                        "items": {
                            "$ref": "#/components/schemas/TransactionResp"
                        },
                        "nullable": true
                    }
                }
            },
            "AdminUserInfoResp": {
                "type": "object",
                "properties": {
                    "name": {
                        "type": "string",
                        "nullable": true
                    },
                    "surname": {
                        "type": "string",
                        "nullable": true
                    },
                    "username": {
                        "type": "string",
                        "nullable": true
                    },
                    "role": {
                        "type": "integer",
                        "format": "int32"
                    }
                }
            },
            "AdminUserInfoRespDataTableResp": {
                "type": "object",
                "properties": {
                    "recordsTotal": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "recordsFiltered": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "data": {
                        "type": "array",
                        "items": {
                            "$ref": "#/components/schemas/AdminUserInfoResp"
                        },
                        "nullable": true
                    }
                }
            },
            "PurcahseHistoryItemResp": {
                "type": "object",
                "properties": {
                    "purchaseTime": {
                        "type": "string",
                        "format": "date-time"
                    },
                    "name": {
                        "type": "string",
                        "nullable": true
                    },
                    "description": {
                        "type": "string",
                        "nullable": true
                    },
                    "quantity": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "price": {
                        "type": "number",
                        "format": "double"
                    },
                    "userName": {
                        "type": "string",
                        "nullable": true
                    }
                }
            },
            "StoreItem": {
                "type": "object",
                "properties": {
                    "id": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "name": {
                        "type": "string",
                        "nullable": true
                    },
                    "description": {
                        "type": "string",
                        "nullable": true
                    },
                    "price": {
                        "type": "number",
                        "format": "double"
                    },
                    "installments": {
                        "type": "integer",
                        "format": "int32"
                    }
                }
            },
            "EmptyResult": {
                "type": "object"
            },
            "UserModel": {
                "type": "object",
                "properties": {
                    "id": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "userName": {
                        "type": "string",
                        "nullable": true
                    },
                    "password": {
                        "type": "string",
                        "nullable": true
                    },
                    "name": {
                        "type": "string",
                        "nullable": true
                    },
                    "surname": {
                        "type": "string",
                        "nullable": true
                    },
                    "userRight": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "accountNumber": {
                        "type": "string",
                        "nullable": true
                    },
                    "cookie": {
                        "type": "string",
                        "nullable": true
                    },
                    "status": {
                        "type": "string",
                        "nullable": true
                    },
                    "siteAction": {
                        "type": "string",
                        "nullable": true
                    },
                    "token": {
                        "type": "string",
                        "nullable": true
                    }
                }
            },
            "BuyProductReq": {
                "type": "object",
                "properties": {
                    "id": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "quantity": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "price": {
                        "type": "number",
                        "format": "double"
                    }
                }
            },
            "TransactionDBModel": {
                "type": "object",
                "properties": {
                    "id": {
                        "type": "integer",
                        "format": "int32"
                    },
                    "senderId": {
                        "type": "string",
                        "nullable": true
                    },
                    "receiverId": {
                        "type": "string",
                        "nullable": true
                    },
                    "transactionDateTime": {
                        "type": "string",
                        "format": "date-time"
                    },
                    "reason": {
                        "type": "string",
                        "nullable": true
                    },
                    "amount": {
                        "type": "number",
                        "format": "double"
                    },
                    "reference": {
                        "type": "string",
                        "nullable": true
                    }
                }
            },
            "NewImageModel": {
                "type": "object",
                "properties": {
                    "username": {
                        "type": "string",
                        "nullable": true
                    },
                    "imageUrl": {
                        "type": "string",
                        "nullable": true
                    }
                }
            },
            "AccountBalanceResp": {
                "type": "object",
                "properties": {
                    "balance": {
                        "type": "number",
                        "format": "double"
                    }
                }
            }
        }
    }
}
