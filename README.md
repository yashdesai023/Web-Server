# Web Server – Java Threading Demonstration

This repository showcases the implementation of a basic HTTP web server in Java, emphasizing different threading models. It's designed to illustrate how threading can impact the performance and scalability of server applications.

## 🧠 Overview

The project demonstrates three distinct threading approaches:

1. **SingleThreaded**: Processes all client requests sequentially on a single thread.
2. **MultiThreaded**: Spawns a new thread for each incoming client connection.
3. **ThreadPool**: Utilizes a fixed-size thread pool to manage client connections efficiently.

Each model serves as an educational example to understand the trade-offs between simplicity, resource utilization, and concurrency in server design.

## 📁 Project Structure

```

Web-Server/
├── SingleThreaded/
│   └── SingleThreaded.java
├── MultiThreaded/
│   └── MultiThreaded.java
├── ThreadPool/
│   └── ThreadPool.java
├── README.md
└── .gitattributes
```



* **SingleThreaded.java**: Implements a server that handles one client at a time.
* **MultiThreaded.java**: Creates a new thread for each client connection, allowing concurrent handling.
* **ThreadPool.java**: Employs a thread pool to manage a fixed number of threads for handling client requests.

## 🚀 Getting Started

### Prerequisites

* Java Development Kit (JDK) 8 or higher

### Compilation and Execution

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yashdesai023/Web-Server.git
   cd Web-Server
   ```



2. **Compile and run the desired server model**:

   * **SingleThreaded**:

     ```bash
     cd SingleThreaded
     javac SingleThreaded.java
     java SingleThreaded
     ```

   * **MultiThreaded**:

     ```bash
     cd MultiThreaded
     javac MultiThreaded.java
     java MultiThreaded
     ```

   * **ThreadPool**:

     ```bash
     cd ThreadPool
     javac ThreadPool.java
     java ThreadPool
     ```

3. **Testing the Server**:

   Open a web browser or use tools like `curl` or `Postman` to send HTTP requests to `http://localhost:8080`.

## 📚 Educational Insights

* **SingleThreaded**: Simplest to implement but cannot handle multiple clients simultaneously.
* **MultiThreaded**: Allows concurrent client handling but may lead to resource exhaustion under high load due to unbounded thread creation.
* **ThreadPool**: Balances concurrency and resource management by limiting the number of active threads.

## 🛠️ Potential Enhancements

* Implementing graceful shutdown mechanisms.
* Adding support for HTTP methods beyond GET.
* Incorporating logging frameworks for better traceability.
* Enhancing error handling and response messages.

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---
