<div align="center">

# Hey, I'm Bennett Daniel 👋

**Mechanical Engineer** · Control Systems · Vehicle Dynamics · Autonomous Vehicle Technologies

[![Portfolio](https://img.shields.io/badge/Portfolio-bjd273.github.io-000?style=for-the-badge&logo=githubpages&logoColor=white)](https://bjd273.github.io/Portfolio/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/bennettdaniel)
[![Email](https://img.shields.io/badge/Email-bjd273@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:bjd273@gmail.com)

</div>

---

Mechanical engineer with a Master's from UT Dallas, focused on **control systems, vehicle dynamics, and autonomous driving**. I've designed an electronic stability controller that cut brake-system weight by **4 kg**, built cost-based path-planning algorithms in **ROS2** for autonomous navigation, and led cross-functional teams from modeling and simulation through real-world validation. Currently teaching robotics and controls at the high-school level while building toward my next role accelerating autonomous vehicle development.

## 🛠️ Skills

<div align="center">

![MATLAB](https://img.shields.io/badge/MATLAB-0076A8?style=flat-square&logo=mathworks&logoColor=white)
![Simulink](https://img.shields.io/badge/Simulink-black?style=flat-square)
![ROS2](https://img.shields.io/badge/ROS2-22314E?style=flat-square&logo=ros&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![SolidWorks](https://img.shields.io/badge/SolidWorks-E4002B?style=flat-square)
![ANSYS](https://img.shields.io/badge/ANSYS-FFB71B?style=flat-square&logoColor=black)
![CarMaker](https://img.shields.io/badge/CarMaker-black?style=flat-square)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

</div>

| | |
|---|---|
| **Programming** | Python, C++, ROS2, Linux, Git, Jira |
| **Machine Learning & CV** | YOLO, CNN, Object Detection & Classification, Reinforcement Learning, Deep Learning |
| **Technical Tools** | MATLAB, Simulink, Simscape, OptimumDynamics, CarMaker, Parametric Creo, ANSYS, SolidWorks |
| **Automotive Systems** | Tire Force Modeling, Suspension Mechanics, Brake System Design, Path Planning, ADAS |
| **Control & Estimation** | PID Control, Model Predictive Control, Optimal Control, Observer Design, Differential Flatness |

---

## 💼 Work Experience

**CTE Teacher** — Dallas ISD, Barack Obama Male Leadership Academy · *Sep 2025 – Present*
Teach programming, robotics control systems, and applied engineering; guide project-based learning with SolidWorks CAD and rapid prototyping, and apply PID/MPC concepts in hands-on modules that feed regional robotics competitions.

**Master's Thesis Student** — NOVA, UT Dallas Premier Autonomous Driving Group · *Aug 2023 – May 2025*
Researched and benchmarked cost-based path-planning algorithms in ROS2, integrating the top-performing method into the open-source Navigator stack. Validated performance in CARLA across urban and highway SIL scenarios, and applied optimal/PID control in Simscape to improve trajectory efficiency and obstacle avoidance.

**Vehicle Dynamics Lead Engineer** — Comet Solar Racing · *Jan 2024 – May 2025*
Designed and validated an Electronic Stability Controller in MATLAB/CarMaker, improving lateral stability during cornering. Built a full-lap simulator with PID-based closed-loop control in Simulink, redesigned the brake system layout for a **4 kg** weight reduction, and engineered the wheel hub and front suspension (SolidWorks + ANSYS FEA).

**Research Assistant** — Automotive Research Cell · *Sep 2022 – May 2023*
Co-authored research on Smart Accident Fatality Reduction (SAFR), building hardware in SolidWorks and classification algorithms with reinforcement learning and ROS2. Designed a vehicle-mounted emergency response device integrating ROS2 communication and differential-flatness control.

**Deep Learning Intern** — Artenal · *Aug 2022 – Nov 2022*
Trained YOLO and SSD models in PyTorch on 1,000+ annotated images and deployed them via ROS2 for real-time waste classification, fine-tuning to **95%** classification accuracy.

---

## 🚗 Engineering Projects

- **Robust Control of Active Suspension System** — Modeled an active suspension system in MATLAB with H2 and H∞ control strategies, injecting disturbances and uncertainties to validate robustness. Achieved **93% robust performance** across 3 driving modes, simulated in Simulink.
- **Model-Free Longitudinal Speed Controller** — Designed a model-free speed controller for autonomous vehicles in MATLAB/Simulink, analyzing Tire-Road Friction Coefficient (TRFC) and applying torque constraints and Algebraically Estimated Derivative (ADE) techniques for noise-resistant speed tracking.
- **Active Bus Footboard Avoidance System (ABFAS)** — Designed a safety system for Indian public buses in SolidWorks that detects open doors and footboard occupancy via reed switches and force sensors, and locks the accelerator pedal under unsafe conditions. Validated the locking mechanism with ANSYS material analysis.

> The vehicle-dynamics and controls work above is also demonstrated live, in-browser, in the [Portfolio](#-portfolio--interactive-control-systems--vehicle-dynamics-simulations) project below — including a from-scratch active-suspension LQR compensator.

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

### 🎡 [Portfolio](https://bjd273.github.io/Portfolio/) — Interactive Control Systems & Vehicle Dynamics Simulations

> Graduate control-systems and vehicle-dynamics coursework ported from MATLAB/Simulink into live, in-browser simulations — no screenshots, no canned animations.

<details>
<summary><b>🔍 Click to expand full breakdown</b></summary>

<br>

**The Problem:** A static portfolio site or a PDF of coursework doesn't do justice to control theory and vehicle dynamics work — the whole point of the math is *how the system behaves over time*. I wanted a way to show that behavior directly, running live, rather than describing it.

**The Solution:** A home page built around a 3D sphere of project cards, rendered on a plain 2D canvas — no WebGL library, no frameworks, no build step. Every card runs its project's actual simulation continuously in the background; selecting a card rotates it to face the viewer and opens its write-up. Only front-facing cards are rendered and stepped, so the cost stays flat no matter how many projects are on the sphere.

#### 📦 The seven simulations

All ported from real MATLAB/Simulink coursework, each solving and rendering its own physics or control problem live:

- **Double Pendulum** — Euler–Lagrange equations of motion for two coupled rods, integrated with a 4th-order Runge–Kutta solver. Two pendulums run identical equations from starting angles 0.05° apart, enough to make them diverge completely within seconds — chaos, visualized.
- **Robot Navigation** — A 41×41 grid where each move can slip sideways with a probability that depends on the previous move. The optimal policy is solved by backward induction over the full state space, then verified live by continuous Monte Carlo rollouts.
- **Adaptive Cruise Control** — A PID spacing controller proven against every vehicle within ±7% mass and ±30% drag of nominal, driven by the real recorded lead-vehicle speed trace from the original test.
- **14-DOF Vehicle Model** — A car corners on its actual Magic Formula tire curve — real mass, inertia, and geometry pulled from the reference model — until the front tires visibly run out of grip.
- **Active Suspension** — A quarter-car LQR compensator with its Riccati equation solved and verified live in-browser, trading ride comfort for control on a single dial.
- **Aircraft Pitch Control** — A lightly-damped short-period pitch response tracking a real ±15°/s command through a real ±20° elevator limit, held by LQR with integral action.
- **Solar Racing Vehicle** — A 255 kg solar racer's launch, genuinely traction-limited before it becomes power-limited, integrated live from rest rather than estimated from a single terminal value.

#### ⚙️ Tech

`Plain HTML/CSS/JavaScript` · `Canvas 2D` (custom 3D projection, rotation, depth-sorting, hit-testing) · `Numerical methods` (RK4 integration, backward induction, Riccati/LQR solvers, Magic Formula tire model)

</details>

---

## 🎓 Education

| | |
|---|---|
| **M.S., Mechanical Engineering** | University of Texas at Dallas · 2023 – 2025 · Richardson, TX |
| **B.E., Automobile Engineering** | Anna University · 2019 – 2023 · Chennai, India |

## 📄 Publications

Joseph, D.B. et al. [**Smart Accident Fatality Reduction (SAFR) System.**](https://link.springer.com/chapter/10.1007/978-981-19-9379-4_38) (2023). In: *Third Congress on Intelligent Systems, CIS 2022*. Lecture Notes in Networks and Systems, vol 613. Springer, Singapore.

## 🏆 Achievements

- **Budding Bright Engineering Award** — Exceptional academic performance
- **Intramural Innovative Projects Funding Recipient**
- **Multiple Hackathon Winner**

---

## 🧩 What I Bring

| | |
|---|---|
| **Full-Stack Ownership** | From MATLAB/Simulink models to ROS2 nodes to production web apps, I design, build, and validate the whole system — no hand-offs needed. |
| **Simulation-to-Reality Pipeline** | I model in MATLAB/Simulink, validate in CarMaker/CARLA, then fabricate and test the physical result — control theory that survives contact with hardware. |
| **Production Mindset** | These aren't tutorial projects — they handle real users, real auth, real data, real vehicles, and real edge cases. |
| **AI Integration** | I build AI (ROS2 perception, YOLO classification, Claude tool-use) into products as a functional enhancement, not a gimmick. |
| **Ship Fast, Iterate** | From a 4 kg brake-system redesign to a deployed classroom platform, I bias toward getting real work in front of real users. |

---

<div align="center">

*I'm looking for my next opportunity to accelerate autonomous vehicle development. Let's talk.*

[![Email](https://img.shields.io/badge/bjd273@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:bjd273@gmail.com)
[![Portfolio](https://img.shields.io/badge/Full_Portfolio-000?style=for-the-badge&logo=githubpages&logoColor=white)](https://bjd273.github.io/Portfolio/)

</div>
