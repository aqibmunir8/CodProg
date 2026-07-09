# CodProg React Project

A modern Vite + React frontend for a course-based web application with pages for browsing courses, managing student progress, authentication, checkout, and payment flow.

![React](https://img.shields.io/badge/React-18.x-61DAFB?logo=react)
![Vite](https://img.shields.io/badge/Vite-5.x-646CFF?logo=vite)
![Node](https://img.shields.io/badge/Node.js-18%2B-339933?logo=node.js)

## Tech Stack

- Vite
- React 18
- React Router DOM
- Axios
- Stripe React/Stripe.js
- ESLint

## Prerequisites

Before getting started, make sure you have the following installed:

- Node.js 18 or higher
- npm or yarn

## Installation

1. Clone the repository:

   ```bash
   git clone <your-repository-url>
   cd codprog-react-project
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Setup & Environment

This project uses a dedicated configuration file named `src/constants.js` for local environment values and API credentials.

Follow these steps:

1- create src/constants.js and see the expected structure. It should look like this:

```bash
export const BASE_URL = "https://(YourProjectID).supabase.co/";
export const SIGNUP_URL = BASE_URL + "auth/v1/signup";
export const LOGOUT_URL = BASE_URL + "auth/v1/logout";
export const LOGIN_URL = BASE_URL + "auth/v1/token?grant_type=password";
export const SUPABASE_API_KEY = "SUPABASEAPIKEY";
export const GET_ALL_COURSES = BASE_URL + "rest/v1/courses?select=*";
export const STRIPE_PUBLISHABLE_KEY = "STRIPE-PUBLISHIBLE-KEY";
```

2- Open src/constants.js and replace the placeholder values (like (YourProjectID), SUPABASEAPIKEY, and STRIPE-PUBLISHIBLE-KEY) with your actual project credentials.

> or there is a file name src/constants2.js rename to constants.js and put your values.

## Running the Development Server

Start the local development server with:

```bash
npm run dev
```

Then open the local URL shown in the terminal, usually:

```text
http://localhost:5173
```

## Build for Production

To create a production build:

```bash
npm run build
```

## Project Structure

```text
public/                 # Static assets
src/
  App.jsx                # Main app component
  main.jsx               # React entry point
  constants.js           # Local config template (ignored by git)
  constants2.js         # Local secrets/configuration file (ignored by git)
  assets/                # Images and static files
  layouts/               # Shared layout components
  pages/                 # Page-level views and routes
  utils/                 # Helper functions and utilities
index.html              # HTML entry point
package.json            # Scripts and dependencies
vite.config.js         # Vite configuration
```

## Contributing

Contributions are welcome. If you make changes, please open a pull request with a clear description of what was updated.
