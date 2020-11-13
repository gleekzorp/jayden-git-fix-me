# Python git-fix-me

> Python Flask backend app for playing with a basic library. It has the ability to add books with information such as the Title, author, genre etc.. It uses a flask sqlite database along with flask-marshmallow for object serialization/deserialization.

## Dependencies

- Python
  - [python](https://www.python.org/)
- Flask
  - [flask-pypi](https://pypi.org/project/Flask/)
  - [flask-docs](https://flask.palletsprojects.com/en/1.1.x/)
- Flask-SQLAlchemy
  - [flask-sqlalchemy-pypi](https://pypi.org/project/Flask-SQLAlchemy/)
  - [flask-sqlalchemy-docs](https://flask-sqlalchemy.palletsprojects.com/en/2.x/)
- Flask-Marshmallow
  - [flask-marshmallow-pypi](https://pypi.org/project/flask-marshmallow/)
  - [flask-marshmallow-docs](https://flask-marshmallow.readthedocs.io/)
- Marshmallow-SQLAlchemy
  - [marshmallow-sqlalchemy-pypi](https://pypi.org/project/marshmallow-sqlalchemy/)
  - [marshmallow-sqlalchemy-docs](https://marshmallow-sqlalchemy.readthedocs.io/en/latest/)

​

## Getting Started

- Make sure you are in your Server Folder

- download zip or clone
- Install all dependencies
  ```
  $ pipenv install
  ```
  ​
- Create your sqlite database
  ```
  $ pipenv shell
  $ python
  >>> from app import db
  >>> db.create_all()
  ```
  ​
- Start your flask server
  ```
  $ python app.py
  ```
  ​

## Flask Routes (test in postman or build a front-end)

- Create Book

  - METHOD: `POST`
  - URL: http://localhost:5000/api/add-book
  - BODY: `application/json`
    ```json
    {
      "title": "title",
      "author": "author",
      "url": "url",
      "genre": "genre",
      "star_rating": "1",
      "book_read": false
    }
    ```

- GET All Books

  - METHOD: `GET`
  - URL: http://localhost:5000/api/books

- Update Book-read

  - METHOD: `PATCH`
  - URL: http://localhost:5000/api/book-read/<id>
  - BODY: `application/json`
    ```json
    {
      "bookread": true
    }
    ```

- DELETE a single book
  - METHOD: `DELETE`
  - URL: http://localhost:5000/api/delete-book/<id>
