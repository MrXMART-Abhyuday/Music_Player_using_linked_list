# Music_Player_using_linked_list
Web-based Music Player built in C++ using Linked Lists (Singly and Doubly) and the httplib web server, playable directly in a web browser.


# 🎵 Linked List Music Player (C++ Web Server)

A web-controlled music player built entirely in C++, showcasing Data Structures and Algorithms (DSA) principles through real-world implementation.
The project integrates Linked Lists to manage a Music Library and Playlist, served over a local web server for browser-based control.


## 🧠 Core Concept

This project demonstrates how traditional data structures can power modern, interactive applications.

* Music Library: Implemented using a Singly Linked List (SLL)
* Playlist: Managed with a Doubly Linked List (DLL) — supports Next and Previous song navigation
* Web Interface: Control playback, add/remove songs, and navigate the playlist from any web browser


## 🛠️ Technology Stack

| Component           | Technology / Concept                                  | Purpose                                                   |
| :------------------ | :---------------------------------------------------- | :-------------------------------------------------------- |
| Backend Core        | C++                                                   | Implements all the linked list logic and playback control |
| Data Structures     | Singly & Doubly Linked Lists                          | Core DSA implementation for song management               |
| Web Server          | [`httplib.h`](https://github.com/yhirose/cpp-httplib) | Header-only C++ HTTP server exposing REST API endpoints   |
| Frontend UI         | HTML, JavaScript, CSS                                 | Browser interface to control playback                     |
| Audio Playback      | Windows Multimedia API (`<windows.h>`, `winmm.lib`)   | Handles `.wav` audio playback on Windows                  |

---

## 📂 Project Structure

MusicPlayer_Shareable/
├── server.exe                    # Compiled executable
├── server.cpp                    # Web server implementation
├── music_player_linkedlist.cpp   # Core DSA and music logic
├── httplib.h                     # Header-only web server library
├── public/
│   └── index.html                # Web-based UI (Frontend)
└── song/
    ├── AalIzzWell.wav
    └── ... (Other .wav files)
    

## ⚙️ Setup & Installation (Windows)

### 1. Requirements

* C++ Compiler: MinGW-W64 (with `g++`)
* IDE: Visual Studio Code (or any C++ IDE)
* Audio Files: PCM-encoded `.wav` files placed inside the `song` folder

### 2. Compile the Project

Run this command in your terminal from the project root:

g++ server.cpp music_player_linkedlist.cpp -o server.exe -lws2_32 -lwinmm -pthread


This compiles the C++ backend and links:

* **`-lws2_32`** → Networking support
* **`-lwinmm`** → Multimedia (audio playback)
* **`-pthread`** → Threading for concurrent request handling


## ▶️ Run the Server

After compilation, start the server with:
./server.exe


You should see:
🎵 Music Player Server running at http://localhost:8080


## 🌐 Access the Player

Open your preferred browser and navigate to:

👉 [http://localhost:8080](http://localhost:8080)

From the web UI, you can:

* Add songs from your Library to your Playlist
* Play / Pause / Stop playback
* Navigate Next / Previous songs
* View currently playing track

---

## 🧩 DSA Behind the Scenes

| Feature                 | Data Structure     | Description                                       |
| ----------------------- | ------------------ | ------------------------------------------------- |
| Music Library           | Singly Linked List | Stores all available songs with O(n) traversal    |
| Playlist Management     | Doubly Linked List | Enables easy navigation (Next/Prev) between songs |
| Now Playing Pointer     | DLL Node Pointer   | Tracks current song node in playlist              |


## 🧱 Future Improvements

* 🔁 Shuffle / Repeat functionality
* ⏱️ Track progress bar in UI
* 📦 Support for MP3 via an audio decoding library
* 🌍 Cross-platform support (Linux/macOS)

## 💡 Learning Outcomes

* Applying Linked List data structures to real-world applications
* Understanding C++ server-side programming with `httplib`
* Integrating frontend and backend via REST APIs
* Managing multithreaded audio control and state management

## 🧑‍💻 Author

Developed by: Abhyuday, Himanshu


## 📜 License

This project is released under the **MIT License** 



