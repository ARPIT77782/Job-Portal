<h1 align="center">
  <br>
  💼 HireHub — Job Portal
  <br>
</h1>

<p align="center">
  A full-stack Job Portal web application built with React, Supabase, and Clerk Authentication.
  <br />
  <a href="https://job-portal-wine-six.vercel.app/" target="_blank"><strong>🌐 View Live Demo »</strong></a>
  <br />
  <br />
  <img src="https://img.shields.io/badge/React-18.3.1-61DAFB?style=for-the-badge&logo=react&logoColor=white" />
  <img src="https://img.shields.io/badge/Vite-5.3.4-646CFF?style=for-the-badge&logo=vite&logoColor=white" />
  <img src="https://img.shields.io/badge/Supabase-2.45.0-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" />
  <img src="https://img.shields.io/badge/Clerk-Auth-6C47FF?style=for-the-badge&logo=clerk&logoColor=white" />
  <img src="https://img.shields.io/badge/TailwindCSS-3.4.7-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/Deployed-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" />
</p>

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Variables](#environment-variables)
  - [Run Locally](#run-locally)
- [Deployment](#-deployment)
  - [Deploy on Vercel](#deploy-on-vercel)
  - [Deploy on Render](#deploy-on-render)
- [Application Routes](#-application-routes)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🚀 About the Project

**HireHub** is a modern, full-stack Job Portal that connects **Job Seekers** and **Recruiters** on a single platform. It features role-based onboarding, real-time job listings, resume uploads, job saving, and application tracking — all powered by Supabase as the backend and Clerk for secure authentication.

---

## ✨ Features

### 👤 For Job Seekers
- 🔐 Secure Sign Up / Sign In via Clerk
- 🔍 Browse and search all job listings
- 🏷️ Filter jobs by **location**, **company**, and **job type**
- 📄 Apply to jobs with resume upload (PDF/Word)
- 💾 Save/bookmark jobs for later
- 📊 Track all submitted applications

### 🏢 For Recruiters
- 📝 Post new job openings with full details
- 🏢 Add and manage company profiles
- 👁️ View all applications received per job
- ✅ Hire or ❌ Reject applicants directly
- 📋 Manage all posted jobs from a dashboard

### 🌐 General
- 🌙 Dark / Light mode toggle
- 📱 Fully responsive design (mobile-friendly)
- ⚡ Blazing fast with Vite
- 🔒 Protected routes (auth-gated pages)

---

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| **React 18** | Frontend UI framework |
| **Vite** | Build tool & dev server |
| **Tailwind CSS** | Styling |
| **Shadcn/UI + Radix UI** | UI Components |
| **Supabase** | Database, Storage & Backend APIs |
| **Clerk** | Authentication & User Management |
| **React Router DOM v6** | Client-side routing |
| **React Hook Form + Zod** | Form handling & validation |
| **Lucide React** | Icons |
| **Embla Carousel** | Landing page carousel |

---

## 📁 Project Structure

```
job-portal/
├── public/                  # Static assets
├── src/
│   ├── api/                 # Supabase API call functions
│   ├── components/          # Reusable UI components
│   │   ├── apply-job.jsx        # Job application drawer
│   │   ├── job-card.jsx         # Job listing card
│   │   ├── header.jsx           # Navigation header
│   │   ├── protected-route.jsx  # Auth guard wrapper
│   │   ├── add-company-drawer.jsx
│   │   ├── application-card.jsx
│   │   ├── created-applications.jsx
│   │   ├── created-jobs.jsx
│   │   └── ui/              # Shadcn UI components
│   ├── hooks/               # Custom React hooks
│   │   └── use-fetch.js     # Data fetching hook
│   ├── layouts/             # Page layout wrappers
│   ├── pages/               # Application pages
│   │   ├── landing.jsx      # Home / Landing page
│   │   ├── onboarding.jsx   # Role selection page
│   │   ├── jobListing.jsx   # All jobs listing
│   │   ├── job.jsx          # Single job detail
│   │   ├── post-job.jsx     # Post a new job
│   │   ├── my-jobs.jsx      # Recruiter's posted jobs
│   │   └── saved-jobs.jsx   # Job seeker's saved jobs
│   ├── utils/               # Utility functions
│   │   └── supabase.js      # Supabase client config
│   ├── App.jsx              # Root component with routes
│   └── main.jsx             # Entry point with ClerkProvider
├── .env                     # Environment variables (not committed)
├── .env.example             # Environment variables template
├── index.html
├── package.json
├── tailwind.config.js
├── vite.config.js
└── vercel.json              # Vercel deployment config
```

---

## 🏁 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or higher)
- [Git](https://git-scm.com/)
- A [Supabase](https://supabase.com) account
- A [Clerk](https://clerk.com) account

---

### Installation

**1. Clone the repository**
```bash
git clone https://github.com/ARPIT77782/Job-Portal.git
cd Job-Portal
```

**2. Install dependencies**
```bash
npm install
```

---

### Environment Variables

Create a `.env` file in the root directory:

```bash
cp .env.example .env
```

Then fill in your values:

```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
```

#### How to get these keys:

**Supabase Keys:**
1. Go to [supabase.com](https://supabase.com) → Your Project
2. Navigate to **Settings → API**
3. Copy **Project URL** and **anon public** key

**Clerk Publishable Key:**
1. Go to [clerk.com](https://clerk.com) → Your Application
2. Navigate to **Configure → API Keys**
3. Copy the **Publishable Key** (starts with `pk_test_...`)

---

### Run Locally

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

**Other available commands:**

| Command | Description |
|---|---|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Run ESLint checks |

---

## 🚀 Deployment

### Deploy on Vercel

**Option A — Using Vercel CLI:**

```bash
# Install Vercel CLI
npm install -g vercel

# Login
vercel login

# Deploy
vercel

# Add environment variables
vercel env add VITE_SUPABASE_URL
vercel env add VITE_SUPABASE_ANON_KEY
vercel env add VITE_CLERK_PUBLISHABLE_KEY

# Deploy to production
vercel --prod
```

**Option B — Using Vercel Dashboard:**

1. Go to [vercel.com](https://vercel.com) → **New Project**
2. Import **`ARPIT77782/Job-Portal`** from GitHub
3. Set build settings:
   - **Framework**: `Vite`
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
4. Add all 3 environment variables
5. Click **Deploy**

> ⚠️ **After deploying**, add your Vercel URL to Clerk's allowed domains:
> Clerk Dashboard → Your App → **Configure → Domains → Add Domain**

---

### Deploy on Render

1. Go to [render.com](https://render.com) → **New → Static Site**
2. Connect repo: **`ARPIT77782/Job-Portal`**
3. Configure:
   - **Build Command**: `npm install && npm run build`
   - **Publish Directory**: `dist`
4. Add environment variables (same 3 keys)
5. Click **Create Static Site**

---

## 🗺 Application Routes

| Route | Page | Access |
|---|---|---|
| `/` | Landing Page | Public |
| `/onboarding` | Role Selection (Seeker / Recruiter) | Auth Required |
| `/jobs` | All Job Listings | Auth Required |
| `/job/:id` | Single Job Detail + Apply | Auth Required |
| `/post-job` | Post a New Job | Recruiter Only |
| `/my-jobs` | Manage Posted Jobs | Recruiter Only |
| `/saved-jobs` | Saved / Bookmarked Jobs | Job Seeker Only |

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

```bash
# Fork the repo, then:
git clone https://github.com/your-username/Job-Portal.git
cd Job-Portal
git checkout -b feature/your-feature-name

# Make your changes, then:
git add .
git commit -m "feat: add your feature description"
git push origin feature/your-feature-name

# Open a Pull Request on GitHub
```

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<p align="center">
  Made with ❤️ | <a href="https://job-portal-wine-six.vercel.app/">Live Demo</a>
</p>
