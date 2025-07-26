# Invoice Generator & Payment Tracker

A full-stack MERN (MongoDB, Express.js, React, Node.js) application for generating invoices and tracking payments.

## 🚀 Live Demo

- **Frontend**: [https://your-frontend.vercel.app](https://your-frontend.vercel.app)
- **Backend API**: [https://your-backend.onrender.com](https://your-backend.onrender.com)

## 🛠 Tech Stack

- **Frontend**: React, Vite, TailwindCSS
- **Backend**: Node.js, Express.js
- **Database**: MongoDB Atlas
- **Deployment**: Vercel (Frontend), Render (Backend)
- **CI/CD**: GitHub Actions
- **Monitoring**: UptimeRobot, Sentry

## 📋 Prerequisites

- Node.js (v18 or higher)
- npm (v9 or higher) or yarn
- MongoDB Atlas account
- GitHub account
- Vercel account (for frontend deployment)
- Render account (for backend deployment)

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/invoice-generator-payment-tracker.git
cd invoice-generator-payment-tracker
```

### 2. Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file based on the example:
   ```bash
   cp .env.example .env
   ```

4. Update the `.env` file with your MongoDB Atlas connection string and other configurations.

5. Start the development server:
   ```bash
   npm run dev
   ```

### 3. Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file based on the example:
   ```bash
   cp .env.example .env
   ```

4. Update the `.env` file with your backend API URL.

5. Start the development server:
   ```bash
   npm run dev
   ```

## 🚀 Deployment

### Backend Deployment (Render)

1. Push your code to a GitHub repository.
2. Create a new Web Service on Render.
3. Connect your GitHub repository.
4. Configure the following settings:
   - **Build Command**: `npm install && npm run build`
   - **Start Command**: `node dist/index.js`
   - **Environment Variables**: Add all variables from your `.env` file

### Frontend Deployment (Vercel)

1. Push your code to a GitHub repository.
2. Import your project in Vercel.
3. Configure the following settings:
   - **Framework Preset**: Vite
   - **Root Directory**: `frontend`
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
   - **Environment Variables**: Add all variables from your `.env` file

## 🔄 CI/CD Pipeline

This project uses GitHub Actions for CI/CD. The workflow includes:

- Linting and testing on pull requests
- Automatic deployment to staging on push to `develop`
- Automatic deployment to production on push to `main`

### Required Secrets

Add these secrets to your GitHub repository settings:

- `RENDER_DEPLOY_HOOK`: Webhook URL from Render
- `VERCEL_TOKEN`: Vercel authentication token
- `VERCEL_ORG_ID`: Vercel organization ID
- `VERCEL_PROJECT_ID`: Vercel project ID

## 📈 Monitoring

### Uptime Monitoring
- Backend: Monitored at `/health` endpoint
- Frontend: Monitored at root URL
- Set up in UptimeRobot with 5-minute intervals

### Error Tracking
- Frontend: Sentry integrated via `@sentry/react`
- Backend: Sentry integrated via `@sentry/node`

## 📂 Project Structure

```
invoice-generator-payment-tracker/
├── backend/                 # Express.js backend
│   ├── src/
│   │   ├── controllers/     # Route controllers
│   │   ├── models/          # MongoDB models
│   │   ├── routes/          # API routes
│   │   ├── middleware/      # Custom middleware
│   │   ├── utils/           # Utility functions
│   │   └── app.js           # Express app setup
│   ├── .env.example         # Environment variables example
│   ├── package.json
│   └── ...
│
├── frontend/                # React frontend
│   ├── public/              # Static files
│   ├── src/
│   │   ├── assets/          # Images, fonts, etc.
│   │   ├── components/      # Reusable components
│   │   ├── pages/           # Page components
│   │   ├── services/        # API services
│   │   ├── store/           # State management
│   │   ├── utils/           # Utility functions
│   │   ├── App.jsx          # Main app component
│   │   └── main.jsx         # Entry point
│   ├── .env.example         # Environment variables example
│   ├── package.json
│   └── ...
│
├── .github/
│   └── workflows/           # GitHub Actions workflows
│       └── ci-cd.yml        # CI/CD pipeline
│
├── .env.example             # Root .env example
└── README.md                # This file

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Vite](https://vitejs.dev/)
- [React](https://reactjs.org/)
- [Express.js](https://expressjs.com/)
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
- [TailwindCSS](https://tailwindcss.com/)
- [Render](https://render.com/)
- [Vercel](https://vercel.com/)