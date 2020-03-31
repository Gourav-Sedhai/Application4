# Application4
#Website
#Home
{%extends "layout.htm"%}
{%block content%}
<div class="home">
    <h1>My HomePage</h1>
    <p>This is a test website.</p>
</div>    
{%endblock%}

#About
{%extends "layout.htm"%}
{%block content%}
<div class="about">
    <h1>My About Page</h1>
    <p>This is a test website.</p>
</div>
{%endblock%}

#Layout
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flask App</title>
    <link rel="stylesheet" href={{url_for('static', filename='css/main.css')}}>
</head>
<body>
    <header>
        <div class="container">
            <h1 class="logo">ALIEN's Web App</h1>
            <strong><nav>
                <ul class="menu">
                    <li><a href="{{ url_for('home') }}">Home</a></li>
                    <li><a href="{{ url_for('about') }}">About</a></li>
                </ul>    
            </nav></strong>
        </div>
    </header>
    <div class="container">
        {%block content%}
        {%endblock%}
    </div>
</body>
</html>
