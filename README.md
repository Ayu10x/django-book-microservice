
# Django Book Microservice

This project is a **Django microservice** that provides a REST API for managing books.  
Built using **Django Rest Framework (DRF)**, it supports CRUD operations for book resources.

## Features
- List all books
- Create a new book
- Retrieve a book by ID
- Update book details
- Delete a book

## Technologies Used
- Python 3.x
- Django 4.x
- Django Rest Framework (DRF)

## Endpoints
| Method | Endpoint             | Description            |
|--------|----------------------|------------------------|
| GET    | `/api/books/`        | List all books         |
| POST   | `/api/books/`        | Create a new book      |
| GET    | `/api/books/<id>/`   | Retrieve a book by ID  |
| PUT    | `/api/books/<id>/`   | Update a book by ID    |
| DELETE | `/api/books/<id>/`   | Delete a book by ID    |

## Setup Instructions

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Ayu10x/django-book-microservice.git
   cd django-book-microservice
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv env
   source env/bin/activate  # Linux/macOS
   env\Scripts\activate      # Windows
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run migrations**:
   ```bash
   python manage.py migrate
   ```

5. **Run the server**:
   ```bash
   python manage.py runserver
   ```

## Example Request
Here is an example of how to **create a new book** using `curl`:

```bash
curl -X POST http://127.0.0.1:8000/api/books/ \
-H "Content-Type: application/json" \
-d '{
  "title": "Microservices with Python",
  "author": "John Doe",
  "published_date": "2024-10-25",
  "isbn": "1234567890123"
}'
```