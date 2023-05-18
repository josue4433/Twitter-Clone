 Twitter Clone


This project is a Twitter clone . It aims to provide practice in reading, understanding, and extending an existing application by fixing bugs, writing tests, and adding new features.

Table of Contents
Introduction
Setup
Part One: Fix Current Features
Part Two: Add Likes
Part Three: Add Tests
Further Study
Introduction
This exercise extends a somewhat-functioning Twitter clone and provides an opportunity to practice working with an existing codebase. The main goals are:

Reading and understanding the existing codebase.
Fixing bugs and addressing issues in the application.
Writing tests to ensure the application's functionality.
Adding new features to enhance the Twitter clone.
Setup
To set up the project, follow these steps:

Create a Python virtual environment:

console
Copy code
$ python3 -m venv venv
$ source venv/bin/activate
(venv) $ pip install -r requirements.txt
Note: If you are using Python 3.8 instead of 3.7, please refer to the important note in the Setup section of the previous readme file.

Set up the database:

console
Copy code
(venv) $ createdb warbler
(venv) $ python seed.py
Start the server:

console
Copy code
(venv) $ flask run
Part One: Fix Current Features
The first part focuses on fixing existing features in the application. Follow the steps below to address the issues:

Understand the Model:

Read models.py and create a diagram of the four tables.
Pay attention to the unique arrangement in the follows table and understand its purpose.
Use debugging tools (e.g., pdb) to explore the relationships set on the model classes.
Fix Logout:

Implement the logout route, which is currently missing.
Flash a success message and redirect to the login page upon successful logout.
Fix User Profile:

Enhance the user profile page by adding missing elements such as location, bio, and header image.
Fix User Cards:

Update the followers, following, and list-users pages to display the user's bio on user cards.
Profile Edit:

Implement the profile editing functionality, allowing users to edit their profile information.
Validate the entered password and display an error message if it is incorrect.
Update the user's information (excluding the password) upon successful submission.
Redirect to the user detail page on success.
Fix Homepage:

Modify the homepage for logged-in users to display only the last 100 warbles from the users they follow.
Research and Understand Login Strategy:

Review the authentication-related code in app.py.
Gain understanding about how the logged-in user is tracked, the purpose of Flask's g object, and the usage of @app.before_request.
Part Two: Add Likes
In the second part, you'll add a new feature to allow users to "like" warbles. Follow these guidelines to implement the feature:

Users should be able to
