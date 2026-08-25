<div align="center">

# Hey, I'm Bennett Daniel 👋

**Mechatronics Engineer** · Building production apps that solve real problems for real people

[![Portfolio](https://img.shields.io/badge/Portfolio-bennettdaniel.notion.site-000?style=for-the-badge&logo=notion&logoColor=white)](https://bennettdaniel.notion.site/Hello-I-m-Bennett-Daniel-15b209d3c94a805f941eea5905d967ae)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/bennettdaniel)
[![Email](https://img.shields.io/badge/Email-bjd273@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:bjd273@gmail.com)

</div>

---

I build **full-stack web applications** from the ground up — from database schema design to polished, responsive UIs. Every project below is **deployed, in active use**, and built to handle the messy realities of actual users. I care about clean architecture, thoughtful UX, and shipping things that work.

## 🛠️ Tech Stack

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js_16-000?style=flat-square&logo=next.js&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Google APIs](https://img.shields.io/badge/Google_APIs-4285F4?style=flat-square&logo=google&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000?style=flat-square&logo=vercel&logoColor=white)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?style=flat-square&logo=framer&logoColor=white)
![Anthropic](https://img.shields.io/badge/Claude_API-191919?style=flat-square&logo=anthropic&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)

</div>

---

## 📦 Featured Projects

### 🏫 [Robotics Class Portal](https://themissioncontrol.vercel.app/) — Full-Stack Classroom Management Platform

> **Three apps in one** — a public-facing site, student portal, and teacher admin hub — all powered by Google Sheets as the database.

<details>
<summary><b>🔍 Click to expand full breakdown</b></summary>

<br>

**The Problem:** As a teacher at Barack Obama Male Leadership Academy, I needed a single platform to run my Robotics, Programming, and Technology Applications classes — handling everything from video lessons to grades to live classroom tools. Existing LMS platforms were too rigid, too expensive, or couldn't do what I needed.

**The Solution:** I designed and built a full-stack web app with **three distinct experiences** served from one codebase:

| Portal | Route | Auth | Purpose |
|--------|-------|------|---------|
| **Public Site** | `/` | None | Announcements, weekly updates, calendar, parent mailing list |
| **Student Portal** | `/dashboard` | Google OAuth | Agenda, tracked video lessons, grades, assignments, quizzes, trivia, portfolio |
| **Teacher Admin** | `/admin` | Google OAuth (role-gated) | Roster, attendance, gradebook, video management, exit tickets, team tower |

#### 🏗️ Architecture Highlights

- **Zero-database design** — Google Sheets is the database, Google Drive stores files. All API calls run server-side through a service account. This means any teacher can fork the repo, connect their Google account, and have their own isolated data environment.
- **Smart video tracking** — YouTube videos play through the IFrame API; the app counts *actual seconds played* (skipping ahead doesn't count). At 80% playback the video is marked as watched. Teachers get a per-period who-watched-what report.
- **AI command palette ("Jarvis")** — Press `Cmd+K` anywhere in the admin panel and type natural language commands like *"give team nova 5 points for the lab"* or *"start a 3 minute timer for station 2"*. Powered by **Claude's tool-use / function-calling API** — the AI picks the right function, extracts parameters from natural language, and executes actions instantly. Built with `cmdk`.
- **Live classroom tools** — Timer, random student selector, noise level meter, morning music player, interactive whiteboard, and slide presenter — all accessible from `/classroom`.
- **Role-based access control** — Student access is request-based: students sign in and submit a request; the teacher approves from the admin panel. Role determined by comparing Google email against environment config.

#### ⚙️ Tech

`Next.js 16 (App Router, Turbopack)` · `React 19` · `TypeScript` · `Tailwind CSS 4` · `NextAuth v5` · `googleapis (Sheets + Drive)` · `Anthropic Claude API` · `cmdk` · `Zustand` · `Recharts` · `Zod` · `Vercel`

#### 📊 Scale

**~9,900 lines of TypeScript** across **97 files** — API routes, server actions, 10+ admin pages, live classroom tools, student dashboard, and public site.

</details>

---

### ⛪ [Restore Ministries](https://restoreministries.vercel.app/) — Ministry Website & Content Platform

> A modern, scroll-animated website with a full CMS, member authentication, and media management — built for a ministry to manage sermons, blog posts, podcasts, and worship content.

<details>
<summary><b>🔍 Click to expand full breakdown</b></summary>

<br>

**The Problem:** Restore Ministries needed a website that wasn't just a static landing page — it needed to be a living content hub where admins could publish blog posts, manage sermon/podcast archives, upload worship videos, and offer members exclusive resources, all without touching code.

**The Solution:** A fully custom React SPA with Supabase as the backend, featuring a scroll-driven cinematic homepage, role-based dashboards, and a complete admin CMS.

#### 🏗️ Architecture Highlights

- **Cinematic scrollytelling homepage** — Scroll-linked parallax animations built with Framer Motion. Four narrative sections fade in/out based on scroll position, layered over a fixed canvas background. Smooth, performant, and visually striking.
- **Full Supabase backend** — PostgreSQL database with Row-Level Security (RLS) policies for every table. Separate tables for profiles, blog posts, sermons, and videos — each with granular access control.
- **Role-based access** — Admin vs. member roles with different dashboards. Admins get a full CMS for managing all content; members get curated access to resources and notes.
- **Content management** — Blog with slug-based routing, rich text content, featured images. Sermon/podcast archive with YouTube embeds and PDF downloads. Worship video feed.
- **Auth flows** — Supabase Auth with email/password, password recovery with deep-link token handling, and automatic profile creation via database triggers.

#### ⚙️ Tech

`React 18` · `TypeScript` · `Vite` · `Tailwind CSS` · `Supabase (Auth + PostgreSQL + Storage)` · `Framer Motion` · `React Router v7` · `Lucide Icons` · `Vercel`

#### 📊 Scale

**~5,000 lines of TypeScript** across **18 files** — 14 page-level components, Supabase client library, scroll animation system, and routing layer.

</details>

---

## 🧩 What I Bring

| | |
|---|---|
| **Full-Stack Ownership** | I design the database schema, build the API layer, and ship the UI. No hand-offs needed. |
| **Production Mindset** | These aren't tutorial projects — they handle real users, real auth, real data, and real edge cases. |
| **Pragmatic Architecture** | Using Google Sheets as a database sounds unconventional until you realize it gives every teacher an admin panel they already know how to use. I pick the right tool for the problem. |
| **AI Integration** | I build AI into products as a UX enhancement (Jarvis command palette), not as a gimmick. |
| **Ship Fast, Iterate** | Both projects went from zero to deployed and in active use. I bias toward getting it in front of users. |

---

<div align="center">

*I'm looking for my next opportunity to build impactful software. Let's talk.*

[![Email](https://img.shields.io/badge/bjd273@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:bjd273@gmail.com)
[![Portfolio](https://img.shields.io/badge/Full_Portfolio-000?style=for-the-badge&logo=notion&logoColor=white)](https://bennettdaniel.notion.site/Hello-I-m-Bennett-Daniel-15b209d3c94a805f941eea5905d967ae)

</div>

