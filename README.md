# web-server-with-golang

# Simple Go Web Server

This repository contains a basic Go program that sets up a simple web server using the `net/http` package.

## Getting Started

### Prerequisites

Make sure you have Go installed on your machine. If not, you can download and install it from [the official Go website](https://golang.org/).

### Running the Code

1. Copy the code below:
   
   ```go
   package main

   import (
       "fmt"
       "log"
       "net/http"
   )

   func main() {
       http.HandleFunc("/hello", hello)

       fmt.Printf("Starting server at port 8080\n")
       if err := http.ListenAndServe(":8080", nil); err != nil {
           log.Fatal(err)
       }
   }

   func hello(w http.ResponseWriter, req *http.Request) {
       fmt.Fprintf(w, "Hello, this is my first web server with Golang!")
   }

Create a new file named main.go and paste the copied code into it.

Open a terminal or command prompt.

Navigate to the directory where the main.go file is located.

Run the following command to start the server:

bash
Copy code
go run main.go
Once the server starts, it will print a message indicating that it's running at port 8080.

Code Explanation
The main.go file contains a simple Go program that does the following:

Imports necessary packages (fmt, log, net/http).
Defines a hello function that handles requests to the /hello endpoint by writing a greeting message back to the client.
Sets up a server using http.HandleFunc to handle requests to the /hello endpoint.
Starts the server using http.ListenAndServe on port 8080.
Accessing the Server
Once the server is running, you can access it by opening a web browser and visiting:

bash
Copy code
http://localhost:8080/hello
Alternatively, you can use tools like cURL or Postman to send GET requests to the /hello endpoint.

### Contribution
Feel free to contribute to this project by improving the code, adding new features, or fixing issues. Create a pull request, and your contributions will be considered.
