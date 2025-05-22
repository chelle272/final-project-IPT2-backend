# Books 
POST http://127.0.0.1:8000/api/books

{
    "message": "Book Created Successfully",
	"data": {
         "id": 1,
         "title": "The Pain of Onkai",
         "author": "N.K. Edo",
         "category": "Fiction",
         "published": "2022",
         "status": "Available",
         "created_at": "2025-05-18T23:56:54.000000Z"
    }
}
	       
GET http://127.0.0.1:8000/api/books/1

{
    "message": "Record Not Found."
}

DELETE http://127.0.0.1:8000/api/books/1

{
    "message": "Book Deleted Successfully"
}

PUT http://127.0.0.1:8000/api/books/1

{
    "message": "Book Updated Successfully",
    "data": {
        "id": 1,
        "title": "Eloquent JavaScript",
        "author": "Marijn Haverbeke",
        "category": "Programming",
        "published": "2024",
        "status": "Available",
        "create_at": "2025-05-18T23:56:54.000000Z"
    }
}

# Register
POST http://127.0.0.1:8000/api/register

{
    "message": "User registered successfully",         
    "token": "1|RUW0cNeEVKvCONB7qIwOn475uQCqIRzCEAaPUy3I60f50012",
    "user": {
        "name": "Car Doe",
        "email": "cardoe@gmail.com",
        "updated_at": "2025-05-21T00:39:27.000000Z",
        "created_at": "2025-05-21T00:39:27.000000Z",
        "id": 1
    }
}

# Login
POST http://127.0.0.1:8000/api/login

{
    "message": "Login successful",         
    "token": "2|M1phAl38ypGtibE3YNzxEA70jA0h4TMN0kvxJVQ9ebae8c4",
    "user": {
        "id": 1,
        "name": "Car Doe",
        "email": "cardoe@gmail.com",
        "email_verified_at": null,
        "updated_at": “2025-05-21T00:39:27.000000Z”,
        "created_at": "2025-05-21T00:39:27.000000Z",
        "id": 1
    }
}

# Borrow
POST http://127.0.0.1:8000/api/borrow

{        
        "user_id": 1,
        "book_id": "1",
        "borrowed_at": “2025-05-21T00:39:27.000000Z”,
        "due_at": "2025-06-01T00:39:27.000000Z",
        "status": "Borrowed"
    }

# Return
POST http://127.0.0.1:8000/api/return/1
{
    "message": "Book Returned Successfull"
}

POST http://127.0.0.1:8000/api/return/2
{
    "message": "Book are not found"
}


# Logout
POST http://127.0.0.1:8000/api/logout
{
    "message": "Logged out"
}


