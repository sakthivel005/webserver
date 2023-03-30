# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```from http.server import HTTPServer, BaseHTTPRequestHandler

content="""
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1> Top five Web Application Development Frameworks </h1>
<h2> 1.Django </h2>
<h2> 2. MEAN Stack </h2>
<h2> 3. REACT </h2>
<h2> 4.  RUBY ON RAILS</h2>
<h2> 5. ASP.NET </h2>

</body>
</html>



"""
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved...")
        self.send_response(200)
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my Webserver")
server_address=('', 80)
httpd=HTTPServer(server_address,MyServer)
httpd.serve_forever()
```

## OUTPUT:
client side output:
![web lab001](https://user-images.githubusercontent.com/120550359/228840650-676ae7b6-805e-45b0-959d-7f04af7883aa.png)


server side output:
![Screenshot_20230330_062458](https://user-images.githubusercontent.com/120550359/228842480-a4587b6d-3672-40d4-8e6f-bac1fd0638a5.png)




## RESULT:
The program is executed succesfully
