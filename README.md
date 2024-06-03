# Python-Flask-Login-API
Build a login API using Python Flask

# Install requirements
Clone the Workshop repository.
Make sure you have Python, pip, and virtualenv installed.
Activate a virtualenv.
Install Flask with Pip $ pip install Flask.

# Run your flask Server
Run your server for the first Time. If everything done correctly, our App is only returning a "Hello, World !" string on the Home Page. Let's pump that

# Create your first app route
Using the render_template method, create a "welcome" route for our app.

The goal of the route is just to return the corresponding html template.
Once the server running, you should see [this](http://localhost:5000/welcome) page.

# Now let's build the login logic
**Define the route and allowed methods:**
Use the @app.route decorator to specify the route /login and allow both GET and POST methods.

**Initialize an error variable:**
This will be used to store any error messages related to the login process.

**Check the request method:**
Determine if the request method is POST (indicating form submission).

**Validate credentials:**
Check if the provided username and password match the expected values.
Handle invalid credentials: If the credentials do not match, set an error message.

**Handle successful login:**
If the credentials are correct, redirect the user to the home page (corresponding to the "/" route).

**Render the login template:**
If the request method is GET or if there was an error during login, render the login.html template with the error message (if any)

Now that users have the ability to login, **we need to protect that URL "/welcome" from unauthorized access**.

In other words, when an end user hits that endpoint, unless they are already logged in, then they should be immediately sent to the login page.

# Add user protection on our app
**Import necessary modules and set up a secret key for sessions.**
Import the following modules/packages : session, flash, wraps in functools

**Update the login logic to set a session variable upon successful login.**
Set a secret key for session management

**Create a logout route to allow users to log out.**

# Feel free to add some google, Github integration to the login page !

**Add a decorator function to check login status before accessing certain routes.**
A decorator is just a function that takes another function as a parameter and returns another function.

Your decorator checks if the user is logged in by looking for the logged_in key in the session.
If the key is not found, **the user is redirected to the home page with a flash message.**
