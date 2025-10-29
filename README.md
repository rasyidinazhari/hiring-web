# hiring-web
this is prototype for hiring web-app for company who want to recruit talent effectively

## Project Overview
This project is a modern job hiring platform built with Next.js 16 and Supabase, featuring an AI-powered gesture capture system using MediaPipe Tasks Vision.

The platform allows administrators to manage job postings, while applicants can apply directly through a dynamic form that automatically adjusts per job configuration.
Additionally, the system uses real-time hand gesture recognition — candidates can take a photo automatically by showing 3 fingers, enhancing user interaction and ensuring a live applicant presence.

## Key Features
- Dynamic job listings with CRUD operations via Supabase.
- page for each job detail, loaded dynamically by slug.
- Auto-generated forms based on database configuration (job_configs).
- Automatic webcam photo capture triggered by hand gesture detection.
- Clean and responsive UI with TailwindCSS integration.
- Secure API routes.

## Tech Stack
| Layer                  | Technology                                                        | Description                                       |
| ---------------------- | ----------------------------------------------------------------- | ------------------------------------------------- |
| **Frontend**           | [Next.js 16 (App Router)](https://nextjs.org/)                    | React framework with server components            |
| **Styling**            | [Tailwind CSS](https://tailwindcss.com/)                          | Utility-first CSS for rapid UI development        |
| **Database**           | [Supabase](https://supabase.com/)                                 | PostgreSQL backend with REST API                  |
| **AI / ML**            | [MediaPipe Tasks Vision](https://developers.google.com/mediapipe) | Real-time hand landmark detection                 |
| **Language**           | TypeScript                                                        | Type-safe development for both frontend & backend |
| **Build Tools**        | PostCSS, LightningCSS                                             | Modern build pipeline optimized for Next.js       |
| **Hosting (optional)** | Vercel / Supabase Edge                                            | Serverless-friendly deployment ready              |
