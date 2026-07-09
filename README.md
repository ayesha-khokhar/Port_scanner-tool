# Port_scanner-tool
# 🔍 Port Scanner

A simple command-line port scanner built with Python that scans a target host for open ports within a given range.

---

## 📋 Description

This tool uses Python's built-in `socket` library to attempt TCP connections on each port in the specified range. If a connection succeeds, the port is reported as **OPEN**.

---

## 🚀 Usage

```bash
python3 portscanner.py TARGET START_PORT END_PORT
```

### Example

```bash
python3 portscanner.py 192.168.1.1 20 100
```

This will scan ports **20 to 100** on the target `192.168.1.1`.

---

## 🛠️ Requirements

- Python 3.x
- No external libraries needed — uses built-in modules only:
  - `sys`
  - `socket`
  - `time`

---

## ⚙️ How It Works

1. Takes 3 command-line arguments: target IP/hostname, start port, end port.
2. Resolves the hostname to an IP address using `socket.gethostbyname()`.
3. Loops through each port in the given range.
4. For each port, creates a TCP socket and tries to connect with a **2-second timeout**.
5. If the connection is successful → prints **"Port X is OPEN"**.
6. Closes the socket after each attempt.

---

## ⚠️ Notes

- Only use this tool on systems you **own or have permission** to scan.
- Unauthorized port scanning may be **illegal**.
- Timeout is set to `2` seconds per port — scanning large ranges may take time.

---

## 📁 Project Structure

```
port_scanner/
│
└── portscanner.py       # Main scanner script
```

---

## 👩‍💻 Author

Made with Python 🐍


Demo Video Link:

https://drive.google.com/file/d/1caf1Q9eWvi3DBLfu4dUw_2MyaEg5itTD/view?usp=drivedk
