# REST API with Django and Django REST Framework (DRF)

This is a simple REST API built using Django and Django REST Framework (DRF). The API allows CRUD operations on an `Item` model, which has fields for `name`, `description`, `price`, and `created_at`.

## Features
- **Endpoints for Items**:
  - `GET /api/items/`: Retrieve a list of all items.
  - `POST /api/items/`: Create a new item.
  - `GET /api/items/<id>/`: Retrieve details of a specific item.
  - `PUT /api/items/<id>/`: Update an existing item.
  - `DELETE /api/items/<id>/`: Delete an item.
- **Django Admin Panel**: Access the admin interface to manage data manually.

## Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
Create a virtual environment:

python -m venv env

Activate the virtual environment:
.\env\Scripts\activate

Install dependencies:
pip install django djangorestframework


Run database migrations:
python manage.py makemigrations
python manage.py migrate

Create a superuser for the admin panel (optional):

python manage.py createsuperuser
Start the development server:

python manage.py runserver


Endpoints
Method	Endpoint	Description
GET	/api/items/	Retrieve all items
POST	/api/items/	Create a new item
GET	/api/items/<id>/	Retrieve a specific item
PUT	/api/items/<id>/	Update a specific item
DELETE	/api/items/<id>/	Delete a specific item




Directory Structure

myproject/
│
├── myproject/
│   ├── settings.py    # Project settings
│   ├── urls.py        # URL routing for the project
│   ├── wsgi.py        # WSGI configuration
│
├── myapp/
│   ├── models.py      # Database models
│   ├── serializers.py # DRF serializers
│   ├── views.py       # API views
│   ├── urls.py        # URL routing for the app
│
└── manage.py          # Django's command-line utility



Testing the API
Use tools like Postman, curl, or your browser (for GET requests) to interact with the API.

Example Requests
1. Retrieve All Items

curl -X GET http://127.0.0.1:8000/api/items/
2. Create a New Item

curl -X POST http://127.0.0.1:8000/api/items/ \
-H "Content-Type: application/json" \
-d '{"name": "Test Item", "description": "This is a test", "price": "9.99"}'
3. Update an Item

curl -X PUT http://127.0.0.1:8000/api/items/1/ \
-H "Content-Type: application/json" \
-d '{"name": "Updated Item", "description": "Updated description", "price": "19.99"}'
4. Delete an Item

curl -X DELETE http://127.0.0.1:8000/api/items/1/


Development
To modify or extend the project:

Add models in myapp/models.py.
Create serializers in myapp/serializers.py.
Define API views in myapp/views.py.
Add routes in myapp/urls.py.
License
This project is licensed under the MIT License.

Acknowledgments
Built with Django and Django REST Framework.
