Here's the complete `README.md` file content:

---

````markdown
 FastAPI Motor Control API

This project is a simple FastAPI application that provides an HTTP POST endpoint to receive and process motor control commands such as `on`, `off`, `clockwise`, and `anticlockwise`. It's designed to simulate or interface with motor control logic.

---

 📦 Requirements

Ensure Python 3.8 or higher is installed.

 Optional: Create a Virtual Environment

```bash
python -m venv venv
 Activate the virtual environment
 On Windows:
venv\Scripts\activate
 On macOS/Linux:
source venv/bin/activate
````

 Install Required Libraries

Install the necessary packages using pip:

```bash
pip install fastapi uvicorn
```

---

 🚀 Running the Server

 Run Normally

```bash
uvicorn main:app --host 0.0.0.0 --port 8000
```

This starts the API server on all network interfaces at port 8000.

 Run in Development Mode with Auto-Reload

```bash
uvicorn main:app --reload
```

This will start the server at `http://127.0.0.1:8000` and reload it automatically on code changes.

---

 📡 Using the API

Send a `POST` request to the `/command` endpoint with a JSON body containing an `action` key.

 Example Request Using `curl`

```bash
curl -X POST "http://127.0.0.1:8000/command" \
     -H "Content-Type: application/json" \
     -d "{\"action\": \"on\"}"
```

---

 ✅ Supported Actions

 `on` – Turns the motor on
 `off` – Turns the motor off
 `clockwise` – Rotates the motor clockwise
 `anticlockwise` – Rotates the motor anticlockwise

Each command is printed to the console and can be extended to interact with actual hardware (e.g., via GPIO, serial communication, etc.).

---

 📁 Project Structure

```
Fast_Api/
├── main.py           FastAPI app with command logic
├── README.md         Project documentation
```

---

 📖 Overview

 `main.py` creates a FastAPI app.
 A POST route `/command` accepts a JSON body with an `action` string.
 Based on the command received, it prints an appropriate message simulating motor behavior.
 Easily extensible for real hardware integration.

---


