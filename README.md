# Task-6
Build a portfolio website with flask
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return """
    <h1>Welcome to My Portfolio</h1>
    <p>Hello, I am Dinesh 👋</p>
    <a href='/about'>About</a> |
    <a href='/projects'>Projects</a> |
    <a href='/contact'>Contact</a>
    """

@app.route("/about")
def about():
    return """
    <h1>About Me</h1>
    <p>I am learning Python and Flask.</p>
    <a href='/'>Home</a>
    """

@app.route("/projects")
def projects():
    return """
    <h1>My Projects</h1>
    <ul>
        <li>To-Do List App</li>
        <li>Calculator App</li>
        <li>REST API using Flask</li>
    </ul>
    <a href='/'>Home</a>
    """

@app.route("/contact")
def contact():
    return """
    <h1>Contact Me</h1>
    <p>Email: dinesh@email.com</p>
    <a href='/'>Home</a>
    """

if __name__ == "__main__":
    app.run(debug=True)
