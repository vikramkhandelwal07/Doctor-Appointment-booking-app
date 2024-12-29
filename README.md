# Prescripto - Hospital Management System

## Description
**Prescripto** is a comprehensive Hospital Management System built on the MERN stack to enhance hospital operations. This system includes features such as secure user authentication, efficient appointment scheduling, patient record management, and real-time communication between doctors and patients. It provides a scalable and user-friendly platform to streamline healthcare workflows and improve the hospital experience.

## Features
- **User Authentication**: Secure login for patients, doctors, and administrators.
- **Appointment Scheduling**: Easy booking, rescheduling, and cancellation of appointments.
- **Patient Records Management**: Store, access, and update patient health records.
- **Doctor-Patient Communication**: Real-time messaging for consultations and follow-ups.
- **Admin Dashboard**: Manage users, appointments, and view analytics.
- **Secure Data Storage**: Ensure patient privacy and data security with MongoDB.

## Tech Stack
- **Frontend**: React.js
- **Backend**: Node.js and Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **State Management**: Redux (optional)

## Getting Started
Follow these instructions to set up the project locally.

### Prerequisites
- Node.js installed
- MongoDB installed or access to a MongoDB cloud instance
- Git installed

### Installation
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/Prescripto-Hospital_Management_System.git
   cd Prescripto-Hospital_Management_System

## Install dependencies

1. **Install admin dependencies**
   ```bash
   cd admin
   npm install
   ```

2. **Install frontend dependencies**
   ```bash
   cd frontend
   npm install
   ```

3. **Set up environment variables**
   In the server directory, create a .env file with the following:

   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   Run the application

4. **Start server:**
   ```bash
   cd backend
   npm run server
   ```

5. **Start Admin Panel:**
   ```bash
   cd admin
   npm run dev
   ```

6. **Start Frontend Panel:**
   ```bash
   cd frontend
   npm run dev
   ```

# Topics
Hospital Management, MERN Stack, MongoDB, Express.js, React, Node.js, Healthcare App, Patient Records, Appointments.

# Contributors
Rithvik Sighakolli [Github](https://github.com/rithviksighakolli)

# Deployment Links
[Prescripto Patient Panel](https://prescripto-hospital-management-system-2dlr.onrender.com)

[Prescripto Admin/Doctor Panel](https://prescripto-hospital-management-system-dmls.onrender.com)

# Contact
For any questions or feedback, please contact [Rithvik Sighakolli](https://mail.google.com/mail/u/0/?tab=rm&ogbl#inbox?compose=GTvVlcSGLdXhmkgwVNdVxlKMVGdjhjxJTzgSsdkdVZdtWgrnhHsRXcxcMlSVxjWjwVvNTQxZDgHxM)

# License
This project is licensed under the MIT License.

```
import React, { useContext, useEffect, useState } from 'react'
import { AppContext } from '../context/AppContext'
import axios from 'axios'
import { toast } from 'react-toastify'
import { useNavigate } from 'react-router-dom'

const Login = () => {

  const [state, setState] = useState('Sign Up')

  const [name, setName] = useState('')
  const [email, setEmail] = useState('')
  const [password, setPassword] = useState('')

  const navigate = useNavigate()
  const { backendUrl, token, setToken } = useContext(AppContext)

  const onSubmitHandler = async (event) => {
    event.preventDefault();

    if (state === 'Sign Up') {

      const { data } = await axios.post(backendUrl + '/api/user/register', { name, email, password })

      if (data.success) {
        localStorage.setItem('token', data.token)
        setToken(data.token)
      } else {
        toast.error(data.message)
      }

    } else {

      const { data } = await axios.post(backendUrl + '/api/user/login', { email, password })

      if (data.success) {
        localStorage.setItem('token', data.token)
        setToken(data.token)
      } else {
        toast.error(data.message)
      }

    }

  }

  useEffect(() => {
    if (token) {
      navigate('/')
    }
  }, [token])

  return (
    <form onSubmit={onSubmitHandler} className='min-h-[80vh] flex items-center'>
      <div className='flex flex-col gap-3 m-auto items-start p-8 min-w-[340px] sm:min-w-96 border rounded-xl text-[#5E5E5E] text-sm shadow-lg'>
        <p className='text-2xl font-semibold'>{state === 'Sign Up' ? 'Create Account' : 'Login'}</p>
        <p>Please {state === 'Sign Up' ? 'sign up' : 'log in'} to book appointment</p>
        {state === 'Sign Up'
          && <div className='w-full '>
            <p>Full Name</p>
            <input onChange={(e) => setName(e.target.value)} value={name} className='border border-[#DADADA] rounded w-full p-2 mt-1' type="text" required />
          </div>
          
        }
        <div className='w-full '>
          <p>Email</p>
          <input onChange={(e) => setEmail(e.target.value)} value={email} className='border border-[#DADADA] rounded w-full p-2 mt-1' type="email" required />
        </div>
        <div className='w-full '>
          <p>Password</p>
          <input onChange={(e) => setPassword(e.target.value)} value={password} className='border border-[#DADADA] rounded w-full p-2 mt-1' type="password" required />
        </div>
        <button className='bg-primary text-white w-full py-2 my-2 rounded-md text-base'>{state === 'Sign Up' ? 'Create account' : 'Login'}</button>
        {state === 'Sign Up'
          ? <p>Already have an account? <span onClick={() => setState('Login')} className='text-primary underline cursor-pointer'>Login here</span></p>
          : <p>Create an new account? <span onClick={() => setState('Sign Up')} className='text-primary underline cursor-pointer'>Click here</span></p>
        }
      </div>
    </form>
  )
}

export default Login
```