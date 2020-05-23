go run main.go

## Intro to REST APIs in Go 
https://medium.com/the-andela-way/build-a-restful-json-api-with-golang-85a83420c9da

```bash
# List all events
curl -s http://127.0.0.1:8080/events | jq .

# Add a new Event
curl -s -d @payload.json http://127.0.0.1:8080/event | jq .
curl -s http://127.0.0.1:8080/events | jq .

# Update an event
curl -s -X PATCH -d @update.json http://127.0.0.1:8080/events/1
curl -s http://127.0.0.1:8080/events | jq .

# Delete an Event
curl -s -X DELETE http://127.0.0.1:8080/events/1 | jq .
curl -s http://127.0.0.1:8080/events | jq .
```