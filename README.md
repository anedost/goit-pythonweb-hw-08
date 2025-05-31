# Contact Management API

This is a RESTful API for managing contacts, built with **FastAPI**, **SQLAlchemy**, and **PostgreSQL**.

## Features

- Store and manage contact information:
  - First name
  - Last name
  - Email address
  - Phone number
  - Date of birth
  - Additional notes (optional)
- Full CRUD operations:
  - Create a new contact
  - Retrieve all contacts
  - Retrieve a single contact by ID
  - Update an existing contact
  - Delete a contact
- Search contacts by:
  - First name
  - Last name
  - Email
- Retrieve contacts with birthdays in the next 7 days
- Swagger (OpenAPI) documentation
- Data validation using **Pydantic**

## Technologies Used

- FastAPI
- SQLAlchemy
- PostgreSQL
- Pydantic
- Uvicorn

## Installation

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/contact-api.git
cd contact-api
```

2. **Create a virtual environment**

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Set up the PostgreSQL database**

Make sure PostgreSQL is running and configure your connection string in `.env` or config file:

```text
DATABASE_URL=postgresql://username:password@localhost:5432/yourdatabase
```

5. **Run the application**

```bash
uvicorn main:app --reload
```

6. **Open API documentation in the browser**

- Swagger UI: http://localhost:8000/docs  
- ReDoc: http://localhost:8000/redoc

## API Endpoints

| Method | Endpoint                | Description                                 |
|--------|-------------------------|---------------------------------------------|
| POST   | `/contacts/`            | Create a new contact                        |
| GET    | `/contacts/`            | Get all contacts                            |
| GET    | `/contacts/{id}`        | Get a contact by ID                         |
| PUT    | `/contacts/{id}`        | Update a contact                            |
| DELETE | `/contacts/{id}`        | Delete a contact                            |
| GET    | `/contacts/search/`     | Search by first name, last name or email    |
| GET    | `/contacts/birthday/`   | Get contacts with birthdays in the next 7 days |

## Requirements

- Python 3.8+
- PostgreSQL 12+
- pip (Python package manager)

## License

MIT License
