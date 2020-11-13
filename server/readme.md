# Python git-fix-me

> Python Flask backend app for playing with a basic library. It has the ability to add books with information such as the Title, author, genre etc.. It uses a flask sqlite database along with flask-marshmallow for object serialization/deserialization. You can create a user, hash their password, and store that data in a database. During the login process it will check that data.
> ​

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
      "username": "test",
      "password": "test"
    }
    ```
- GET

  - METHOD: `GET`
  - URL: http://localhost:5000/api/books
  - BODY: `application/json`

    ```json
    {
      "username": "test",
      "password": "test"
    }
    ```

    - PUT / PATCH by Id
    - METHOD: `PATCH`
    - URL: http://localhost:5000/api/book-read/<id>
    - BODY: `application/json`

      ```json
      {
        "username": "test",
        "password": "test"
      }
      ```

    - DELETE
    - METHOD: `DELETE`
    - URL: http://localhost:5000/api/delete-book/<id>
    - BODY: `application/json`
      ```json
      {
        "username": "test",
        "password": "test"
      }
      ```
