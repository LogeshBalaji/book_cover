# Ex.06 Book Front Cover Page Design
# Date: 26.11.2024
# AIM:
To design a book front cover page using HTML and CSS.

# DESIGN STEPS:
## Step 1:
Create a Django Admin project.

## Step 2:
Create an app in the Django interface.

## Step 3:
Create a folder named 'static' in the app folder.

## Step 4:
Create a new HTML file in the static folder.

## Step 5:
Write the HTML code with relevant CSS properties.

## Step 6:
Choose the appropriate style and color scheme.

## Step 7:
Insert the images in their appropriate places.

## Step 8:
Publish the website in the LocalHost.

# PROGRAM:
## urls.py(server1) 
~~~
from django.urls import path  

from.import views  

urlpatterns=[  
    path('',views.home,name='home')  
]
~~~  
## views.py(server1)  
~~~
from django.shortcuts import render
from http.server import BaseHTTPRequestHandler, HTTPServer
from importlib.resources import contents
from django.http import HttpResponse

content='''
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Application Development - Volume 5</title>
    <link rel="stylesheet" href="styles.css"> <!-- External CSS file link -->
</head>
<body>
    <div class="book">
        <div class="bookcover"></div>
        <div class="center-content">
            <h2 class="title">WED APPLICATION DEVELOPMENT</h2>
            <img src="js.css" alt="JavaScript Icon" class="icon">
            
            <h4 class="subtitle">HTML | CSS | JAVA</h4>
            <img src="js.css3.png" alt="JavaScript Image" class="image-small">
            
            <h3 class="volume">VOLUME 5</h3>
            <img src="web(bc).jpeg" alt="Book Cover" class="cover-img">
            
            <h4 class="tech">WITH HIGH TECHNICAL CODE</h4>
            <h4 class="best-for">BEST FOR COLLEGE STUDIES</h4>
            
            <div class="editor-info">
                <img src="web(bc2).jpeg" alt="Editor Image 1" class="editor-img">
                <span class="editor-text">Editor: ANTONOV</span>
            </div>
            <div class="editor-info">
                <span class="editor-text">Editor in Chief: JONY</span>
                <img src="web(bc3).jpeg" alt="Editor Image 2" class="editor-img">
            </div>
        </div>
    </div>
</body>
<style>
    body {
        font-family: 'Arial', sans-serif;
        margin: 0;
        padding: 0;
        background-color: #222; /* Dark background for contrast */
        color: white;
    }
    
    /* Book Container */
    .book {
        height: 760px;
        width: 500px;
        position: relative;
        margin: 10% auto;
        background: url('black-screen.jpg');
        background-size: cover;
        border: 10px solid white;
        border-radius: 15px; /* Rounded corners */
        padding: 20px;
        perspective: 500px;
        transform-style: preserve-3d;
        box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.5); /* Adding shadow for depth */
    }
    
    /* Centering content */
    .center-content {
        text-align: center;
    }
    
    /* Main Title */
    .title {
        color: yellow;
        font-family: 'Trebuchet MS', sans-serif;
        font-size: 2.5em;
        margin-bottom: 20px;
        text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); /* Text shadow for a glowing effect */
    }
    
    /* Icon Styles */
    .icon {
        width: 50px;
        margin-top: 10px;
    }
    
    /* Subtitle and Smaller Text */
    .subtitle {
        color: yellow;
        font-family: 'Georgia', 'Times New Roman', serif;
        font-size: 1.3em;
        margin-bottom: 10px;
    }
    
    .image-small {
        width: 200px;
        margin-top: 10px;
        transition: transform 0.3s ease; /* Smooth hover effect */
    }
    
    .image-small:hover {
        transform: scale(1.1); /* Slight zoom on hover */
    }
    
    /* Volume Section */
    .volume {
        color: yellow;
        font-size: 1.5em;
        margin-top: 20px;
    }
    
    /* Cover Image */
    .cover-img {
        width: 100px;
        margin-top: 20px;
        border-radius: 8px;
    }
    
    /* High Tech Section */
    .tech {
        color: yellow;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 1.3em;
        margin-top: 20px;
    }
    
    /* Best for College Studies Section */
    .best-for {
        color: white;
        font-size: 1.2em;
        margin-top: 10px;
    }
    
    /* Editor Info Section */
    .editor-info {
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: white;
        font-family: 'Gill Sans', sans-serif;
        margin-top: 15px;
        font-size: 1.1em;
    }
    
    .editor-img {
        height: 50px;
        border-radius: 50%;
        border: 2px solid white;
    }
    
    .editor-text {
        flex: 1;
        padding: 10px;
    }
    
    /* Responsive Design */
    @media screen and (max-width: 600px) {
        .book {
            width: 90%;
            margin-top: 20px;
        }
    
        .title {
            font-size: 2em;
        }
    
        .subtitle {
            font-size: 1.1em;
        }
    
        .editor-info {
            font-size: 1em;
            flex-direction: column;
            align-items: center;
        }
    
        .image-small {
            width: 150px;
        }
    }
</style>
</html>
'''
class Myserver(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
Httpd = HTTPServer(server_address,Myserver)
Httpd.serve_forever()
~~~   
## urls.py(server)
~~~
from django.contrib import admin  
from django.urls import path,include  

urlpatterns = [  
    path('', include('server1.urls')),  
    path('admin/', admin.site.urls),  
]
~~~ 
# OUTPUT:
![Screenshot 2024-12-06 210143](https://github.com/user-attachments/assets/20799d05-41d9-4831-9703-7e3d1e659301)
![Screenshot 2024-12-06 210228](https://github.com/user-attachments/assets/078c7f00-cc9d-48b9-aa5d-85098936dd29)

# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
