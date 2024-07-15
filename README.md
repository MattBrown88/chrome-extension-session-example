This repo demonstrates how to implement Session-based authentication for a chrome extension using Django as the backend.

Django Create and activate virtual environment

$ virtualenv env --python=python3.11

$ source ./env/bin/activate

Switch to django_backend directory

$ cd session_chrome_app

Install requirements

$ pip install -r requirements.txt

Migrate

$ python manage.py migrate

Create superuser

$ python manage.py createsuperuser

Start server

$ python manage.py runserver

Chrome Extension Go to chrome://extensions/ in Chrome, Click Load unpacked and upload the chrome_extension folder.

Pin the extension

Using the app Click the extension icon, if the user is not logged in, it should open the login screen (/accounts/login). Once the user has logged in, the badge on the icon will specify if the token is verified, refreshed or expired. In this example, the access token is set to expire in 10s and the refresh token in 30s.
