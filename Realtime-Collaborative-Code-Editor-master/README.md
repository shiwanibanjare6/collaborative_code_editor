# 🚀 Sync Code — Realtime Collaborative Code Editor

**Sync Code** is a real-time collaborative code editor that allows multiple developers to write, edit, and collaborate on code together from different devices and browser windows.

Instead of sharing code through messages or repeatedly sending files, users can join the same room and work on the same code in real time. Changes made by one user are instantly synchronized with everyone else in the room.

---

## ✨ Features

* 👥 **Real-Time Collaboration** — Multiple users can work on the same code simultaneously.
* ⚡ **Instant Code Synchronization** — Changes are reflected across connected users in real time.
* 🏠 **Room-Based Collaboration** — Create a room and share the room ID with other users.
* 📋 **One-Click Room ID Copy** — Easily copy the room ID to your clipboard.
* 🚪 **Join & Leave Rooms** — Users can join, leave, and rejoin collaborative sessions.
* 👤 **Live User Presence** — Joining and leaving of users is reflected in real time.
* 🎨 **Multiple Themes** — Choose an editor theme according to your preference.
* 💻 **Syntax Highlighting** — Supports syntax highlighting for multiple programming languages.
* 💾 **Persistent Preferences** — Selected language and theme can be stored in local storage.
* 🔐 **Room Join Control** — Room owners can accept or reject users attempting to join.
* 🔔 **Toast Notifications** — User actions and important events are communicated through notifications.

---

## 🛠️ Tech Stack

| Technology         | Purpose                               |
| ------------------ | ------------------------------------- |
| **React.js**       | Frontend user interface               |
| **Node.js**        | Backend runtime                       |
| **Express.js**     | Server-side application               |
| **Socket.io**      | Real-time bidirectional communication |
| **CodeMirror**     | Code editor and syntax highlighting   |
| **React-Toastify** | Notifications and user feedback       |
| **Docker**         | Application containerization          |
| **PM2**            | Node.js process management            |

---

## 🏗️ How It Works

The application follows a client-server architecture with **Socket.io** handling real-time communication.

```text
             ┌──────────────────┐
             │     User A       │
             │  Code Editor     │
             └────────┬─────────┘
                      │
                      │ WebSocket
                      ▼
             ┌──────────────────┐
             │   Node.js +      │
             │   Socket.io      │
             │     Server       │
             └────────┬─────────┘
                      │
                      │ WebSocket
                      ▼
             ┌──────────────────┐
             │     User B       │
             │  Code Editor     │
             └──────────────────┘
```

When a user edits the code:

1. The editor detects the change.
2. The client sends the update through **Socket.io**.
3. The server receives the change.
4. The server broadcasts the update to other users in the same room.
5. Connected clients update their editors in real time.

This allows multiple users to collaborate without manually refreshing or sharing updated files.

---

## 🐳 Running with Docker

### Prerequisites

Make sure you have:

* Docker
* Docker Compose

### Using the Docker Image

Pull the pre-built Docker image:

```bash
docker pull mohitur/code-editor
```

Run the container:

```bash
docker run -p 8000:8000 -p 3000:3000 -p 5000:5000 mohitur/code-editor
```

Open the application:

```text
http://localhost:3000
```

### Create a Collaborative Room

1. Click **Create New Room**.
2. Enter your username.
3. Create the room.
4. Copy the generated **Room ID**.
5. Open the application in another browser window or incognito tab.
6. Enter the same Room ID.
7. Start collaborating in real time.

You can open the same room in multiple browser windows to test multi-user collaboration.

---

## 🐳 Build the Docker Image Yourself

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository.git
```

Navigate into the project:

```bash
cd your-repository
```

Configure the required environment variables in the Docker configuration.

Then start the application:

```bash
docker-compose up -d
```

Open:

```text
http://localhost:3000
```

---

## 💻 Running Locally

### Prerequisites

Recommended versions:

* **Node.js:** v20.11.1
* **npm:** v10.2.4
* **PM2:** v5.3.1

Install PM2 globally:

```bash
npm install -g pm2
```

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the root directory.

Copy the required values from the provided example environment file and add the necessary credentials/configuration.

### 4. Start the React Client

```bash
npm start
```

### 5. Start the Server

In another terminal:

```bash
npm run server:dev
```

Alternatively, use PM2:

```bash
pm2 start server.js
```

### 6. Open the Application

Visit:

```text
http://localhost:3000
```

You can now create a room and invite other users using the generated Room ID.

### Stop the Server

If running normally:

```bash
Ctrl + C
```

If using PM2:

```bash
pm2 stop server.js
```

---

## 🧪 Testing Real-Time Collaboration

To test the collaborative functionality:

1. Open the application in Browser Window 1.
2. Create a new room.
3. Copy the Room ID.
4. Open Browser Window 2 or an Incognito window.
5. Join using the same Room ID.
6. Start typing code in either editor.
7. Verify that changes appear in the other editor instantly.
8. Open additional browser windows to test multiple users.

---

## 📂 Project Structure

A typical structure of the application looks like:

```text
Sync-Code/
│
├── client/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── ...
│   └── package.json
│
├── server/
│   └── ...
│
├── public/
│
├── Dockerfile
├── docker-compose.yml
├── server.js
├── package.json
├── .env
└── README.md
```

> The exact structure may vary depending on the implementation and project configuration.

---

## 🔮 Future Scope

Some potential improvements for Sync Code include:

* [x] Multi-language syntax highlighting
* [x] Multiple editor themes
* [x] Save language and theme preferences in local storage
* [x] Accept/reject users joining a room
* [ ] Integrated video and voice communication
* [ ] Local code file upload
* [ ] Code execution directly inside the editor
* [ ] User authentication and profiles
* [ ] Persistent cloud-based code storage
* [ ] Collaborative cursor and selection indicators
* [ ] Version history and code restoration
* [ ] Integrated chat for collaborators
* [ ] AI-powered code completion and debugging

---

## 🎯 Why Sync Code?

Traditional collaboration often involves repeatedly sharing code through messaging applications, manually merging changes, or sending updated files.

Sync Code provides a simpler workflow:

```text
Create Room
     ↓
Share Room ID
     ↓
Multiple Users Join
     ↓
Edit Code Together
     ↓
Changes Synchronize Instantly
     ↓
Collaborate & Ship Faster 🚀
```

The project demonstrates practical implementation of **real-time communication, WebSockets, client-server architecture, collaborative editing, and modern web development**.

---

## 👩‍💻 About the Developer

Hi, I'm **Shiwani Banjare**, a B.Tech student specializing in **Data Science and Artificial Intelligence at IIIT Naya Raipur**.

I'm interested in building software applications, AI-powered systems, and developer-focused tools while continuously improving my problem-solving and full-stack development skills.

### Connect with Me

* 💼 **LinkedIn:** [Shiwani Banjare](https://www.linkedin.com/)
* 🐙 **GitHub:** [Shiwani Banjare](https://github.com/shiwanibanjare6)
* 💻 **LeetCode:** [sims67](https://leetcode.com/)

---

## ⭐ Contributing

Contributions, improvements, and bug fixes are welcome!

### Fork the Repository

```bash
git clone https://github.com/your-username/your-repository.git
```

### Create a Branch

```bash
git checkout -b feature/your-feature-name
```

### Make Your Changes

Implement your feature or fix the issue.

### Commit Your Changes

```bash
git add .
git commit -m "Add your feature"
```

### Push Your Branch

```bash
git push origin feature/your-feature-name
```

Then open a **Pull Request** on GitHub.

---

## 📄 License

This project is intended for learning, experimentation, and collaborative development.

---

## ⭐ Show Your Support

If you find **Sync Code** useful or interesting, consider giving the repository a ⭐ on GitHub!

**Built with ❤️ by Shiwani Banjare**
