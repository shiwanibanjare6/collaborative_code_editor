# Sync Code

A real-time collaborative code editor that allows multiple users to write and edit code together in the same room.

Users can create a room, share the room ID with others, and collaborate on code in real time. Changes made by one user are instantly reflected for everyone connected to the room.

## Features

* Real-time collaborative code editing
* Multiple users can join the same room
* Changes are synchronized instantly
* Create and join rooms using a Room ID
* Copy Room ID with one click
* Users can leave and rejoin rooms
* Real-time user join and leave updates
* Syntax highlighting for multiple programming languages
* Multiple editor themes
* Saves selected language and theme preferences
* Accept or reject users joining a room

## Tech Stack

* React.js
* Node.js
* Express.js
* Socket.io
* CodeMirror
* React-Toastify
* Docker
* PM2

## How It Works

Sync Code uses **Socket.io** for real-time communication between users.

When a user makes changes in the editor, the changes are sent to the server through a WebSocket connection. The server then broadcasts those changes to other users in the same room.

```text
User 1
   │
   │ Code Changes
   ▼
Socket.io Server
   │
   │ Broadcast
   ▼
User 2 ─── User 3
```

This allows everyone in the same room to work on the code simultaneously.

## Running with Docker

### Prerequisites

* Docker
* Docker Compose

### Using the Docker Image

Pull the Docker image:

```bash
docker pull mohitur/code-editor
```

Run the container:

```bash
docker run -p 8000:8000 -p 3000:3000 -p 5000:5000 mohitur/code-editor
```

Open the application at:

```text
http://localhost:3000
```

### Create a Room

1. Click **Create New Room**.
2. Enter your username.
3. Create the room.
4. Copy the Room ID.
5. Open the application in another browser window or incognito tab.
6. Enter the same Room ID.
7. Start collaborating.

## Running Locally

### Prerequisites

* Node.js v20.11.1
* npm v10.2.4
* PM2 v5.3.1 (optional)

Install PM2 if required:

```bash
npm install -g pm2
```

### Installation

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

Install dependencies:

```bash
npm install
```

Create a `.env` file in the root directory and add the required environment variables.

### Start the Client

```bash
npm start
```

### Start the Server

Open another terminal and run:

```bash
npm run server:dev
```

Or using PM2:

```bash
pm2 start server.js
```

The application will be available at:

```text
http://localhost:3000
```

## Testing Collaboration

To test the application:

1. Open the application in your browser.
2. Create a new room.
3. Copy the Room ID.
4. Open another browser window or incognito tab.
5. Join using the same Room ID.
6. Start editing the code.
7. Changes should appear in both windows in real time.

You can open multiple browser windows to test collaboration between several users.

## Future Improvements

* [ ] Voice and video chat
* [ ] Upload local code files
* [ ] Code execution
* [ ] User authentication
* [ ] Persistent code storage
* [ ] Collaborative cursor indicators
* [ ] Version history
* [ ] In-room chat

## About

Hi, I'm **Shiwani Banjare**, a B.Tech student in **Data Science and Artificial Intelligence at IIIT Naya Raipur**.

I enjoy building web applications and working with different technologies to create practical and useful projects.

### Connect

* **GitHub:** [Shiwani Banjare](https://github.com/shiwanibanjare6)
* **LinkedIn:** [Shiwani Banjare](https://www.linkedin.com/)

## Contributing

Contributions and suggestions are welcome.

1. Fork the repository.
2. Clone your fork.
3. Create a new branch.
4. Make your changes.
5. Commit and push your changes.
6. Create a Pull Request.

## License

This project is open for learning and development purposes.

---

**Built by Shiwani Banjare**
