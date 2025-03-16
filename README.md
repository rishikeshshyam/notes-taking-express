# Notes Tonight

**Notes Tonight** is a simple note-taking web application built with Node.js, Express, MongoDB, and EJS. It allows users to create, view, and delete notes with a simple and intuitive user interface.

---

## Table of Contents

1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Setup Instructions](#setup-instructions)
4. [Running the Application](#running-the-application)
5. [Folder Structure](#folder-structure)
6. [Contributing](#contributing)
7. [License](#license)

---

## Features

- **Create Notes**: Allows users to create new notes with a title and description.
- **View Notes**: Displays a list of notes with titles, descriptions, and creation dates.
- **Delete Notes**: Users can delete notes from the list.
- **Responsive Design**: The application is fully responsive and mobile-friendly.

---

## Technologies Used

- **Node.js**: JavaScript runtime for building the server.
- **Express.js**: Web framework for Node.js used to build the routes and handle HTTP requests.
- **MongoDB**: NoSQL database used to store notes.
- **Mongoose**: ODM (Object Data Modeling) library for MongoDB to interact with the database.
- **EJS**: Templating engine for rendering dynamic HTML pages on the server.
- **Bootstrap**: CSS framework for responsive design and UI components.
- **Method-Override**: Middleware used to support HTTP verbs like DELETE in HTML forms.

---

## Setup Instructions

Follow these steps to set up the project on your local machine:

### 1. **Clone the repository**
   
   First, clone the repository to your local machine using the following command:

   ```bash
   git clone https://github.com/yourusername/notes-tonight.git
   ```

   Replace `yourusername` with your actual GitHub username.

### 2. **Install Dependencies**

   Navigate into the project folder and run `npm install` to install the required dependencies:

   ```bash
   cd notes-tonight
   npm install
   ```

### 3. **Set Up MongoDB**

   This project uses MongoDB for data storage. You can either:

   - Set up a local MongoDB server: [MongoDB Setup](https://www.mongodb.com/docs/manual/installation/)
   - Or use MongoDB Atlas for a cloud-based database: [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)

   Once you have your MongoDB instance set up, make sure to create a `.env` file in the root directory of the project with the following contents:

   ```
   SERVER=mongodb://localhost:27017/notes-tonight   # MongoDB URI for local setup
   PORT=3000                                        # Port number (optional, default is 3000)
   ```

   Replace the `SERVER` value with your actual MongoDB URI if using a cloud instance like MongoDB Atlas.

### 4. **Create the `.env` File**

   The `.env` file is used to store environment variables such as your MongoDB connection string. Create a `.env` file in the root directory of your project:

   ```bash
   touch .env
   ```

   Inside the `.env` file, add the following:

   ```
   SERVER=mongodb://localhost:27017/notes-tonight  # Local MongoDB URI
   PORT=3000                                       # Server port
   ```

   This file ensures that sensitive information (like your MongoDB URI) is kept safe.

---

## Running the Application

To run the application locally, follow these steps:

### 1. **Start the Application**

   Run the following command to start the server:

   ```bash
   npm start
   ```

   This will start the server on the port specified in your `.env` file (default is `3000`).

### 2. **Access the Application**

   Open your web browser and go to the following URL to access the application:

   ```
   http://localhost:3000
   ```

   You should now be able to create, view, and delete notes.

---

## Folder Structure

Here's an overview of the folder structure of the project:

```
notes-tonight/
├── models/                # Contains Mongoose models (e.g., 'note.js')
│   └── note.js            # Schema definition for Note
├── routes/                # Contains route files for the app
│   └── notes.js           # CRUD routes for handling notes
├── views/                 # EJS template files
│   ├── index.ejs          # The main page to view notes
│   ├── new.ejs            # The form to create new notes
├── .env                   # Environment variables for MongoDB connection
├── app.js                 # Main application file (Express server setup)
├── package.json           # Project dependencies and configuration
└── README.md              # Project documentation (this file)
```

### Key Files:
- **`app.js`**: The entry point of the application, where the Express server is set up.
- **`models/note.js`**: The Mongoose model for the Note data structure.
- **`routes/notes.js`**: Contains routes for creating, viewing, and deleting notes.
- **`views/`**: Contains the EJS template files for rendering HTML views.

---

## Contributing

We welcome contributions to the project! If you'd like to contribute, follow these steps:

1. Fork the repository.
2. Clone your fork to your local machine.
3. Create a new branch for your feature or fix.
4. Make your changes.
5. Commit your changes with a meaningful commit message.
6. Push your changes to your forked repository.
7. Create a pull request to merge your changes.
8. 

