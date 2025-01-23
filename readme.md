# Eduverse: AI-Powered Learning Roadmap Generator

# <p align="center"> <img src="splash.png" height="300" width = "300"></p>

## Table of Contents

1. [Introduction](#introduction)
2. [Problem Statement](#problem-statement)
3. [Features](#features)
4. [How It Works](#how-it-works)
5. [Technology Stack](#technology-stack)
6. [Installation](#installation)
7. [Usage](#usage)
8. [Contributing](#contributing)
9. [License](#license)
10. [Acknowledgments](#acknowledgments)

## Introduction

Eduverse is an innovative desktop application designed to help users create, manage, and share personalized learning roadmaps for any skill they wish to acquire. Whether you're learning to code, play an instrument, or master a new language, Eduverse simplifies the process by providing structured roadmaps, resource management, and social sharing capabilities. Built with generative AI at its core, Eduverse empowers users to learn smarter, not harder.

## Problem Statement

Learning a new skill can be overwhelming. Many learners struggle with:

- **Lack of Structure**: Not knowing where to start or how to progress.
- **Resource Overload**: Overwhelming amount of resources present all over the internet. Difficulty in organizing and managing learning materials.
- **Motivation**: Losing track of progress and feeling demotivated.
- **Collaboration**: Limited ability to share resources or follow others' learning paths.

Eduverse addresses these challenges by providing a centralized platform where users can create structured roadmaps, attach resources, track progress, and collaborate with others all powered by generative AI to make the process seamless and intuitive.

## Features

### 1. **Create Custom Roadmaps**

- Users can create detailed roadmaps for any skill, breaking it down into modules and topics.
- Example: A roadmap for learning Python could include modules like "Basics," "Data Structures," and "Web Development," with topics like "Variables," "Lists," and "Flask Framework."

### 2. **Edit and Update Roadmaps**

- Users can easily modify and update the contents of their roadmaps to reflect their learning progress.
- Example: Add a new topic, reorder modules, or mark a topic as completed.

### 3. **Resource Management**

- Attach resources (PDFs, videos, links) to specific modules or topics.
- Example: Attach a YouTube tutorial to the "Flask Framework" topic or a PDF eBook to the "Data Structures" module.

### 4. **Automatic Google Drive Integration**

- Users can share resources, they are automatically uploaded to Google Drive, and sharable links are stored in the database.
- Example: Share a resource with a friend by generating a Google Drive link.

### 5. **Social Sharing**

- Share your roadmaps and resources with others or follow roadmaps created by other users.
- Example: Follow a roadmap created by an expert in machine learning or share your own roadmap for learning guitar.

### 6. **Progress Tracking**

- Track your learning progress and stay motivated.
- Example: Mark topics as "In Progress" or "Completed" and visualize your progress with a progress bar.

### 7. **Internet Resource Recommendations**

- Eduverse can fetch and recommend relevant links from the internet for the user's convenience by scraping the Bing search engine.
- Example: If a user creates a roadmap for "Machine Learning," Eduverse can recommend top-rated courses, tutorials, and articles from the web.

## How It Works

### 1. **Generative AI for Roadmap Creation**

- Eduverse uses OpenAI's GPT to suggest modules and topics based on the skill the user wants to learn.
- Example: If a user wants to learn "Digital Marketing," the AI generates a roadmap with modules like "SEO," "Content Marketing," and "Social Media Advertising and their relevant topics all in the format of the course object."

### 2. **Resource Upload and Sharing**

- When a user clicks on share resource, the app will request the permissions to access the user's google drive and upon agreeing, it authenticates and fetches the access and refresh token( which are stored on users device for future use).
- Once tokens are fetched, the resource file is uploaded to Google Drive via the Google Drive API.
- A sharable link is generated and stored in the database for easy access.

### 3. **Progress Tracking**

- Users can mark topics as "Not Started","In Progress" or "Completed," and the app updates the progress bar in real-time.

### 4. **Social Collaboration**

- Users can browse shared roadmaps, follow them, and access the attached resources.
- Example: A user can follow a roadmap for "Web Development" and access all the resources shared by the creator.

### 5. **Internet Resource Recommendations**

- Eduverse uses web scraping to fetch relevant links from Bing based on the course or skill name.
- Example: For a roadmap on "Data Science," Eduverse can recommend links to freeCodeCamp tutorials, Coursera courses, and Medium articles.

## Technology Stack

![Electron] ![HTML] ![CSS] ![React.js] ![Express.js] ![MongoDB] ![Mongoose ODM] ![git] ![ChatGPT] ![SpringBoot]

### Frontend

- **Electron + React**: For building a cross-platform desktop application with a responsive and intuitive user interface.

### Backend

- **Express + Mongoose**: For handling API requests, database operations, and business logic.

### Database

- **MongoDB Atlas**: For storing user data, roadmaps, resources, and progress tracking information.

<!-- ### Authentication

- **Google OAuth**: For secure user authentication and Google Drive integration. -->

### File Storage

- **Google Drive API**: For uploading resources and generating sharable links.

### Generative AI

- **OpenAI GPT**: For generating roadmap suggestions and content.

### Web Scraping

- **Pupeteer**: For scraping and fetching relevant links from the internet.

## Usage

### 1. **Creating a Roadmap**

- Open the Eduverse app.
- Click on "Create New Roadmap."
- Enter the skill name, description, and add modules/topics.
- Attach resources to specific topics if needed.
- Save the roadmap.

### 2. **Editing a Roadmap**

- Select the roadmap you want to edit.
- Modify the modules, topics, or resources as needed.
- Save your changes.

### 3. **Sharing Resources**

- Attach a resource to a topic.
- Click on "Share Resource."
- The resource will be uploaded to Google Drive, and a sharable link will be generated and stored.

### 4. **Following a Roadmap**

- Browse shared roadmaps.
- Click on "Follow" to add the roadmap to your list.
- Track your progress and access shared resources.

### 5. **Fetching Internet Recommendations**

- While creating or editing a roadmap, click on "Fetch Recommendations."
- Eduverse will scrape Bing for relevant links and display them for you to add to your roadmap.

Watch this video for a working demo.

<video src = "./usage.mp4" controls width="75%"></video>

## Installation

To run the code on your local machine (for developers or contributors)

### Prerequisites

- Node.js and npm installed
- MongoDB Atlas account
- Google Cloud Platform account with Google Drive API enabled
- OpenAI api key

### Steps

1. **Clone the Repository**

   ```bash
   git clone https://github.com/Mohit-Harsh/StudentPortal.git
   cd "Electron App"

   ```

2. **Install Dependencies**

   ```bash
   # Install electron app's dependencies
   npm install
   ```

3. **Set Up Environment Variables**

   Create a `.env` file in the root directory with the following variables:

   ```env
   MONGO_URI=your_mongodb_atlas_connection_string
   GOOGLE_CLIENT_ID=your_google_client_id
   GOOGLE_CLIENT_SECRET=your_google_client_secret
   OPENAI_API_KEY=your_openai_api_key
   ```

4. **Run the Application**

   ```bash
   # Start the Electron app
   npm run start
   ```

## Contributing

We welcome contributions from the community! If you'd like to contribute to Eduverse, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Push your branch to your fork.
5. Submit a pull request with a detailed description of your changes.

## License

Eduverse is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Thank you for checking out Eduverse! We hope this tool helps you on your learning journey 🚀

[Electron]: https://img.shields.io/badge/Electron-20232A?style=for-the-badge&logo=electron&logoColor=61DAFB
[HTML]: https://img.shields.io/badge/HTML-grey?style=for-the-badge&logo=html5
[CSS]: https://img.shields.io/badge/CSS-blue?style=for-the-badge&logo=css3
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[Express.js]: https://img.shields.io/badge/Express.js-yellowgreen?style=for-the-badge&logo=express
[git]: https://img.shields.io/badge/Git-262626?style=for-the-badge&logo=git
[MongoDB]: https://img.shields.io/badge/MongoDB-green?style=for-the-badge&logo=mongodb
[Mongoose ODM]: https://img.shields.io/badge/Mongoose-red?style=for-the-badge&logo=mongoose
[ChatGPT]: https://img.shields.io/badge/ChatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white
[SpringBoot]: https://img.shields.io/badge/SpringBoot-black?style=for-the-badge&logo=springboot&logoColor=green
