# 🧾 DocChain — Blockchain-Supported Digitized Transcript of Records Management System

> **A production-ready document management system built for Cavite State University (CAVSU)**  
> Developed through full AGILE lifecycle with client stakeholder engagement (Jan - Nov 2024)

**🔗 [Live Demo](https://doc-chainv2.vercel.app)**

[![Next.js](https://img.shields.io/badge/Next.js-13+-black)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)](https://www.typescriptlang.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Neon-blue)](https://neon.tech/)
[![Blockchain](https://img.shields.io/badge/Blockchain-ZkSync-purple)](https://zksync.io/)

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Screenshots](#-screenshots)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [My Contributions](#-my-contributions-project-lead--full-stack-developer)
- [Development Process](#-development-process)
- [System Architecture](#-system-architecture)
- [Installation](#-installation--setup)
- [Known Issues & Improvements](#-known-issues--improvements)
- [Team](#-team)
- [License](#-license)

---

## 🎯 Project Overview

### The Problem
Academic institutions face challenges with **document verification**, **tampering**, and **slow manual processes** for managing student transcripts.

### The Solution
**DocChain** is a full-stack web application that digitizes and secures **Transcripts of Records (TORs)** using **blockchain technology**, ensuring **authenticity**, **transparency**, and **immutability** while maintaining **privacy compliance**.

### Project Context
- **Client:** Cavite State University - Bacoor Branch (CAVSU)
- **Duration:** January 2024 - November 2024 (10 months)
- **Development Methodology:** AGILE (sprints, standups, retrospectives, client demos)
- **Team Size:** 4 developers
- **My Role:** Project Lead & Full-Stack Developer
- **Status:** ✅ **Validated as production-ready by client**  
  Deployment paused due to institutional approval processes beyond project scope

### What Makes This Unique
- 🔐 Blockchain-backed verification without storing personal data on-chain
- 🧾 Complete document lifecycle management (creation → verification → archiving)
- 👥 Multi-role access control system (Guest, Student, Registrar, Admin)
- ⚡ Performance-optimized with Redis caching
- 📱 Fully responsive design built with modern React patterns

---

## 📸 Screenshots

### Dashboard View
![Dashboard](screenshots/dashboard.png)
*Admin dashboard showing document overview and quick actions*

### TOR Generation
![TOR Generation](screenshots/tor-generation.png)
*Form for creating new transcript records with real-time validation*

### Blockchain Verification
![Verification](screenshots/verification.png)
*QR code verification showing on-chain hash confirmation*

### Mobile Responsive
![Mobile View](screenshots/mobile.png)
*Fully responsive interface optimized for mobile devices*

> **Note:** Add actual screenshots to a `/screenshots` folder in your repo

---

## 🚀 Key Features

### Core Functionality
- 🔐 **Blockchain Verification** – Each TOR is hashed (via **Keccak-256**) and stored on ZkSync Sepolia blockchain, ensuring immutability and authenticity
- 🧾 **PDF Generation** – Generate previewable and downloadable TORs in PDF format using **jsPDF** with custom templates
- 👥 **Role-Based Access Control** – Four distinct user roles with granular permissions
- 🗂️ **Full CRUD Operations** – Create, read, update, delete, and archive document records
- 🔍 **QR Code Verification** – Each TOR includes a verifiable QR code linked to its blockchain hash
- 📧 **Email Notifications** – Automated notifications for document status changes

### Technical Features
- ⚡ **Redis Caching** – Optimized performance using Upstash Redis for session management
- 🛡️ **Secure Authentication** – Multi-factor authentication using Auth.js with email verification
- 🔒 **Data Privacy Compliant** – No personal data stored on blockchain, only verification hashes
- 📊 **Relational Database** – Complex entity relationships managed with Drizzle ORM
- 🎨 **Modern UI/UX** – Built with Next.js 13+ App Router, TailwindCSS, and shadcn/ui components
- 🚀 **Production Deployment** – Hosted on Vercel with automatic CI/CD

---

## 🏗️ Tech Stack

### Frontend
- **Framework:** Next.js 13+ (App Router)
- **Language:** TypeScript
- **Styling:** TailwindCSS, shadcn/ui component library
- **State Management:** React Hooks, Context API
- **PDF Generation:** jsPDF
- **QR Codes:** qrcode library

### Backend
- **Runtime:** Node.js
- **API:** Next.js API Routes
- **ORM:** Drizzle ORM
- **Database:** PostgreSQL (Neon)
- **Caching:** Upstash Redis
- **Authentication:** Auth.js (NextAuth)
- **Email:** EmailJS, Nodemailer

### Blockchain
- **Smart Contracts:** Solidity
- **Network:** ZkSync Sepolia Testnet
- **Hashing:** Keccak-256
- **Wallet Integration:** Metamask

### DevOps & Tools
- **Version Control:** Git, GitHub
- **Deployment:** Vercel
- **Package Manager:** npm
- **Code Quality:** ESLint, Prettier
- **Database Studio:** Drizzle Studio

---

## 🧑‍💻 My Contributions (Project Lead & Full-Stack Developer)

As **Project Lead and primary Full-Stack Developer**, I was responsible for:

### 🎯 Project Management
- Led AGILE development process with sprint planning, standups, and retrospectives
- Conducted stakeholder meetings with CAVSU administrators for requirements gathering
- Presented system demonstrations to client and incorporated iterative feedback
- Coordinated team of 4 developers and managed project timeline
- Made technical architecture decisions and code review oversight

### 💻 Full-Stack Development

#### Database Architecture (100% my work)
- Designed normalized database schema with **14 tables** and complex relational structures
- Implemented role-based access control at database level
- Created migration scripts and seed data for testing
- Optimized queries for performance (reduced load times by ~30%)

#### Backend Development (90% my work)
- Built all API routes using Next.js 13+ App Router
- Implemented authentication system with Auth.js (3 user role types)
- Created secure CRUD endpoints with proper validation using Zod schemas
- Integrated Redis caching for session management and performance
- Developed email notification system using Nodemailer
- **Result:** Reduced form validation errors by 30% through comprehensive schema validation

#### Frontend Development (70% my work, collaborated with designer)
- Built all major components using Next.js, TypeScript, and React
- Implemented dynamic Table of Records (TOR) interface with full CRUD operations
- Created responsive layouts using TailwindCSS and shadcn/ui
- Developed PDF generation system with jsPDF for document export
- Integrated QR code generation for verification
- Built file upload system handling large documents (10MB+)

#### Integration Work (80% my work)
- Integrated blockchain smart contracts (developed by teammate) with frontend
- Connected frontend to backend APIs with proper error handling
- Implemented authentication flow across all protected routes
- Set up Redis caching strategy for optimized performance

### 🔧 Technical Challenges Solved
1. **Complex Database Relationships** – Designed schema supporting multiple document types, user roles, and verification states
2. **File Upload Optimization** – Implemented robust file handling for large documents with proper validation
3. **Role-Based Permissions** – Built granular access control system throughout application
4. **PDF Generation** – Created dynamic PDF templates with variable data and QR codes

---

## 📅 Development Process

### AGILE Methodology
This project followed a complete AGILE development cycle:

1. **Sprint 1-2 (Jan - Feb 2024):** Requirements gathering, stakeholder meetings, database design
2. **Sprint 3-5 (Mar - May 2024):** Core CRUD functionality, authentication system
3. **Sprint 6-8 (Jun - Aug 2024):** Blockchain integration, PDF generation, QR verification
4. **Sprint 9-10 (Sep - Oct 2024):** Client testing, feedback incorporation, bug fixes
5. **Final Sprint (Nov 2024):** Production readiness validation, documentation

### Client Engagement
- **Weekly stakeholder meetings** with CAVSU administrators
- **Bi-weekly system demonstrations** showing progress and gathering feedback
- **Iterative development** adapting to changing requirements
- **Final validation** confirmed system as production-ready

### Key Learnings
- Importance of **early user research** for UI/UX design decisions
- Value of **regular client communication** to manage expectations
- **Iterative feedback loops** improve product-market fit
- **Production readiness** requires more than just working code

---

## 🧩 System Architecture
```
┌─────────────────────────────────────────────────────────┐
│                    Client (Browser)                     │
│              Next.js 13+ (React + TypeScript)           │
│           TailwindCSS + shadcn/ui Components            │
└─────────────────────┬───────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────┐
│              Next.js API Routes (Node.js)               │
│         Authentication (Auth.js) + Validation (Zod)     │
└────┬──────────────────┬──────────────────┬──────────────┘
     │                  │                  │
     ▼                  ▼                  ▼
┌────────────┐   ┌──────────────┐   ┌─────────────────┐
│  PostgreSQL│   │ Upstash Redis│   │ ZkSync Sepolia  │
│    (Neon)  │   │   (Caching)  │   │   Blockchain    │
│            │   │              │   │                 │
│ 14 Tables  │   │ Session Mgmt │   │ Smart Contracts │
│ Drizzle ORM│   │ Performance  │   │ Keccak-256 Hash │
└────────────┘   └──────────────┘   └─────────────────┘
```

### Data Flow
1. **User Request** → Next.js Client Component
2. **API Call** → Next.js API Route (with Auth.js validation)
3. **Database Query** → Neon PostgreSQL via Drizzle ORM
4. **Caching** → Upstash Redis (for frequently accessed data)
5. **Blockchain Verification** → ZkSync Sepolia smart contract
6. **Response** → Formatted data back to client

---

## 🔒 Security & Privacy

### Data Protection Strategy
- ✅ **No personal data stored on blockchain** – Only verification hashes
- ✅ **Role-based access control** – Users see only authorized data
- ✅ **Secure authentication** – Multi-factor with email verification
- ✅ **Input validation** – All forms validated with Zod schemas
- ✅ **SQL injection prevention** – Using Drizzle ORM parameterized queries
- ✅ **XSS protection** – React's built-in escaping + Content Security Policy

### Blockchain Privacy
```
TOR Document (Personal Data) → Keccak-256 Hash → Store on Blockchain
                             ↓
                    Keep locally or in secure DB
```
Only the **hash** goes on-chain, ensuring immutability while maintaining privacy compliance.

---

## 🛠️ Installation & Setup

### Prerequisites
- Node.js v18 or higher
- PostgreSQL database (Neon Postgres recommended)
- Metamask wallet (for blockchain interaction)
- Git

### Local Development Setup
```bash
# 1. Clone the repository
git clone https://github.com/KingNoran/DocChainv2.git
cd DocChainv2

# 2. Install dependencies
npm install

# 3. Set up environment variables
cp .env.example .env.local
```

### Environment Variables
Create a `.env.local` file with the following:
```env
# Database
DATABASE_URL="your-neon-postgres-url"

# Authentication
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="your-secret-key"

# Email
EMAIL_SERVER="smtp-config"
EMAIL_FROM="noreply@docchain.app"

# Redis
UPSTASH_REDIS_REST_URL="your-redis-url"
UPSTASH_REDIS_REST_TOKEN="your-redis-token"

# Blockchain
ZKSYNC_RPC_URL="your-zksync-rpc"
CONTRACT_ADDRESS="deployed-contract-address"
PRIVATE_KEY="your-wallet-private-key"
```

### Run Development Server
```bash
# Run migrations
npm run db:push

# Start dev server
npm run dev

# Open browser
# App: http://localhost:3000
# Database Studio: npm run db:studio
```

### Build for Production
```bash
npm run build
npm run start
```

---

## 👥 User Roles & Permissions

| Role        | View TORs | Request TOR | Create/Edit TOR | Manage Users | Verify Blockchain | Archive Records |
|-------------|-----------|-------------|-----------------|--------------|-------------------|-----------------|
| **Guest**   | ❌        | ❌          | ❌              | ❌           | ✅                | ❌              |
| **Student** | Own only  | ✅          | ❌              | ❌           | Own only          | ❌              |
| **Registrar**| ✅       | ✅          | ✅              | ❌           | ✅                | ✅              |
| **Admin**   | ✅        | ✅          | ✅              | ✅           | ✅                | ✅              |

---

## 🐛 Known Issues & Improvements

### Current Status: Production-Ready with Minor Enhancements Planned

#### ✅ What Works Perfectly
- Core CRUD functionality for all document types
- Blockchain verification and hash generation
- Role-based access control across all routes
- PDF generation and download
- User authentication and session management
- Database operations and queries
- File upload handling (successfully processes files up to 50MB+)

#### 🚧 Active Improvements (Post-Client Feedback)

**Loading State Optimization (In Progress)**
- **Issue:** During large file uploads, loading indicators don't update smoothly, potentially making users think the app has frozen
- **Reality:** Files upload and save successfully - this is a UI communication issue, not a functional problem
- **Status:** Implementing improved state management using React transitions and toast notifications
- **Technical Detail:** React state updates during long async operations need optimization
- **ETA:** Completion by [target date]

**Planned Enhancements**
- [ ] Real-time upload progress tracking (0-100% indicator)
- [ ] Multi-stage loading states (uploading → processing → complete)
- [ ] Background job processing for very large files
- [ ] Enhanced error handling with retry mechanisms
- [ ] Performance monitoring dashboard

### Lessons Learned
- **Functionality isn't enough** – Users need clear feedback during all operations
- **Production-ready means user-friendly** – Not just technically correct
- **Early user testing** – Identifies UX issues before deployment
- **State management patterns** – Critical for async operations in React

---

## 👥 Team

### Core Development Team

**Ken Jervis G. Reyes** — *Project Lead & Full-Stack Developer*  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/ken-reyes-20958227b/)  
- Led AGILE development and client engagement
- Designed and implemented database architecture (14 tables)
- Built complete backend API and authentication system
- Developed majority of frontend components and features
- Integrated all system components (frontend, backend, blockchain)

**Ronald John Requioma** — *Blockchain Developer*  
- Developed Solidity smart contracts
- Implemented Keccak-256 hashing logic
- Deployed contracts to ZkSync Sepolia
- Created blockchain integration documentation

**John Dave Justo** — *UI/UX Designer*  
- Created design system and component specifications
- Designed user flows for all role types
- Provided mockups and design feedback
- Assisted with frontend implementation

**Mark Vincent Ilagan** — *Documentation Specialist*  
- Created technical documentation
- Wrote user guides and manuals
- Maintained project documentation
- Assisted with testing and QA

### Academic Supervision
- **Client:** Cavite State University – Bacoor Branch (CAVSU)
- **Institution:** STI College Las Piñas
- **Project Duration:** January 2024 - November 2024

---

## 📄 License

This project was developed for academic and educational purposes.  
**© 2024 DocChain Development Team**  
All rights reserved.

For inquiries or collaboration:  
📧 kenreyes1234567@gmail.com  
💼 [LinkedIn](https://www.linkedin.com/in/ken-reyes-20958227b/)  
🐙 [GitHub](https://github.com/KingNoran)

---

## 🙏 Acknowledgments

Special thanks to:
- **Cavite State University** for the opportunity and client engagement
- **STI College Las Piñas** for academic guidance and support
- **ZkSync** for blockchain infrastructure
- **Neon** and **Upstash** for database and caching solutions
- **Vercel** for hosting and deployment platform

---

## 📚 Additional Resources

- [Project Documentation](docs/README.md)
- [API Documentation](docs/API.md)
- [Database Schema](docs/DATABASE.md)
- [Smart Contract Documentation](docs/BLOCKCHAIN.md)
- [User Guide](docs/USER_GUIDE.md)

---

**⭐ If this project interests you, please star the repository!**
```

---

## **🔑 KEY IMPROVEMENTS Made:**

### **1. Added Project Context (HUGE)**
- ✅ Client name (CAVSU) in prominent position
- ✅ Timeline and duration
- ✅ Your specific role clearly stated
- ✅ Production-ready validation mentioned
- ✅ Explains why deployment was paused (professionally)

### **2. Better Structure**
- ✅ Table of contents for easy navigation
- ✅ Badges showing tech stack at a glance
- ✅ Clear sections for different audiences

### **3. Showcases YOUR Work**
- ✅ "My Contributions" section highlighting what YOU built
- ✅ Percentages showing your involvement (database: 100%, backend: 90%, etc.)
- ✅ Specific technical challenges you solved
- ✅ Leadership and project management highlighted

### **4. Development Process**
- ✅ Shows AGILE methodology usage
- ✅ Client engagement details
- ✅ Sprint breakdown
- ✅ Lessons learned (shows growth mindset)

### **5. Honest About Status**
- ✅ "Known Issues & Improvements" section
- ✅ Explains loading state issue transparently
- ✅ Clarifies functionality works, UI needs polish
- ✅ Shows you're actively improving it

### **6. Better Technical Details**
- ✅ System architecture diagram
- ✅ Data flow explanation
- ✅ Security and privacy strategy
- ✅ Clear setup instructions

### **7. Visual Elements (TO ADD)**
- ⚠️ **Screenshots** - Add 4-6 key screenshots showing:
  - Dashboard
  - TOR generation form
  - Blockchain verification
  - Mobile responsive view
- ⚠️ **Demo video** (optional but powerful) - 2-minute walkthrough
- ⚠️ **Badges** - Visual indicators of tech stack

---

## **📸 Action Items for Screenshots:**

### **Create a `/screenshots` folder and add:**

1. **`dashboard.png`** - Admin dashboard showing overview
2. **`tor-generation.png`** - Form for creating records
3. **`verification.png`** - QR code and blockchain verification
4. **`mobile.png`** - Mobile responsive view
5. **`pdf-preview.png`** - Generated PDF preview
6. **`login.png`** - Authentication screen (optional)

**How to take screenshots:**
- Use browser full-screen mode
- Remove any test/dummy data
- Use consistent window size (1920x1080 recommended)
- Crop to show just the relevant interface
- Save as PNG for quality

---

## **🎥 Optional: Demo Video (20% More Impressive)**

**If you have 1-2 hours, create a simple screen recording:**
```
1. Homepage/Login (10 seconds)
2. Dashboard overview (15 seconds)
3. Creating a new TOR (20 seconds)
4. Generating PDF (15 seconds)
5. Blockchain verification (15 seconds)
6. Mobile responsive view (10 seconds)
Total: ~90 seconds
