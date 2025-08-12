# Build-a-REST-API-with-Flask

1) GET /users :-
curl -X GET http://localhost:5000/users

Response:-

[
  {
    "id": 1,
    "name": "Alice",
    "email": "alice@example.com"
  },
  {
    "id": 2,
    "name": "Bob",
    "email": "bob@example.com"
  }
]

2) POST /users :-
curl -X POST http://localhost:5000/users \
     -H "Content-Type: application/json" \
     -d '{"name": "Charlie", "email": "charlie@example.com"}'

Response :- 

{
  "id": 3,
  "name": "Charlie",
  "email": "charlie@example.com",
  "message": "User created successfully"
}

3) PUT /users/<id> :-
   curl -X PUT http://localhost:5000/users/2 \
     -H "Content-Type: application/json" \
     -d '{"name": "Bob Smith", "email": "bobsmith@example.com"}'

Response :- 

{
  "id": 2,
  "name": "Bob Smith",
  "email": "bobsmith@example.com",
  "message": "User updated successfully"
}

4) DELETE /users/<id> :-
   curl -X DELETE http://localhost:5000/users/1

Response :- 

{
  "message": "User with id 1 deleted successfully"
}


