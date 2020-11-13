# Book Api

Flask
https://flask.palletsprojects.com/en/1.1.x/
Flask SQLAlchemy
https://flask-sqlalchemy.palletsprojects.com/en/2.x/
Flask Marshmallow
https://flask-marshmallow.readthedocs.io/en/latest/
Marshmallow-sqlalchemy
https://marshmallow-sqlalchemy.readthedocs.io/en/latest/
Api Endpoints

Get all guides

URL: http://localhost:5000/guide
Method: Get
Create a guide

URL: http://localhost:5000/guide
Method: Post
Send Body of json:
{
"title": "some title",
"content": "some content"
}

Get a guide

URL: http://localhost:5000/guide/id
Method: Get
Edit a guide

URL: http://localhost:5000/guide/id
Method: Put
Send Body of json:
{
"title": "Updated title",
"content": "Updated content"
}

Delete a guide

URL: http://localhost:5000/guide/id
Method: Delete
Environment Stuff
open terminal in folder
Run this in the terminal:
$ pipenv --three (sets python3 as the version for that environment)
use the following command to enter shell:
$ pipenv shell
install packages locally in the pipenv through this command:
\$ pipenv install numpy" or whatever the library is called
command to open repl is still python

To start server
\$ python app.py
