# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
```
<!DOCTYPE html>
<html>
<head>
    <title>TCP/IP Protocol Suite</title>
</head>
<body>
    <h1>Protocols in TCP/IP Protocol Suite</h1>
    <ul>
        <li>HTTP (HyperText Transfer Protocol)</li>
        <li>FTP (File Transfer Protocol)</li>
        <li>TCP (Transmission Control Protocol)</li>
        <li>UDP (User Datagram Protocol)</li>
        <li>IP (Internet Protocol)</li>
        <li>SMTP (Simple Mail Transfer Protocol)</li>
        <li>DNS (Domain Name System)</li>
        <li>DHCP (Dynamic Host Configuration Protocol)</li>
    </ul>
</body>
</html>
```
```
from http.server import SimpleHTTPRequestHandler, HTTPServer

# Set the server address and port
host = 'localhost'
port = 8000

# Create HTTP server using the built-in request handler
server = HTTPServer((host, port), SimpleHTTPRequestHandler)

print(f"Server started at http://{host}:{port}")
print("Press Ctrl+C to stop the server")

# Run the server
try:
    server.serve_forever()
except KeyboardInterrupt:
    print("\nServer is shutting down...")
    server.server_close()
```


## OUTPUT:
![Screenshot (74)](https://github.com/user-attachments/assets/a068ceb0-5af6-4084-88fe-371579eb45c4)



## RESULT:
The program for implementing simple webserver is executed successfully.
