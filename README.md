# authentication-lab

University of Alberta, CMPUT 404 Lab 9 starter repository. Use the different
HTTP authentication schemes provided in Django Rest Framework.

## Getting Started

1. Clone this repository.
    * `git clone https://github.com/uofa-cmput404/authentication-lab.git`
2. Change directory into this repository.
    * `cd authentication-lab`
3. Initialize a Python3 virtual environment
    * `virtualenv venv --python=python3`
4. Activate the virtual environment and install the application dependencies
    ```bash
    source venv/bin/activate
    pip install -r requirements.txt
    ```
5. Run the migrations and create a superuser.
    ```bash
    ./manage.py migrate
    ./manage.py createsuperuser
    ```
6. Start the Django application.
    `./manage.py runserver`

## Answers

**Question 1:** By default, Django uses basic and session authentication. This can be configured by modifying the DEFAULT_AUTHENTICATION_CLASSES attribute inside the REST_FRAMEWORK dictionary in settings.py.

**Question 2:** httpie uses basic authentication when the -a flag is provided.

**Question 3:** In the case of session authentication, a session ID is assigned to the user upon authentication which must then be sent with each request as a cookie. By looking up the provided session ID, the server can retrieve the associated session data. By contrast, token authentication works by associating a client with a given token on the backend which must then be sent as an Authorization HTTP header with each request. Unlike session authentication, token authentication does not require the user to first login; they can simploy provide their assigned token. An advantage of token authentication over basic authentication is that a user can be associated with multiple tokens which can allow for different privileges. 

**Question 4:** abc

**Question 5:** abc
