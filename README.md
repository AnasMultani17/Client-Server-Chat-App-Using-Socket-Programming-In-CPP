
# Client-Server Chat Application in C++

A real-time terminal-based chat application built using **C++** and **Socket Programming** for both Linux-based server and client communication.

## 🚀 Features
- Multi-client support with concurrent communication via **multi-threading**
- Real-time chat system with colored terminal output for different users
- Graceful exit using signal handling (`Ctrl + C`)
- Optimized for **low-latency**, responsive communication
- Lightweight and runs entirely in terminal (no GUI dependencies)

## 🧠 Technologies Used
- **C++**
- **POSIX Sockets**
- **Multithreading (`<thread>`, `<mutex>`)**
- **Linux system calls**: `socket()`, `bind()`, `listen()`, `accept()`, `connect()`, `send()`, `recv()`
- ANSI escape sequences for terminal coloring

## 🛠 How to Run

### Compile the Server
```bash
g++ server.cpp -o server -pthread
```

### Compile the Client
```bash
g++ client.cpp -o client -pthread
```

### Start the Server
```bash
./server
```

### Start the Client (in a different terminal)
```bash
./client
```

> 📝 Note: Both server and client must run on the same machine or within the same network. You can also replace `INADDR_ANY` with a specific IP if required.

## 📂 File Structure
- `server.cpp` - Handles multiple clients, message broadcasting, and client management
- `client.cpp` - Connects to server, sends/receives messages with UI feedback

## 🧩 Concepts Demonstrated
- Concurrent programming with thread safety
- Terminal manipulation and formatting
- Custom protocol for broadcasting messages
- Use of `mutex` and `signal` for safe thread and process control

## 📜 License
This project is for educational purposes only. Contributions and forks are welcome!
