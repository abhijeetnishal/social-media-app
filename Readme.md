# Social Media Application

This project aims to recreate the core functionality of the popular social media platform Twitter(now X.com). Users can register, log in, post tweets, follow other users, and interact with their timeline. This repository contains the codebase and configurations for both the frontend and backend of the Twitter Clone project.
<br>

## Table of Contents

- [**Features**](#features)
- [**Technologies**](#technologies)
- [**Future Enhancement**](#usage)
- [**Running the Application using docker**](#running-the-application-using-docker)
- [**Project Installation**](#project-installation)
- [**Usage**](#usage)
  <br>

## Features

- **_User Registration, Login, and Logout_**: Users can create accounts, log in using their credentials, and log out when they're done.
- **_Tweet Management_**: Authenticated users can post new tweets, schedule tweets, edit their existing tweets, and delete their own tweets.
- **_Timeline_**: The home page displays a chronological timeline of tweets from users the authenticated user is following, as well as their own tweets.
- **_Profile Page_**: Users have their own profile page where they can view their followers and the users they are following.
- **_Error handling and validation_**
- **_Caching with Redis_**

<br>

## Technologies

The project utilizes the following technologies:

- **Backend**:
  - **_Node.js_**: The backend of the application is built using Node.js, providing a fast and scalable runtime environment.
  - **_Express.js_**: A web application framework for Node.js for rapid development.
  - **_MongoDB_**: MongoDB serves as the database for storing user data, tweets, and other relevant information.
  - **_TypeScript_**: TypeScript is used throughout the project to ensure strong type safety and enhance the development process.
  - **_Redis_**: Redis is utilized for caching purposes, improving the overall performance of the application by reducing database queries.
    <br>
- **Frontend**:
  - **_Next.js_**: A React framework for building server-side rendered and statically generated web applications.
  - **_TypeScript_**: TypeScript is used throughout the project to ensure strong type safety and enhance the development process.
  - **_Tailwind CSS_**: Tailwind CSS is used for styling the frontend, offering a utility-first approach and speeding up the design process.
  - **_Zustand_**: Zustand is a state management library for React, providing a simple and efficient way to manage application state.

<br>

## Running the Application using docker

1. Clone the repository:

```bash
   git clone https://github.com/abhijeetnishal/social-media-app.git
```

2. Move to server directory using below command:

```bash
    cd server
```

3. Create a .env file in root directory of server and copy contents of .env.example file to .env file and add MongoDB URI to setup database.
4. Make sure that docker is installed in your system. Run the below command to build docker image for server:

```bash
    docker build -t your_server_image_name .
```

5. Run a container based on your_server_image_name using below command, exposing port 8080 on the host machine and mapping it to port 8080 inside the container

```bash
    docker run -p 8080:8080 your_server_image_name
```

6. Now move to client directory using below command:

```bash
    cd ../client
```

7. Create a .env file in root directory of client and copy contents of .env.example file to .env file and add your backend URL.
8. Run the below command to build docker image for client:

```bash
    docker build -t your_client_image_name .
```

9. Run a container based on your_client_image_name using below command:

```bash
    docker run -p 3000:3000 your_client_image_name
```

## Project Installation

- To install the application locally, follow these steps:

1. Clone the repository to your local machine using:

```bash
    git clone https://github.com/abhijeetnishal/social-media-app.git
```

2. Move to server directory:

```bash
    cd server
```

3. To install dependencies run the below command:

```bash
    npm install
```

4. Create a .env file in root directory of server and copy contents of .env.example file to .env file and add your secret keys.
5. Start the server using command:

```bash
    npm start
```

6. Now move to client folder:

```bash
    cd ../client
```

7. Create a .env file in root directory of client and copy contents of .env.example file to .env file and add your running backend URL.
8. To install dependencies run the below command:

```bash
    npm install
```

9. start the next.js app using command:

```bash
    npm run dev
```

<br>

## Usage

- To use the application, follow these steps:
  1. Register a new account with your username and password.
  2. Log in to the application using username and password.
  3. In Home page create, schedule, edit or delete post for our own and and see posts of following users.
  4. In profile page, you can see followers and following list in chronological manner.
     <br>
