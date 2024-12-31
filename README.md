# Doctor Appointment-Booking-System

## Description

**Prescripto** is a comprehensive Hospital Management System built on the MERN stack to enhance hospital operations. This system includes features such as secure user authentication, efficient appointment scheduling, patient record management, and real-time communication between doctors and patients. It provides a scalable and user-friendly platform to streamline healthcare workflows and improve the hospital experience.

## PS: The backend was deployed using Render, so there is more than an expected delay. Apologies for the inconvenience!
**Live Link**

  **backend** - https://doctor-appointment-booking-app-backend-1wxp.onrender.com
  
  **frontend** - https://doctor-appointment-booking-app-frontend-n8gi.onrender.com
  
  **admin** - https://doctor-appointment-booking-app-admin.onrender.com


### Images or Demo
#### Desktop view

<div style="display: flex; flex-wrap: nowrap; overflow-x: auto; gap: 20px; padding: 10px; background-color: gray;">

  <img src="screenshots/ws-1.png" alt="web view 1"  style="border-radius: 8px;">

  <img src="screenshots/ws-2.png" alt="web view 2" style="border-radius: 8px;">

  <img src="screenshots/ws-3.png" alt="web view 3"  style="border-radius: 8px;">

  <img src="screenshots/ws-4.png" alt="web view 4"  style="border-radius: 8px;">

  <img src="screenshots/ws-5.png" alt="web view 5"  style="border-radius: 8px;">

  <img src="screenshots/ws-6.png" alt="web view 6"  style="border-radius: 8px;">

  <img src="screenshots/ws-7.png" alt="web view 7"  style="border-radius: 8px;">

  <img src="screenshots/ws-8.png" alt="web view 8"  style="border-radius: 8px;">

  <img src="screenshots/ws-9.png" alt="web view 9"  style="border-radius: 8px;">

  <img src="screenshots/ws-10.png" alt="web view 10"  style="border-radius: 8px;">
  
  <img src="screenshots/ws-11.png" alt="web view 11"  style="border-radius: 8px;">
  
  <img src="screenshots/ws-12.png" alt="web view 12"  style="border-radius: 8px;">
  
  <img src="screenshots/ws-13.png" alt="web view 13"  style="border-radius: 8px;">
  
  <img src="screenshots/ws-14.png" alt="web view 14"  style="border-radius: 8px;">

</div>


#### mobile view

<div style="display: flex; flex-wrap: nowrap; overflow-x: auto; gap: 20px; padding: 10px; background-color: gray;">

  <img src="screenshots/ss-1.jpg" alt="mobile view 1" width="300" 
  style="border-radius: 8px;">

  <img src="screenshots/ss-2.jpg" alt="mobile view 2" width="300"  style="border-radius: 8px;">

  <img src="screenshots/ss-3.jpg" alt="mobile view 3" width="300"  style="border-radius: 8px;">

  <img src="screenshots/ss-4.jpg" alt="mobile view 4" width="300"  style="border-radius: 8px;">

  <img src="screenshots/ss-5.jpg" alt="mobile view 5" width="300"  style="border-radius: 8px;">

  <img src="screenshots/ss-6.jpg" alt="mobile view 6" width="300"  style="border-radius: 8px;">

  <img src="screenshots/ss-7.jpg" alt="mobile view 7" width="300"  style="border-radius: 8px;">

  <img src="screenshots/ss-8.jpg" alt="mobile view 8" width="300"  style="border-radius: 8px;">

  <img src="screenshots/ss-9.jpg" alt="mobile view 9" width="300"  style="border-radius: 8px;">

</div>


## Table of Contents

- [Doctor Appointment-Booking-System](#doctor-appointment-booking-system)
  - [Description](#description)
  - [PS: The backend was deployed using Render, so there is more than an expected delay. Apologies for the inconvenience!](#ps-the-backend-was-deployed-using-render-so-there-is-more-than-an-expected-delay-apologies-for-the-inconvenience)
    - [Images or Demo](#images-or-demo)
      - [Desktop view](#desktop-view)
      - [mobile view](#mobile-view)
  - [Table of Contents](#table-of-contents)
    - [Tech Stack](#tech-stack)
      - [Frontend](#frontend)
      - [Backend](#backend)
      - [Development Tools](#development-tools)
    - [Features](#features)
      - [User Features](#user-features)
      - [Doctor Features](#doctor-features)
      - [Admin Features](#admin-features)
      - [General Features](#general-features)
    - [Installation Instructions](#installation-instructions)
      - [Prerequisites](#prerequisites)
      - [Installation](#installation)
- [API Documentation](#api-documentation)
  - [User Routes](#user-routes)
  - [Doctor Routes](#doctor-routes)
  - [Admin Routes](#admin-routes)
    - [Deployment](#deployment)

---

### Tech Stack
[![My Skills](https://skillicons.dev/icons?i=js,react,nodejs,express,vercel,mongodb,tailwind,html,css)](https://skillicons.dev)

#### Frontend
- **React.js**: A JavaScript library for building user interfaces.
- **React Router DOM**: A collection of navigational components for React applications.
- **React Toastify**: A library for adding notifications to your React app.
- **Vite**: A build tool that aims to provide a faster and leaner development experience for modern web projects.
- **Tailwind CSS**: A utility-first CSS framework for rapid UI development.
- **Axios**: A promise-based HTTP client for the browser and Node.js.

#### Backend
- **Node.js**: A JavaScript runtime built on Chrome's V8 JavaScript engine.
- **Express.js**: A minimal and flexible Node.js web application framework.
- **Mongoose**: An ODM (Object Data Modeling) library for MongoDB and Node.js.
- **JWT (jsonwebtoken)**: A library to work with JSON Web Tokens.
- **Bcrypt**: A library to help you hash passwords.
- **Multer**: A middleware for handling `multipart/form-data`, which is primarily used for uploading files.
- **Cloudinary**: A cloud service that offers a solution to a web application's entire image management pipeline.
- **Razorpay**: A payment gateway solution.
- **Stripe**: A suite of APIs powering online payment processing and commerce solutions.
- **Validator**: A library for string validation and sanitization.
- **Cors**: A package for providing a Connect/Express middleware that can be used to enable CORS with various options.
- **Dotenv**: A module that loads environment variables from a `.env` file into `.env`.

#### Development Tools

- **Nodemon**: A tool that helps develop Node.js based applications by automatically restarting the node application when file changes in the directory are detected.
- **ESLint**: A tool for identifying and reporting on patterns found in ECMAScript/JavaScript code.
- **PostCSS**: A tool for transforming CSS with JavaScript plugins.
- **Autoprefixer**: A PostCSS plugin to parse CSS and add vendor prefixes to CSS rules using values from Can I Use.

### Features

#### User Features

- **User Authentication**: Secure login and registration for patients, doctors, and administrators.
- **Profile Management**: Users can update their profile information, including personal details and profile picture.
- **Appointment Booking**: Patients can book appointments with doctors based on their availability.
- **Appointment Management**: Patients can view, cancel, and reschedule their appointments.
- **Payment Integration**: Secure online payment options using Razorpay and Stripe for appointment fees.
- **Doctor Search**: Patients can search for doctors by specialty and location.
- **Doctor Profiles**: Detailed profiles for doctors, including their specialties, experience, and availability.
- **Notifications**: Real-time notifications for appointment confirmations, cancellations, and reminders.

#### Doctor Features

- **Doctor Dashboard**: Overview of appointments, earnings, and patient statistics.
- **Appointment Management**: Doctors can view, cancel, and mark appointments as completed.
- **Profile Management**: Doctors can update their profile information, including personal details, specialties, and availability.
- **Patient Communication**: Real-time messaging with patients for consultations and follow-ups.

#### Admin Features

- **Admin Dashboard**: Overview of hospital operations, including user statistics, appointment analytics, and system performance.
- **User Management**: Admins can manage user accounts, including patients, doctors, and other administrators.
- **Doctor Management**: Admins can add, update, and remove doctor profiles.
- **Appointment Management**: Admins can view and manage all appointments in the system.
- **Data Analytics**: Detailed analytics and reports on hospital operations, user activity, and appointment trends.

#### General Features

- **Responsive Design**: The application is fully responsive and works seamlessly on both web and mobile devices.
- **Secure Data Storage**: All user data is securely stored and managed using MongoDB.
- **Environment Configuration**: Easy configuration of environment variables for different deployment environments.
- **Error Handling**: Comprehensive error handling and logging for better system reliability and debugging.

### Installation Instructions

#### Prerequisites
- Node.js installed
- MongoDB installed or access to a MongoDB cloud instance
- Git installed

#### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/Prescripto-Hospital_Management_System.git
   ```
2. **Install dependencies for the backend**  
   ```bash
   cd backend
   npm install
   ```
3. **Install dependencies for the admin panel**
   ```bash
   cd ../admin
   npm install
   ```
4. **Install dependencies for the frontend**
   ```bash
   cd ../frontend
   npm install
   ```
5. **Set up environment variables**

Create a `.env` file in the backend, admin, and frontend directories and add the necessary environment variables 

6. **Start the backend server**
   ```bash
   cd backend
   npm server.js
   ```
7. **Start the admin panel**
   ```bash
   cd admin
   npm run dev
   ```
8. **Start the frontend application**
   ```bash
   cd frontend
   npm run dev
   ```
**Accessing the Application**
Access the admin panel at `http://localhost:5174`
Access the backend API at `http://localhost:4000`
Access the frontend application at `http://localhost:5173`

# API Documentation

## User Routes

| **Method** | **Endpoint**                      | **Description**                                     | **Requires Authentication** |
|------------|------------------------------------|---------------------------------------------------|-----------------------------|
| POST       | `/api/user/register`              | Register a new user.                              | No                          |
| POST       | `/api/user/login`                 | Login a user.                                     | No                          |
| GET        | `/api/user/get-profile`           | Get user profile data.                            | Yes                         |
| POST       | `/api/user/update-profile`        | Update user profile data.                         | Yes                         |
| POST       | `/api/user/book-appointment`      | Book an appointment.                              | Yes                         |
| GET        | `/api/user/appointments`          | Get user appointments.                            | Yes                         |
| POST       | `/api/user/cancel-appointment`    | Cancel an appointment.                            | Yes                         |
| POST       | `/api/user/payment-razorpay`      | Make payment for an appointment using Razorpay.   | Yes                         |
| POST       | `/api/user/verifyRazorpay`        | Verify Razorpay payment.                          | Yes                         |
| POST       | `/api/user/payment-stripe`        | Make payment for an appointment using Stripe.     | Yes                         |
| POST       | `/api/user/verifyStripe`          | Verify Stripe payment.                            | Yes                         |

## Doctor Routes

| **Method** | **Endpoint**                      | **Description**                                     | **Requires Authentication** |
|------------|------------------------------------|---------------------------------------------------|-----------------------------|
| POST       | `/api/doctor/login`               | Login a doctor.                                   | No                          |
| POST       | `/api/doctor/cancel-appointment`  | Cancel an appointment.                            | Yes                         |
| GET        | `/api/doctor/appointments`        | Get doctor appointments.                          | Yes                         |
| GET        | `/api/doctor/list`                | Get list of all doctors.                          | No                          |
| POST       | `/api/doctor/change-availability` | Change doctor availability.                       | Yes                         |
| POST       | `/api/doctor/complete-appointment`| Mark an appointment as completed.                | Yes                         |
| GET        | `/api/doctor/dashboard`           | Get doctor dashboard data.                        | Yes                         |
| GET        | `/api/doctor/profile`             | Get doctor profile data.                          | Yes                         |
| POST       | `/api/doctor/update-profile`      | Update doctor profile data.                       | Yes                         |

## Admin Routes

| **Method** | **Endpoint**                      | **Description**                                     | **Requires Authentication** |
|------------|------------------------------------|---------------------------------------------------|-----------------------------|
| POST       | `/api/admin/login`                | Login an admin.                                   | No                          |
| POST       | `/api/admin/add-doctor`           | Add a new doctor.                                 | Yes                         |
| GET        | `/api/admin/appointments`         | Get all appointments.                             | Yes                         |
| POST       | `/api/admin/cancel-appointment`   | Cancel an appointment.                            | Yes                         |
| GET        | `/api/admin/all-doctors`          | Get list of all doctors.                          | Yes                         |
| POST       | `/api/admin/change-availability`  | Change doctor availability.                       | Yes                         |
| GET        | `/api/admin/dashboard`            | Get admin dashboard data.                         | Yes                         |

  
### Deployment
- the services are deployed on render using free pack so might be slow in use....
- thank you for visiting




