📌 Task Objective
Build a simple REST API using Flask in Python to manage a list of users stored in memory (no database).
The API must support the following operations:
  GET all users
  GET a single user by ID
  POST create a new user
  PUT update a user
  DELETE delete a user
🚀 Technologies Used
  Python
  Flask
  Postman (for testing)
🧠 How the API Works
  The API stores user data in a Python dictionary:
  users = {}
  Each user looks like:
  {
    "id": 1,
    "name": "John"
  }
▶️ How to Run the Application
  1️⃣ Install Flask
      pip install flask
  2️⃣ Run the Application
      python app.py

You should see:
Running on http://127.0.0.1:5000
📮 API Endpoints & Testing (Using Postman)
✅ 1. Create a User (POST)
  URL:
    POST http://127.0.0.1:5000/users
    Body → raw → JSON
    {
      "id": 1,
      "name": "Sreehari"
    }
Response:
{
  "id": 1,
  "name": "Sreehari"
}
✅ 2. Get All Users (GET)
URL:
GET http://127.0.0.1:5000/users
Response Example:
{
  "1": {
    "id": 1,
    "name": "Sreehari"
  }
}
✅ 3. Get a User by ID (GET)
URL:
GET http://127.0.0.1:5000/users/1
Response:
{
  "id": 1,
  "name": "Sreehari"
}
✅ 4. Update a User (PUT)
URL:
PUT http://127.0.0.1:5000/users/1
Body → JSON
{
  "name": "Sreehari Updated"
}
Response:
{
  "id": 1,
  "name": "Sreehari Updated"
}
✅ 5. Delete a User (DELETE)
URL:
DELETE http://127.0.0.1:5000/users/1
Response:
{
  "message": "User deleted successfully"
}
