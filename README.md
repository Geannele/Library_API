# 📚 Library Management System API using SLIM Framework

## Overview 
The Library Management System API is built using the SLIM Framework to create lightweight, RESTful endpoints. It’s a simple yet powerful example of how SLIM makes API development easy and efficient, providing a seamless way to manage resources like books, members, and transactions.

## Key Features 
### 🔒 JWT Authentication 
- Token-based user verification for secure API access. One-time token validity to enhance session security.
### 🔍 Advanced Search and Filters 
- Search for books by genre, author, availability, or publication date.
### 📖 Comprehensive CRUD Operations
- Add, update, delete, and view book records with search by title, author, or unique id.

## Endpoints🚀 
### User Endpoints 👤
**Method:** POST 
**Endpoint:** users/register
Register a new user.
**Payload:**
{
    "email": "gean@gmail.com",
    "username": "Geannele",
    "password": "gean1234"
}

**Response:**
{
    "status": "success",
    "data": null
}

**Method:** POST 
**Endpoint:** users/login
Login and obtain JWT token
**Payload:**
{
    "email": "gean@gmail.com",
    "password": "gean1234"
}

**Response:**
{
    "status": "success",
    "token": ""
}

**Method:** GET
**Endpoint:** users/displayAll
View all users in the system.
**Payload:**
{
    "token": ""
}

**Response:**
{
    "status": "success",
    "new_token": ""
    "data": [
        {
           "userid" "",
           "email": "",
           "username": "",
        }
    ]
}

### Book Endpoints 📚
**Method:** POST 
**Endpoint:** books/add
Add a new book.
**Payload:**
{
    "author": "authors_name",
    "title": "book_title",
    "genre": "book_genre",
    "token": ""
}

**Response:**
{
    "status": "succcess",
    "new_token": ""
}

**Method:** PUT 
**Endpoint:** books/update
Update an existing book.
**Payload:**
{
    "author": "authors_name",
    "title": "book_title",
    "genre": "book_genre",
    "bookCode" "bookCode"
    "token": ""
}

**Response:**
{
    "status": "success",
    "new_token": ""
}

**Method:** DELETE 
**Endpoint:** books/delete
Delete a book by bookCode.
**Payload:**
{
    "bookCode": "bookCode",
    "token": ""
}

**Response:** 
{
    "status": "success",
    "new_token": ""
}

**Method:** GET
**Endpoint:** books/displayAll
Display all books by a specific author  
**Payload:**
{
    "token": ""
}
**Response:**
{
    "status": "success",
    "new token": ""
    "data": [
        {
           "bookid": "",
           "title": "",
           "genre": "",
           "bookCode": "",
           "authorid": "",
           "authorname": ""
        }
    ]
}

**Method:** GET
**Endpoint:** /books/displayauthorsbooks
Display all authors by a specific books
**Payload:**
{
    "token": "",
    "authorname": "author_name"
}
**Response:**
{
    "status": "success",
    "new_token":
    "data": [
      {
        "bookid": "book_ID",
        "title": "book_title",
        "genre": "book_genre",
        "bookCode": "bookCode",
        "authorid": "author_id",
        "authorname": "author_name"
      }
   ]
}

**Method:** GET
**Endpoint:** /books/displaytitlebooks
Search books by title.
**Payload:**
{
    "token": "",
    "booktitle": "book_title"
}
**Response:**
{
    
  "status": "success",
  "new_token": "",
  "data": [
    {
      "bookid": ,
      "title": "",
      "genre": "",
      "bookCode": "",
      "authorid": ,
      "authorname": ""
    }
  ]
}

**Method:** GET
**Endpoint:** books/displaygenrebooks
Search books by genre.
**Payload:**
{
    "token": "",
    "bookgenre": "book_genre"
}
**Response:**
{
    "status": "success",
  "new_token": "",
  "data": [
    {
      "bookid": ,
      "title": "",
      "genre": "",
      "bookCode": "",
      "authorid": ,
      "authorname": ""
    }
  ]
}

### Author Endpoints ✍️
**Method:** POST
**Endpoint:** /authors/add
Add a new author.
**Payload:**
{
    "authorname": "author_name",
    "token": ""
}
**Response:**
{
    "status": "success",
    "new_token": ""
}

**Method:** PUT
**Endpoint:** /authors/update
Update author information.
**Payload:**
{
    "authorid": "author_id",
    "authorname": "author_name",
    "token": ""
}
**Response:**
{
    "status": "success",
    "new_token": ""
}

**Method:** DELETE
**Endpoint:** /authors/delete
Delete an author by ID.
**Payload:**
{
    "authorid": "author_name",
    "token": ""
}
**Response:**
{
    "status": "success",
    "new_token": ""
}

**Method:** GET
**Endpoint:** /authors/display
View all authors.
**Payload:**
{
    "token": ""
}
**Response:**
{
    
  "status": "success",
  "new_token": ""
  "data": [
    {
      "authorid": ,
      "authorname": ""
    }
  ]
}




 
