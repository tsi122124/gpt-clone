# ChatGPT Clone

A full-stack ChatGPT Clone built with React, Express, MySQL, and Google's Gemini AI API. The application allows users to submit programming-related questions, receive AI-generated responses, and store conversation history in a MySQL database.

## Project Overview

This project demonstrates the integration of a modern frontend application with a backend API, database persistence, and generative AI capabilities.

The chatbot is configured to focus exclusively on:

* Programming
* Software Engineering
* Computer Science
* Information Technology

Questions outside these topics are politely rejected and redirected toward technical subjects.

---

## Features

### Backend

* Express.js REST API
* MySQL database integration
* Conversation history storage
* Request validation
* Gemini AI integration
* System prompt enforcement for technical topics
* Error handling

### Frontend

* React-based chat interface
* Sidebar component
* Chat header component
* Message list display
* Chat input component
* Axios API communication
* Real-time response rendering
* Conversation history loading

---

## Tech Stack

### Frontend

* React
* Vite
* Axios
* CSS Modules

### Backend

* Node.js
* Express.js
* MySQL
* Google Gemini API

### Database

* MySQL

---

## Project Structure

```text
gpt-clone/
│
├── backend/
│   ├── db/
│   ├── src/
│   ├── index.js
│   ├── package.json
│   └── .env
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── vite.config.js
│
└── README.md
```

---

## Installation

### Clone Repository

```bash
git clone <repository-url>
cd gpt-clone
```

---

## Backend Setup

Navigate to the backend folder:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

Create a `.env` file:

```env
DB_HOST=localhost
DB_USER=your_username
DB_PASSWORD=your_password
DB_DATABASE=gpt_clone

GEMINI_API_KEY=your_api_key
GEMINI_MODEL=gemini-2.0-flash-lite
```

Start the server:

```bash
npm start
```

---

## Frontend Setup

Navigate to the frontend folder:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Run the development server:

```bash
npm run dev
```

---

## API Endpoints

### Get Conversation History

```http
GET /api/chat/conversations
```

Returns all stored chat messages.

---

### Create New Conversation

```http
POST /api/chat/conversations
```

Request Body:

```json
{
  "question": "What is a closure in JavaScript?"
}
```

Response:

```json
{
  "userConversation": {},
  "assistantConversation": {}
}
```

---

## Database Schema

### conversations

| Column      | Type      |
| ----------- | --------- |
| id          | INT       |
| role        | VARCHAR   |
| content     | TEXT      |
| token_count | INT       |
| created_at  | TIMESTAMP |

---

## System Prompt Behavior

The chatbot is configured to answer only:

* Programming
* Software Engineering
* Computer Science
* Information Technology

Non-technical questions are politely declined.

Example:

**User:**

```text
What should I eat for dinner?
```

**Assistant:**

```text
I am designed to answer questions related to programming, software engineering, computer science, and information technology.
```

---

## Learning Outcomes

Through this project I practiced:

* REST API development
* React frontend development
* Database integration with MySQL
* AI API integration
* State management
* Client-server communication
* Error handling
* Full-stack application architecture

---

## Author

Tsion Habtesilassei

Phase 4 - Week 2

Evangadi Bootcamp
