# my-bsl-http-server
# Building an HTTP Server using Socket

## Project Description

This project is a low-level HTTP Web Server built from scratch using the **Bonezegei Scripting Language (BSL)** and the **BSL Socket Library**.

The server runs locally on **port 8080** and handles HTTP GET requests using custom route handling.

The server supports the following routes:

* `/` — Default landing page
* `/about` — About page
* Any other route — Custom 404 Not Found page

This project demonstrates how a basic HTTP server can receive client requests through sockets, identify the requested route, and return an appropriate HTTP response.

---

## Technologies Used

* Bonezegei Scripting Language (BSL)
* BSL Socket Library
* Visual Studio Code
* Git
* GitHub

---

## Project Structure

```text
my-bsl-http-server/
├── .gitattributes
├── LICENSE
├── README.md
├── src/
│   └── http.bzg
└── documentation/
    ├── home.png
    ├── about.png
    ├── 404.png
    └── terminal.png
```

---

## Installation and Setup

### 1. Install Visual Studio Code

Download and install Visual Studio Code if it is not already installed.

Open Visual Studio Code and go to the Extensions tab.

Search for:

```text
Bonezegei
```

Install the **Bonezegei Scripting Language Formatter** extension.

Follow the installation instructions provided by the extension to install the BSL Interpreter for your operating system.

---

### 2. Install the BSL Socket Library

Open a terminal or command prompt and run:

```bash
bzg install socket
```

This installs the Socket Library required by the HTTP server.

---

### 3. Clone or Download the Repository

Clone this repository using Git:

```bash
git clone [YOUR_GITHUB_REPOSITORY_URL](https://github.com/a-bbles/my-bsl-http-server/tree/main)
```

Then navigate into the project directory:

```bash
cd my-bsl-http-server
```

---

### 4. Run the HTTP Server

Run the BSL source file:

```bash
bzg src/http.bzg
```

If the server starts successfully, the terminal should display:

```text
Socket Ready
Server running on http://localhost:8080/
```

---

## Usage

Once the server is running, open a web browser and visit the following addresses.

### Home Page

Open:

```text
http://localhost:8080/
```

The server responds with a `200 OK` status and displays the default landing page.

![Home Page](documentation/home.png)

---

### About Page

Open:

```text
http://localhost:8080/about
```

The server responds with a `200 OK` status and displays information about the project.

![About Page](documentation/about.png)

---

### 404 Not Found Page

Open an unmapped route such as:

```text
http://localhost:8080/anything
```

The server responds with a `404 Not Found` status and displays a custom error page.

![404 Page](documentation/404.png)

---

## Terminal Screenshot

The following screenshot shows the terminal while the HTTP server is running.

![Terminal](documentation/terminal.png)

---

## HTTP Routes

| Route           | HTTP Status     | Description          |
| --------------- | --------------- | -------------------- |
| `/`             | `200 OK`        | Default landing page |
| `/about`        | `200 OK`        | About page           |
| Any other route | `404 Not Found` | Custom error page    |

---

## How the Server Works

The server follows these basic steps:

1. Initialize the socket library.
2. Create a server socket.
3. Bind the server to port `8080`.
4. Listen for incoming client connections.
5. Accept a client connection.
6. Read the HTTP request.
7. Determine which route was requested.
8. Generate the appropriate HTTP response.
9. Send the response to the client.
10. Close the client connection.
11. Continue listening for new connections.

---

## Learning Outcomes

Through this laboratory activity, the project demonstrates:

* Basic socket programming
* HTTP request and response handling
* Custom route handling
* HTTP status codes
* HTML response generation
* Use of the Bonezegei Scripting Language
* Use of Git and GitHub for project management

---

## Author

**Shifra "Abby" Garcia**

BS Information Technology
Network Systems

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for more information.

```
```
