
# Django Email Sending Example

This repository demonstrates how to send emails using Django. Follow the steps below to set up and test the email-sending functionality.

## Pre-requisites

Ensure you have the following installed:

- Python 3.6+
- Django 3.2+

## Getting Started

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/send-email-django.git
cd send-email-django
```

### Step 2: Set Up Virtual Environment

Create and activate a virtual environment:

```bash
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
```

### Step 3: Install Dependencies

Install the required Python packages:

```bash
pip install -r requirements.txt
```

### Step 4: Configure Email Settings

Update the `settings.py` file with your email configuration. Here is an example configuration:

```python
# settings.py
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'your-email@gmail.com'
EMAIL_HOST_PASSWORD = 'your-email-password'  # Use app password for Gmail
```

> **Note:** Avoid hardcoding sensitive information. Use environment variables or a secrets manager for better security.




### Step 6: Configure URL Routing

Add a URL pattern for the email view in `urls.py`:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('send-email/', views.send_email, name='send_email'),
]
```

### Step 7: Test the Email Functionality

Run the Django development server:

```bash
python manage.py runserver
```

Visit the endpoint in your browser or use a tool like Postman:

```
http://127.0.0.1:8000/send-email/
```

You should receive an email at the recipient address on the console.



### Setup
1. Create a folder and put all the files inside it.
2. Create a virtual environtment - `virtualenv env`
3. Activate VirtualENV - Ubuntu - `source env/bin/activate`   |   Windows - `. .\env\Scripts\activate`
4. Run requirements.txt - `pip3 install -r requirements.txt`
5. Run the Application - `python3 manage.py runserver`
6. Go to - http://localhost:8000/
