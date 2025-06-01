# WebTouchMouse--v2
WebTouchMouse: Remotely control your computer's mouse using a touch-sensitive web interface. Turn your phone or any browser-enabled device into a wireless touchpad!**
# WebTouchMouse 🖱️📱

**WebTouchMouse: Remotely control your computer's mouse using a touch-sensitive web interface. Turn your phone or any browser-enabled device into a wireless touchpad!**

This project allows you to control your computer's mouse pointer, clicks, and scrolling remotely from any device with a web browser on the same network. It's perfect for presentations, controlling media playback from a distance, or any situation where a physical mouse is inconvenient.

## 🚀 How it Works

The system is composed of two main parts:

1.  **Server (Python Backend):**
    * A Python script using **Flask** serves a simple web page.
    * **Flask-SocketIO** is used for real-time, bidirectional communication (via WebSockets) between the server (your computer) and the client (your phone/browser).
    * **PyAutoGUI** listens to commands received via SocketIO (like mouse movements, clicks, scrolls) and executes them on the host computer, effectively controlling the system's mouse.

2.  **Client (Web Interface):**
    * An HTML page styled with **Tailwind CSS** (via CDN) provides the user interface.
    * Vanilla **JavaScript** captures touch events on a designated touchpad area and button clicks.
    * These events are then emitted to the Python server using the **SocketIO client library**.

## ✨ Core Features

* **Real-time Remote Mouse Control:** Smooth cursor movement based on touch input.
* **Web-Based Universal Client:** No need to install any app on your remote device; a web browser is all you need.
* **Touchpad Functionality:**
    * **Mouse Movement:** Single-finger drag on the touchpad area.
    * **Scrolling:** Two-finger drag for vertical scrolling.
* **Click Operations:**
    * Dedicated "Left Click" and "Right Click" buttons.
    * **Select Mode:** A toggle to enable click-and-drag functionality (simulates `mouseDown` and `mouseUp`).
* **Two-Page User Interface:**
    * **Page 1 (Full Controls):** Provides the main touchpad, left/right click buttons, and the "Select Mode" toggle.
    * **Page 2 (Simplified Controls):** Offers a touchpad with a tap-for-left-click feature and a dedicated right-click button for quick actions.
* **Low Latency:** Leverages WebSockets for responsive control.

## 🛠️ Tech Stack

* **Backend:**
    * Python 3
    * Flask
    * Flask-SocketIO
    * PyAutoGUI
* **Frontend:**
