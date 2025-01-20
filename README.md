# Project: Course Helper Application

## Overview
This is a web application for managing courses, including features to create, update, and delete course entries. The app is built with HTML , CSS , Javascript , React.js, Next.js in Node.js , Express.js ,
React, Supabase, Vercel and utilizes TypeScript for type safety.

## Features
- **Course Management**: Create, edit, and delete courses.
- **User Authentication**: Integration with Supabase authentication for secure user management.
- **Responsive Design**: TailwindCSS is used to ensure the app looks great on all devices.

## Project Structure
The project follows a modular structure for better scalability and maintainability.

### File Structure
```
.
├── src
│   ├── components
│   │   ├── CourseCard.tsx
│   │   ├── CourseForm.tsx
│   ├── lib
│   ├── pages
│   │   ├── Login.tsx
│   │   ├── SignUp.tsx
│   │   ├── Courses.tsx
│   ├── types
│   ├── App.tsx
│   ├── index.css
│   ├── main.tsx
│   ├── vite-env.d.ts
├── supabase
│   ├── migrations
│   │   ├── 20250118152121_tight_cottage.sql
├── .env
├── .gitignore
├── eslint.config.js
├── index.html
├── package-lock.json
├── package.json
├── postcss.config.js
├── tailwind.config.js
├── tsconfig.app.json
├── tsconfig.json
├── tsconfig.node.json
├── vite.config.ts
```

## Key Components

### `CourseCard.tsx`
- A functional component that displays course details.
- Props:
  - `course`: Contains the course information.
  - `onEdit`: A callback for editing a course.
  - `onDelete`: A callback for deleting a course.

### `20250118152121_tight_cottage.sql`
- SQL migration file to create the `courses` table in Supabase.
- Schema:
  - `id`: UUID (Primary Key)
  - `name`: Text (Required)
  - `code`: Text (Required)
  - `credits`: Integer (Required)
  - `timings`: Text (Required)
  - `description`: Text (Required)
  - `user_id`: UUID (References `auth.users`)
  - `created_at`: Timestamp with time zone
- Security policies:
  - Users can read, insert, update, and delete their own courses.

### `App.tsx`
- The entry point for the application.
- Defines routes using React Router:
  - `/`: Login page.
  - `/signup`: Sign-up page.
  - `/courses`: Courses management page.
  - `*`: Redirects to `/`.

## Setup Instructions

### Prerequisites
- Node.js (v16 or later)
- Supabase account

### Steps
1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up the environment variables:
   - Create a `.env` file in the root directory.
   - Add the following variables:
     ```env
     VITE_SUPABASE_URL=<your_supabase_url>
     VITE_SUPABASE_ANON_KEY=<your_supabase_anon_key>
     ```

4. Run the application:
   ```bash
   npm run dev
   ```

5. Open the app in your browser:
   ```

   http://localhost:3000
   ```

## Technologies Used
- **React**: Frontend library.
- **TypeScript**: Type safety.
- **Supabase**: Backend as a Service (BaaS) for authentication and database.
- **TailwindCSS**: CSS framework for styling.
- **Vite**: Fast build tool.



