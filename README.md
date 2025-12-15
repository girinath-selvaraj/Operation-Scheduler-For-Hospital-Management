🏥 Operation Scheduler for Hospital Management

A Web-based Operation Theater (OT) Scheduling and Management System Technologies: HTML, CSS, JavaScript, Firebase Domain: Healthcare

--

📌 Project Overview

Healthcare organizations face challenges in efficiently managing Operating Theater (OT) schedules. Issues such as doctor availability, emergency surgeries, anesthesia team allocation, and equipment planning demand a dynamic, error-free, centralized scheduling system.

This project transforms a manual static OT schedule into a dynamic and interactive scheduler, enabling hospital administrators to manage daily OT operations easily.

The system provides interfaces for: ✔ Admin & User login ✔ Doctor management ✔ Patient management ✔ Operation scheduling ✔ Viewing past & upcoming OT activities ✔ Tracking pre- and post-operative events ✔ Attaching surgery reports ✔ Logging all activities for audit purposes
--

🎯 Problem Statement

Hospitals often use static OT scheduling methods, causing issues in:

Efficient allocation of doctors & rooms

Managing emergency or canceled procedures

Tracking pre/post-operative workflows

Resource & equipment management

Recording operation notes and reports

This project replaces static scheduling with a dynamic model that supports real-time updates and comprehensive OT activity tracking.

--

🛠️ Features / System Modules 🔐 Admin / User Login

Firebase Authentication

Admin role verification using Firestore

Secure session handling
--
👨‍⚕️ Manage Doctor Details

Add doctor

Edit doctor

Delete doctor

View doctor list

Fields include:

Doctor Name

Specialization

Experience

OT availability
--
🧑‍🦽 Manage Patient Details

Add patient details

Medical history

Surgery type

Assigned doctor

Contact information

--

🗓️ Post Operation Schedule Details

Each OT schedule includes:

Operation Date & Time

OT Number

Surgery Type

Anesthesia Type

Anesthesiologist Name

Assistant Surgeon (optional)

Nurses Involved

Pre-Operative Notes

Post-Operative Notes

Surgery Reports & Attachments

Required Drugs, Instruments, Materials

Doctor Remarks
--
📊 View OT Activity

View previous OT schedules

View upcoming scheduled procedures

Detailed activity monitoring
--
🏗️ System Architecture ├── public/ │ ├── index.html → Login Page │ ├── dashboard_admin.html │ ├── doctor.html │ ├── patient.html │ ├── schedule.html │ ├── view.html │ ├── js/ │ │ ├── firebase.js │ │ ├── dashboard.js │ │ ├── doctor.js │ │ ├── patient.js │ │ ├── schedule.js │ │ ├── logout.js │ ├── env.js → Firebase Config ├── firebase.json ├── firestore.rules ├── firestore.indexes.json ├── README.md

📡 Technology Stack Component Technology Frontend HTML, Tailwind CSS, JavaScript Backend Firebase Authentication Database Firebase Firestore Hosting Firebase Hosting Logging Custom JS-based logging (console + Firestore logs)
--
🔐 Firebase Modules Used

Firebase Auth → Email/Password Login

Firestore → Users, Doctors, Patients, Schedules

Firebase Hosting → Deployment

🧩 Code Requirements Fulfilled

✔ Modular JavaScript files ✔ Reusable functions ✔ Logging for every action ✔ Firestore-based real-time data ✔ Admin role-based routing ✔ Cloud/Local deployment support ✔ GitHub publishing

📝 Logging

Every important action is logged:

Login / Logout

Add / Edit / Delete doctor

Add / Edit / Delete patient

Creating schedule

Updating schedule

Viewing reports

Logs stored in console + Firestore (/logs/{docId})
--
🚀 How to Run the Project Locally 1️⃣ Clone the repository git clone https://github.com/your-username/operation-scheduler.git cd operation-scheduler

2️⃣ Add Firebase Config

Create file:

public/env.js

Paste:

export const firebaseConfig = { apiKey: "your-key", authDomain: "your-domain", projectId: "your-id", storageBucket: "your-bucket", messagingSenderId: "your-sender", appId: "your-app-id" };

3️⃣ Run Firebase Hosting

Install Firebase CLI:

npm install -g firebase-tools

Login:

firebase login

Serve locally:

firebase serve

It runs at: 👉 http://localhost:5000

🌐 Deployment (Firebase Hosting)

firebase deploy

Your live website will go online instantly.
--
🧪 Testing

Covered areas:

Login validation

Admin role check

Firestore CRUD operations

Schedule conflict handling

UI responsiveness
