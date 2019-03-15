
**API Documentation**


Welcome to the SME API.



## Authentication



A JSON Web Token is used to send information that can be verified and trusted by **means** of a digital signature. It comprises a compact and URL-safe JSON object, which is cryptographically signed to verify its authenticity, and which can also be encrypted if the payload contains sensitive information.

Application may request to access routes, services, or resources on behalf of that user. To do so, it uses an access token, which is in the form of a **JWT** token. user has to provide **JWT** token in header as a authorization in every subsequent request after login.


**Authentication**

Authenticate API in environment with token in response

### HTTP Request

````POST 5.133.176.54:82/api/v1.0/auth/authenticate````


```Request
 user           string                API Key or any secret key
 REQUIRED
```

```Response

200: OK
{
    "success": true,
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpYXQiOjE1NDk1MzEzNTIsImV4cCI6MTU0OTYxNzc1Mn0.6cTXghU1IdDreucri4nQKK-Q2HjnHgL7CtTKmvYTRzo"
}
403: Forbidden
{
    "success": false,
    "message": "403 - Invalid API secret key."
}

```






