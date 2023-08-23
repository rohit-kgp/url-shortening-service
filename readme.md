
# URL Shortener

• Developed a robust URL shortening service in Golang, allowing users to input lengthy URLs and receiving compact short URL

• Implemented a custom key generation algorithm to ensure uniqueness and optimized storage of short URLs in database

• Engineered a seamless redirection mechanism that efficiently translates short URLs back to their original long forms

## Run

Run with Docker

```bash
docker-compose up
```



Redirect
Open url in your browser [http://localhost:8080/bN](http://localhost:8080/1)

Get info for url shortener\
`curl http://localhost:8080/info/1 `

Response:
```json
{
 "success":true,
 "response": {
    "url":"www.youtube.com",
    "visited":true,
    "count":1
 }
}
```

## Using Postman

```
POST http://localhost:8080/encode/
```
Request Body:

```
{
    "url":"erp.iitkgp.ac.in"
}
```

Response:
```
{
    "success": true,
    "response": "http://localhost:8080/1"
}
```