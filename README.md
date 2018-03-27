**Authentication**
----
  <_Para autenticarmos, precisamos ._>

* **URL**

  https://auth-api-dev.casinoportugal.pt/connect/token

* **Method:**
  
  `POST` 
* **Basic Auth**
  
| Key | Value |
| --- | --- |
| **ClientId** | yubuy |
| **Client Secret** | hsPY9up2Z7 |

* **Hearders Params**

| Header | Value |
| --- | --- |
| **content-type** | application/x-www-form-urlencoded |

* **Data Params**

| Key | Value |
| --- | --- |
| **grant_type** | client_credentials |

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
    "access_token": "eyJhbGciOiJSUzI1NiIsImtpZCI6IjZCN0FDQzUyMDMwNUJGREI0RjcyNTJEQUVCMjE3N0NDMDkxRkFBRTEiLCJ0eXAiOiJKV1QiLCJ4NXQiOiJhM3JNVWdNRnY5dFBjbExhNnlGM3pBa2ZxdUUifQ.eyJuYmYiOjE1MjE4MDYyODAsImV4cCI6MTUyMTg5MjY4MCwiaXNzIjoiaHR0cHM6Ly9kb2N3YXlhdXRoZGV2LmF6dXJld2Vic2l0ZXMubmV0IiwiYXVkIjpbImh0dHBzOi8vZG9jd2F5YXV0aGRldi5henVyZXdlYnNpdGVzLm5ldC9yZXNvdXJjZXMiLCJhcGkxIl0sImNsaWVudF9pZCI6InNhc2FwcCIsImNsaWVudF9JZCI6IkQwRkZBRDUwLUJDQjctNDE1MC04NUVBLTE4QzNDM0FFRjNFRiIsImNsaWVudF9QYXJ0bmVySWQiOiIxIiwiY2xpZW50X0luc3VyYW5jZSI6IjEiLCJzY29wZSI6WyJhcGkxIl19.Tfc6WpA9LqNNTQldGxch14K9RJPZooHVmEY9x2L5hUhjBIcVFX18xiq3wJLoOg6SKZCkL7irHnwq8pTEVPCfm2xUIE6LMcUnWlAgg8v2tFkCqr_BDQ0OYc_dC3Z0T7u70b1jB6iWc1jPYBqTxOVZt0OGUWjquzaySPXbzBVdzHhQ7gbM-d-Ftn2aYdZkdG0esj6NVxfsBHnET4BwuiuyiyMdD5M3b65yBj_1E9EdT32HQwSOYAQBaqFiYdOe-w8EvRAuuCmPfdyahMZraRufMnP3Cynp9w93spuJmCtCLmTVSnNYP_pljbnq5SMceB7T91tHLzd51OdaKg46btSwqQ",
    "expires_in": 86400,
    "token_type": "Bearer"
}`
 
* **Error Response:**

  <_Most endpoints will have many ways they can fail. From unauthorized access, to wrongful parameters etc. All of those should be liste d here. It might seem repetitive, but it helps prevent assumptions from being made where they should be._>

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{
    "error": "invalid_request"
}`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Email Invalid" }`
    
    
    
    
**Buscar Competições**
----
  <_Para autenticarmos, precisamos ._>

* **URL**

  https://odds-api-issue-5-dev.casinoportugal.pt/api/competitions

* **Method:**
  
  `GET` 
  
* **Hearders Params**

| Header | Value |
| --- | --- |
| **content-type** | application/x-www-form-urlencoded |
| **Authorization** | Bearer + token |


* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
    "success": true,
    "data": [
        {
            "id": 1,
            "marketId": 1,
            "name": "Benfica",
            "odd": 320
        },
        {
            "id": 2,
            "marketId": 1,
            "name": "Empate",
            "odd": 220
        },
        {
            "id": 3,
            "marketId": 1,
            "name": "Porto",
            "odd": 170
        }
    ]
}`
 
* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** ``

 


