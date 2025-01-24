# Multi-Page HTML Application

This project is a basic HTML-based multi-page application that demonstrates:
1. A **Login Page** with basic password validation.
2. A **User Information Page** displaying static user details.
3. A **Personal Profile Page** with user-specific content and a logout feature.

---

## Features

### 1. **Login Page**
   - Accepts a username and password.
   - Basic validation:
     - Password must be at least 6 characters long.
     - Default credentials:
       - **Username**: `user`
       - **Password**: `password123`
   - Displays error messages for invalid credentials.

### 2. **User Information Page**
   - Displays static user details (name and email).
   - Includes a "Go to Profile" button to navigate to the profile page.

### 3. **Personal Profile Page**
   - Displays a personalized message.
   - Includes a "Logout" button to return to the login page.

---

## How to Run the Project

### 1. **Direct Method**
   - Save the project file as `index.html`.
   - Open the file in any web browser (e.g., Chrome, Firefox, Edge).
   - Interact with the pages as per the flow:
     1. Login with the username and password.
     2. Navigate through the pages.

### 2. **Optional: Run on a Local Server**
   - Install [Node.js](https://nodejs.org/) (if not already installed).
   - Use a static server to host the project:
     - Open a terminal and navigate to the folder containing the `index.html`.
     - Run:
       ```bash
       npx serve
       ```
     - Open the provided URL (e.g., `http://localhost:5000`) in your browser.

---

## Project Structure
This project consists of a single HTML file with inline CSS and JavaScript:


