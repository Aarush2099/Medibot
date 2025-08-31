# Medibot

Medibot is an integrated web application that provides AI-assisted medical advice and support. By leveraging state-of-the-art generative AI and a user-friendly interface, Medibot helps users ask medical queries, access assistance, upload and view reports, and manage appointments. The project consists of a Flask-based backend and a React-based frontend that work together seamlessly.

--------------------------------------------------

## Introduction

Medibot is designed to deliver medical support through an intelligent chatbot and a suite of interactive web pages. Built with Flask for the backend and React for the frontend, the application supports tasks such as chatting with a health assistant powered by Google Generative AI, file uploads for medical reports, and navigation through help and registration pages. The project aims to simplify access to medical help and provide a platform for both users seeking medical guidance and healthcare professionals looking to provide assistance.

--------------------------------------------------

## Features

- **Intelligent Chatbot:**  
  Users can interact with a chatbot that is specially designed for medical queries. The chatbot uses the Google Generative AI model (Gemini 1.0-pro) to generate medically relevant answers.

- **User Authentication and Navigation:**  
  Includes separate routes/pages for login, registration, and dashboards. The frontend leverages React Router to navigate between pages for a seamless user experience.

- **File Upload and Report Management:**  
  Users can upload images of their medical reports. The backend stores these files under a designated directory and displays them for download through a responsive interface.

- **Voice and Speech Recognition:**  
  In the chatbot page, users can utilize built-in speech recognition for easier query input and receive audible responses, thanks to integrated web APIs.

- **Dynamic Data Visualization:**  
  Health statistics are presented using charts such as line and bar graphs. This feature provides users with a visual representation of their progress, including parameters like blood pressure and sugar levels.

- **Responsive Design:**  
  The front-end interface is designed to be mobile-friendly and utilizes modern CSS frameworks along with custom styles for an intuitive user experience.

--------------------------------------------------

## Requirements

### Backend
- **Programming Language:** Python  
- **Framework:** Flask  
- **Dependencies:**  
  The backend requirements are listed in the `backend/requirements.txt` file and include packages such as:
  - Flask
  - Werkzeug
  - Google Generative AI library (configured in `backend/bot.py`)
  - Additional dependencies for image handling and file upload security

### Frontend
- **Programming Language:** JavaScript (ES6+)  
- **Framework:** React  
- **Tools:**  
  - React Router for page navigation
  - Axios for handling HTTP requests  
  - Chart.js and react-chartjs-2 for displaying graphs and statistics  
  - Package dependencies are maintained in the `fronten/package.json` file

--------------------------------------------------

## License

Medibot is released under the **MIT License**. This license allows for reuse, modification, and distribution of the project with proper attribution.

--------------------------------------------------

## Contributing

Contributions are welcome. If you would like to contribute to Medibot, please follow these guidelines:

- **Fork the Repository:**  
  Create a personal fork of the project and clone it locally.

- **Create a Feature Branch:**  
  Use descriptive names for your feature branches.

- **Code Standards:**  
  Follow the existing coding style and maintain consistency with formatting and documentation.

- **Testing:**  
  Make sure to run and update any tests where applicable. The frontend includes tests set up via React Testing Library.

- **Submit a Pull Request:**  
  Once your changes are ready, submit a pull request with a clear description of the changes and fix any conflicts with the main branch.

--------------------------------------------------

## Configuration

Before running the application, the following configuration steps are required:

- **Backend Configuration:**  
  - Set the secret key in the Flask application (see `backend/app.py`).
  - In `backend/bot.py`, configure your Google Generative AI API key in the designated section.
  - Define the upload folder path for saving user reports and ensure the directory exists.

- **Frontend Configuration:**  
  - Ensure that the required dependencies are installed using npm or yarn as specified in the `fronten/package.json` file.
  - Configure the React Router paths to match the backend routes if deploying on a single domain.
  - Update any API endpoints if you change the default backend URL (e.g., from `http://localhost:5000`).

--------------------------------------------------

## Usage

### Running the Backend
1. Navigate to the `backend` directory.
2. Install the required Python packages:
   ```
   pip install -r requirements.txt
   ```
3. Configure your Google Generative AI API key in `backend/bot.py`.
4. Start the Flask server:
   ```
   python app.py
   ```
   The server will run on the default port (e.g., http://localhost:5000).

### Running the Frontend
1. Navigate to the `fronten` directory.
2. Install the Node dependencies:
   ```
   npm install
   ```
3. Start the React development server:
   ```
   npm start
   ```
   The application will run on the default port (e.g., http://localhost:3000).

### Navigating the Application
- **Home/Landing Page:**  
  The landing page showcases a welcoming interface with quick links to login, register, or interact with the chatbot.
  
- **User Authentication:**  
  Routes like `/login` and `/register` redirect users to dedicated pages for login and registration.

- **Chatbot Interaction:**  
  The `/ChatbotPage` route lets users ask medical queries. The chatbot uses either text or voice (via the integrated speech recognition) to handle user input and provide informed responses.

- **File Upload:**  
  The `/upload` route provides an interface for users to upload images of their health reports. Submitted files are stored and then displayed on the `/show` page for viewing or downloading.

- **Help and Assistance:**  
  Users can navigate to `/GetHelp` or `/ProvideHelp` to either get or offer help related to medical queries or appointments.

--------------------------------------------------

Medibot offers a comprehensive platform for accessing medical guidance and support through advanced AI technology, all within a responsive web interface. Contributions and improvements to this project are always welcome.
