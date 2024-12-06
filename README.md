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
from django.urls import path  

from.import views  

urlpatterns=[  
    path('',views.home,name='home')  
]  
## views.py(server1)  
~~~
from django.shortcuts import render    
from django.http import HttpResponse  
#Create your views here.  

def home(request):  
    return render(request, 'home.html') 
content="""
    """
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
from django.contrib import admin  
from django.urls import path,include  

urlpatterns = [  
    path('', include('server1.urls')),  
    path('admin/', admin.site.urls),  
]  
## creating new folder templates in that new html file 'home'

~~~
<link rel="stylesheet" href="black-screen.jpg">
<div class="book">
    <div class="bookcover"></div>
    <center>
        <br>
    <div style="color:yellow; font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;"><h2 style="display: block;">WED APPLICATION DEVELOPMENT</h2></div>
    <img src="js.css" width="50px">
    <div style="color:yellow; font-family: Georgia, 'Times New Roman', Times, serif;"><h4 class="title.txt1">HTML|CSS|JAVA</h4><img src="js.css3.png" width="200px"></div>
    <div style="color:yellow;"><h3>VOLUME 5</h3></div>
    <img src="web(bc).jpeg" height="100px">
    <div style="color:yellow; font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;"><h4>WITH HIGH TECHNICAL CODE</h4></div>
    <div style="color: white;"> <h4>BEST FOR COLLEGE STUDIES</h4></div>
    <div style="color: white;font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;"><img align="left" src="web(bc2).jpeg" height="50px">Editor:ANTONOV</div>
    <div style="color: white;font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;">Editor in chief:JONY<img align="right" src="web(bc3).jpeg" height="50px"></div>
</center>
</div>
<style>
    .book
    {
        height: 650px;
        width:450px;
        position: relative;
        margin-left: 40%;
        margin-top: 10%;
        background: url(black-screen.jpg);
        background-size: cover;
        perspective: 500px;
        transform-style: preserve-3d;
        border: 10px solid white;
    }
</style>
~~~

# OUTPUT:
![Screenshot 2024-12-06 104921](https://github.com/user-attachments/assets/4a9e15c5-c659-4f0f-9deb-1eaca82fd5f9)
![Screenshot 2024-12-06 104907](https://github.com/user-attachments/assets/0c29f5ad-430d-409f-85ce-83ebb162d88e)
![Screenshot 2024-12-06 104638](https://github.com/user-attachments/assets/199c4939-60af-469e-b98c-572f2d06c993)



# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
