# MAKE-API-OF-PROJECT

This problem statement is focused on building a **full-stack website** that combines both frontend and backend development using any technology of your choice, such as **React**, plain **HTML**, **CSS**, and **JavaScript**. It allows for creative flexibility while incorporating core concepts of web development, including user registration, authentication, and role-based access control. Below is a breakdown of the key features and instructions:

### Core Features:

#### **Navigation Bar**
- The website will have a **navbar** visible on all pages.
- The navbar should include links to the following pages:
  - **Home Page**: The main landing page with a welcome note.
  - **About Page**: Describes the project and its features.
  - **Sign Up Page**: For user registration.
  - **Login Page**: For user authentication.
  
- Once a user logs in, their **username** should appear on the navbar, and a **logout** button should be displayed, allowing them to log out.

#### **Home Page**
- This is the main page of the website and can be creative, including:
  - A **welcome note**.
  - Use of **images**, **GIFs**, or other visual elements to make it engaging.

#### **About Page**
- The **About Page** will provide a detailed explanation of the project:
  - Information about all the pages and their purposes.
  - A list of the technologies and **packages** used in the project.
  - You can include **screenshots** of your project to showcase its features.

#### **Sign Up Page**
- The **registration form** will have fields for user information:
  - **Username**: A unique identifier for the user.
  - **Email**: The user's email address.
  - **Date of Birth**: A field for entering the date of birth.
  - **Role**: A dropdown menu allowing the user to select their role (either **Admin** or **Explorer**).
  - **Location**: A field for the user’s location.
  - **Password** and **Confirm Password**: The user must enter the same password in both fields to successfully register.
  
- Once registered, the **user details** (username, email, etc.) will be stored in a **MongoDB database**.

#### **Login Page**
- The login form will have:
  - **Username**: The user's unique identifier.
  - **Password**: The user's password.
  
- Upon successful login:
  - The user is redirected to the **Home Page**.
  - The username is displayed on the **navbar** on all pages.
  
- The authentication process will be handled by a **middleware** to ensure secure login.
  
- A **logout button** will be displayed on the navbar, allowing users to log out and remove the username from the navbar.

### **Backend (Node.js, Express, MongoDB)**
1. **Routes**:
   - `POST`: Used to register new users during the sign-up process.
   - `GET`: To retrieve all user details (e.g., for admin review).
   - `GET`: To retrieve details of a specific user.
   - `PATCH/PUT`: Allows updating of user details (only **admins** can perform this action).
   - `DELETE`: Allows deletion of a user’s details (only **admins** can perform this action).

2. **Middlewares**:
   - **Authenticator**: This middleware ensures that only authenticated users are allowed to log in.
   - **Validator**: Checks the user’s role (Admin or Explorer) to determine if they have the appropriate permissions for certain actions, like updating or deleting user details.
   - **UserLogger**: Logs the **username** and **role** of the user in a `log.txt` file upon successful login for tracking purposes.

### **Database (MongoDB)**
- The project uses **MongoDB** to store user details such as:
  - **Username**
  - **Email**
  - **Date of Birth**
  - **Role** (Admin or Explorer)
  - **Location**
  - **Password** (which will be hashed for security)

### **Summary**
- This full-stack project helps you practice both frontend and backend development.
- You’ll build multiple pages (Home, About, Sign Up, and Login) with a shared navbar for navigation.
- **User authentication** and **role-based access control** are implemented with secure login using middleware.
- The backend will manage routes for user registration, authentication, and user management, with additional middleware to handle validation and logging.
- **MongoDB** will serve as the database to store user information.
