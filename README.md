# Sync Code

**Sync Code** is a real-time collaborative code editor that allows multiple users to edit code together in the same room.

Users can create a room, share the room ID, and work on the same code editor. Changes made by one user are synchronized with other users in the room using Socket.io.

## Features

* Real-time collaborative code editing
* Create and join rooms using a Room ID
* Multiple users can edit code together
* Syntax highlighting
* Different editor themes
* Copy Room ID
* Leave a room

## Tech Stack

* React.js
* Node.js
* Express.js
* Socket.io
* CodeMirror
* React-Toastify

## How It Works

The frontend is built using React.js and CodeMirror.

Socket.io is used to establish real-time communication between the client and server. When a user changes the code, the change is sent to the server and then shared with other users in the same room.

```text
User 1
   |
   | Code Changes
   ↓
Socket.io Server
   |
   | Sends Changes
   ↓
User 2
```

This allows users in the same room to see code changes in real time.

## Running Locally

### Requirements

* Node.js
* npm

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

Create a `.env` file and add the required environment variables.

Start the frontend:

```bash
npm start
```

Start the server in another terminal:

```bash
npm run server:dev
```

Open:

```text
http://localhost:3000
```

## How to Use

1. Create a new room.
2. Enter your username.
3. Copy the Room ID.
4. Open the application in another browser window.
5. Join using the same Room ID.
6. Start editing the code together.

## Future Improvements

* Voice and video chat
* Code execution
* File upload
* User authentication

## About

Built by **Shiwani Banjare**, a B.Tech student in Data Science and Artificial Intelligence at **IIIT Naya Raipur**.

**GitHub:** https://github.com/shiwanibanjare6

**LinkedIn:** https://www.linkedin.com/

---

**Built with React.js, Node.js and Socket.io ❤️**
