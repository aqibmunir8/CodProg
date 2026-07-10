
# CodProg LMS - React Capstone Project

🚀 **[View Live Demo](https://codprog.vercel.app/)**

A modern, production-ready frontend for a monetizable Learning Management System (LMS). Built as a comprehensive engineering capstone project, this application handles everything from secure user authentication and complex state management to a complete Stripe checkout workflow and video streaming.

![React](https://img.shields.io/badge/React-18.x-61DAFB?logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-5.x-646CFF?logo=vite&logoColor=white)
![Node](https://img.shields.io/badge/Node.js-18%2B-339933?logo=node.js&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-Backend-3ECF8E?logo=supabase&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-Payments-008CDD?logo=stripe&logoColor=white)

## 📌 Project Overview

This project was developed to solve real-world SaaS challenges, moving beyond basic CRUD operations to implement secure, distributed workflows. 

**Key Features:**
- **Secure Authentication & Authorization:** Handled via Supabase with protected React routes.
- **Monetization Workflow:** Fully integrated Stripe checkout for processing course purchases and managing access tiers.
- **Media Delivery:** Optimized video streaming integration for delivering course content efficiently.
- **Dynamic State Management:** Seamless synchronization between user authentication, database security policies, and UI state.

## 🛠 Tech Stack

- **Build Tool:** Vite
- **Frontend Framework:** React 18
- **Routing:** React Router DOM
- **API & Data Fetching:** Axios
- **Payments:** Stripe React / Stripe.js
- **Code Quality:** ESLint

## ⚙️ Prerequisites

Before getting started, make sure you have the following installed on your local machine:

- Node.js 18 or higher
- npm or yarn

## 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone <your-repository-url>
   cd codprog-react-project


2. **Install dependencies:**
```bash
npm install
```



## 🔐 Environment Configuration

**[Configure Supabase](https://github.com/Codprog-Technologies/Codprog-clone/tree/main/supabase)** to set up your backend database and authentication.

This project uses a dedicated configuration file named `src/constants.js` to manage environment values, API keys, and endpoint URLs securely.

1. Locate the template file `src/constants2.js` and rename it to `src/constants.js`.
2. Open `src/constants.js` and replace the placeholder values with your actual project credentials:

```javascript
// src/constants.js Example Structure
export const BASE_URL = "https://<YourProjectID>.supabase.co/";
export const SIGNUP_URL = BASE_URL + "auth/v1/signup";
export const LOGOUT_URL = BASE_URL + "auth/v1/logout";
export const LOGIN_URL = BASE_URL + "auth/v1/token?grant_type=password";
export const SUPABASE_API_KEY = "<YOUR_SUPABASE_API_KEY>";
export const GET_ALL_COURSES = BASE_URL + "rest/v1/courses?select=*";
export const STRIPE_PUBLISHABLE_KEY = "<YOUR_STRIPE_PUBLISHABLE_KEY>";

```

*(Note: Ensure `constants.js` remains in your `.gitignore` to prevent leaking secrets.)*

## 💻 Running the Development Server

Start the local development server with:

```bash
npm run dev

```

Open your browser and navigate to the local URL shown in the terminal, usually:
`http://localhost:5173`

## 🏗 Build for Production

To create an optimized production build:

```bash
npm run build

```

The compiled output will be generated in the `dist/` directory, ready for deployment.

## 📂 Project Architecture

```text
public/                  # Static assets
src/
 ├── App.jsx             # Main app component & route wrapper
 ├── main.jsx            # React entry point
 ├── constants.js        # Local config & secrets (ignored by git)
 ├── assets/             # Images, icons, and global CSS
 ├── layouts/            # Shared structural components (Navbars, Footers)
 ├── pages/              # Page-level views (Home, Course, Checkout)
 └── utils/              # Helper functions and API logic
index.html               # HTML entry point
package.json             # Scripts and dependencies
vite.config.js           # Vite build configuration

```

## 🤝 Contributing

Contributions, issues, and feature requests are welcome. If you are suggesting a major change, please open an issue first to discuss what you would like to change.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
