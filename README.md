# AramSpace - Online Therapist Booking & Clinic Management SaaS

**🔗 Live Demo:** [Insert Your Live URL Here - e.g., https://aramspace.com]

> **🔒 Proprietary Software Disclaimer**
> This repository serves as an architectural showcase and technical portfolio piece. The actual source code is proprietary and closed-source, belonging to the respective company. Therefore, no source code is published in this repository. 

AramSpace is a modern, full-featured scheduling and clinic management platform built specifically for therapists and mental health professionals. Designed for high performance and seamless user experience, it handles complex appointment scheduling, secure authentication, patient management, and analytics.

## 📸 Project Previews
*(The system UI and features are demonstrated in the repository assets)*

## 🎯 Project Overview & Business Value
This platform serves as a complete B2B/B2C solution, eliminating the friction of manual appointment booking.
* **For Patients:** Offers an intuitive interface to browse therapists, view real-time availability, and securely book sessions.
* **For Therapists/Admins:** Provides a comprehensive dashboard with advanced calendar management, patient records (PDF exports), secure document uploads, and interactive data visualization (charts).
* **Enterprise Ready:** Containerized via Docker and deployed on Microsoft Azure infrastructure for maximum scalability and reliability.

## 🏛 Technical Architecture & Tech Stack

The application is built on the cutting-edge React ecosystem, utilizing modern server-side rendering and static generation techniques.

### Frontend & Core App
* **Framework:** Next.js 15.5 (App Router with Turbopack for ultra-fast compilation)
* **UI & Styling:** React 18, Bootstrap 5, React Select, React Toastify
* **State & Authentication:** NextAuth (Secure user sessions)
* **PWA Support:** `next-pwa` (Allows installation on mobile devices)

### Advanced Features & Libraries
* **Complex Scheduling:** `@fullcalendar/react` (Day/Time Grid), `react-multi-date-picker`, `react-datepicker`
* **Rich Text Editing:** `@ckeditor/ckeditor5-react`
* **Data Visualization & Analytics:** Recharts, `react-circular-progressbar`, D3
* **File Management & Export:** `react-dropzone` (file uploads), `html2pdf.js` (invoice/report generation)
* **Security & Anti-Spam:** Cloudflare Turnstile integration (`@marsidev/react-turnstile`)
* **Mapping:** `react-simple-maps`

## 🐳 Docker Containerization & Azure Deployment
*(Architectural Overview of the Deployment Process)*

This project is fully configured for production deployment using Docker and Azure Container Registry (ACR).

### 1. Multi-Stage Docker Build
We utilize a multi-stage `Dockerfile` to ensure the final image is minimal, secure, and optimized for Node.js production environments.

### 2. Azure Container Registry (ACR) Deployment
* The local image is tagged and authenticated via Azure CLI.
* Pushed securely to the remote Azure registry.
* Provisioned and deployed directly to Azure App Service / AKS environments.
