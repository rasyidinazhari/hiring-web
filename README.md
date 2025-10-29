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
| **Hosting** | Vercel / Supabase Edge                                            | Serverless-friendly deployment ready              |

## How to Run Locally
1️⃣ Clone this repository
git clone https://github.com/<your-username>/web-hiring.git
cd web-hiring

2️⃣ Install dependencies

Make sure you’re using Node.js ≥ 18.17 (recommended Node 20 or 22 LTS).

npm install

3️⃣ Set up environment variables

Create a .env.local file in the project root and fill with your Supabase credentials:

NEXT_PUBLIC_SUPABASE_URL=<your-supabase-url>
NEXT_PUBLIC_SUPABASE_ANON_KEY=<your-supabase-anon-key>
NEXT_PUBLIC_BASE_URL=http://localhost:3000

4️⃣ Prepare local model for hand tracking

Copy the hand landmark model to your public directory:

mkdir -p public/models
cp node_modules/@mediapipe/tasks-vision/wasm/hand_landmarker.task public/models/


Or download it manually from:

https://cdn.jsdelivr.net/npm/@mediapipe/tasks-vision@latest/wasm/hand_landmarker.task

5️⃣ Run the development server
npm run dev


Then open http://localhost:3000
 to see your app live.

🖐️ Gesture Capture Demo

When on the /apply/[slug] page:

Allow camera permission.

Show three fingers in front of the webcam.

The system will automatically capture your photo and attach it to the application form.

📦 Folder Structure
web-hiring/
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   ├── jobs/
│   │   │   │   ├── route.ts
│   │   │   │   ├── [slug]/route.ts
│   │   │   │   └── [id]/candidates/route.ts
│   │   ├── apply/[slug]/page.tsx
│   │   ├── admin/jobs/page.tsx
│   │   └── layout.tsx
│   ├── components/ui/
│   │   ├── DynamicForm.tsx
│   │   └── WebcamCapture.tsx
│   └── lib/supabase.ts
├── public/models/hand_landmarker.task
├── tailwind.config.js
├── postcss.config.js
├── package.json
└── README.md

⚙️ Troubleshooting

Blank page: Check .env.local and ensure Supabase URL & key are valid.

500 on /api/jobs: Confirm table jobs exists with columns slug, title, status, etc.

Gesture not working: Ensure webcam permission is granted and hand_landmarker.task file is available in /public/models.

🧑‍💻 Author

Wisnu — Fullstack Developer | ML & Backend Engineer
📍 Indonesia
🌐 LinkedIn
 • GitHub
 • MersifLab
