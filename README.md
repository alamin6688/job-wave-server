# Job Wave – Freelance Job Platform

A full-stack web application connecting job seekers and employers for freelance work opportunities.

## 📋 Project Overview

**Job Wave** is a comprehensive freelance job marketplace that enables employers to post job opportunities and allows freelancers to bid on projects. The platform streamlines the hiring process with an intuitive interface, secure authentication, and real-time bid management.

**What it solves:**

- Bridges the gap between employers looking to hire and freelancers seeking opportunities
- Eliminates the complexity of manual job posting and application tracking
- Provides a centralized platform for project-based work

**Who it is for:**

- Freelancers seeking flexible work opportunities
- Small businesses and entrepreneurs needing contract work
- Enterprises managing multiple project bids

---

## 🚀 Live Demo & Repository

| Link                    | URL                                               |
| ----------------------- | ------------------------------------------------- |
| **Live Demo**           | https://job-wave-client.vercel.app                |
| **Frontend Repository** | https://github.com/alamin6688/job-wave-client.git |
| **Backend Repository**  | (This repository)                                 |

---

## 🛠️ Tech Stack

**Frontend:**

- React.js
- TypeScript / JavaScript
- Tailwind CSS
- Vercel Deployment

**Backend:**

- Node.js
- Express.js
- MongoDB
- JWT Authentication
- Vercel Deployment

**Database:**

- MongoDB (Cloud)

**Authentication:**

- JSON Web Tokens (JWT)
- Cookie-based session management

---

## ✨ Key Features

- 🔐 **Secure Authentication** – JWT-based user authentication with role-based access
- 💼 **Job Posting** – Employers can create and manage job listings
- 🎯 **Advanced Search & Filtering** – Search jobs by title, filter by category, and sort by deadline
- 💬 **Bid Management** – Freelancers can place bids on jobs; employers review and manage bids
- 📊 **Pagination** – Efficient job listing with pagination for better performance
- ✏️ **Job Management** – Update, edit, and delete job postings
- 🔍 **My Bids Tracking** – Freelancers can view all their placed bids
- 📬 **Bid Requests** – Employers receive and manage bid requests for their jobs
- 🛡️ **Duplicate Bid Prevention** – System prevents duplicate bids from the same user on the same job

---

## 📦 Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
PORT=5000
DB_USER=your_mongodb_user
DB_PASS=your_mongodb_password
ACCESS_TOKEN_SECRET=your_jwt_secret_key
```

**Note:** Never commit the `.env` file to version control.

---

## 🔧 Installation & Setup

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB Atlas account

### Steps

1. **Clone the repository**

   ```bash
   git clone <backend-repo-url>
   cd job-wave-server
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Configure environment variables**
   - Create a `.env` file in the root directory
   - Add the required environment variables (see above)

4. **Run the development server**

   ```bash
   npm start
   ```

   The server will start on `http://localhost:5000` (or the port specified in `.env`)

5. **Verify the connection**
   - Open your browser and navigate to `http://localhost:5000`
   - You should see the message: "Job Wave is running!"

---

## 📡 API Documentation

### Base URL

```
http://localhost:5000
https://your-deployed-url
```

### Authentication

Most endpoints require JWT authentication passed via cookies or Authorization headers.

### Endpoints

#### **Authentication**

| Method | Endpoint  | Description                | Auth Required |
| ------ | --------- | -------------------------- | ------------- |
| `POST` | `/jwt`    | Generate JWT token         | ❌ No         |
| `GET`  | `/logout` | Clear authentication token | ❌ No         |

#### **Jobs**

| Method   | Endpoint          | Description                                | Auth Required |
| -------- | ----------------- | ------------------------------------------ | ------------- |
| `GET`    | `/jobs`           | Get all jobs                               | ❌ No         |
| `GET`    | `/job/:id`        | Get a single job by ID                     | ❌ No         |
| `GET`    | `/jobs/:email`    | Get all jobs posted by a user              | ✅ Yes        |
| `GET`    | `/all-jobs`       | Get paginated jobs with filtering & search | ❌ No         |
| `GET`    | `/all-jobs-count` | Get total count of jobs                    | ❌ No         |
| `POST`   | `/job`            | Create a new job                           | ❌ No         |
| `PUT`    | `/job/:id`        | Update a job                               | ✅ Yes        |
| `DELETE` | `/job/:id`        | Delete a job                               | ❌ No         |

#### **Bids**

| Method  | Endpoint               | Description                          | Auth Required |
| ------- | ---------------------- | ------------------------------------ | ------------- |
| `POST`  | `/bid`                 | Place a bid on a job                 | ❌ No         |
| `GET`   | `/my-bids/:email`      | Get all bids placed by a user        | ✅ Yes        |
| `GET`   | `/bid-requests/:email` | Get all bid requests for a job owner | ✅ Yes        |
| `PATCH` | `/bid/:id`             | Update bid status                    | ❌ No         |

---

## 🚀 Deployment

### Deploy on Vercel

1. **Connect your repository to Vercel**
   - Go to https://vercel.com
   - Import your GitHub repository

2. **Set environment variables**
   - In Vercel project settings, add all required environment variables

3. **Deploy**
   - Vercel will automatically deploy on push to the main branch

### CORS Configuration

The backend is configured to accept requests from:

- `http://localhost:5000`
- `http://localhost:5173`
- `https://job-wave.netlify.app`
- `https://job-wave-client.web.app`
- `https://job-wave-client.vercel.app`

---

## 📈 Future Improvements

- 📧 Email notifications for job updates and bids
- ⭐ User ratings and reviews system
- 💰 Integrated payment processing (Stripe/PayPal)
- 📅 Advanced scheduling and calendar integration
- 🔔 Real-time notifications using WebSockets
- 📊 Analytics dashboard for employers
- 🌐 Multi-language support
- 🎯 AI-powered job recommendation system

---

## 🐛 Known Limitations

- No real-time updates (uses polling/refresh)
- Basic user profile management
- Limited payment integration
- No dispute resolution system yet
- File upload functionality not yet implemented

---

## 👨‍💻 Author & Contact

**Developer:** Al Amin  
**Role:** Full-Stack Developer  
**GitHub:** https://github.com/alamin6688  
**Frontend Repository:** https://github.com/alamin6688/job-wave-client.git

---

## 📄 License

This project is licensed under the ISC License.

---

## 🙏 Acknowledgments

- MongoDB for database hosting
- Vercel for seamless deployment
- Express.js community for excellent documentation

---

**Last Updated:** January 25, 2026
