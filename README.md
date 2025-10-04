# DailySpark ✨

Welcome to **DailySpark**, your lightweight, mobile-first website for daily motivation and knowledge challenges.

This project serves a daily inspirational quote (a mix of Islamic and universal wisdom) and a general knowledge quiz question. It's built with a simple and robust stack, designed to be fast, free to host, and easy to manage.



## Features

-   **Daily Content:** A new quote and quiz are automatically served every day.
-   **Mixed Content:** A curated mix of Islamic and universal quotes and quizzes.
-   **Shareable:** Easily share the daily inspiration on WhatsApp, Facebook, or by copying a link.
-   **History Navigation:** Browse through previous days' content.
-   **Admin Panel:** A simple, password-protected admin panel to add and manage quotes and quizzes.
-   **Lightweight & Fast:** Built with vanilla HTML, CSS, and JavaScript. No heavy frameworks.
-   **No Database Required:** All content is stored in simple JSON files.
-   **Deploy Anywhere:** Ready to be deployed on free services like Render, Vercel, or Netlify.

## Tech Stack

-   **Backend:** Node.js + Express
-   **Frontend:** HTML5, CSS3 (Plain), JavaScript (Vanilla)
-   **Data Storage:** JSON files
-   **Dependencies:** Express, Helmet, CORS, DotEnv

## Getting Started

Follow these instructions to get the project running on your local machine.

### Prerequisites

-   Node.js (v16 or later)
-   npm (usually comes with Node.js)

### Local Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    cd DailySpark
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Set up environment variables:**
    Copy the example `.env.example` file to a new file named `.env`.
    ```bash
    cp .env.example .env
    ```
    The `.env` file contains the default admin credentials. You can change them if you wish.
    ```
    ADMIN_USER=WarriorSamim3
    ADMIN_PASS=WarriorSamim
    ```

4.  **Run the development server:**
    This command uses `nodemon` to automatically restart the server when you make changes.
    ```bash
    npm run dev
    ```

5.  **Run the production server:**
    For a normal start, use:
    ```bash
    npm start
    ```

The application will be running at `http://localhost:3000`.

## Admin Panel

To manage the content:

1.  Navigate to `http://localhost:3000/admin/admin.html`.
2.  Log in using the credentials from your `.env` file.
3.  You can now add new quotes and quizzes. The lists of existing content will appear on the same page.

## Deployment

This project is ready for deployment on any platform that supports Node.js. Here are the instructions for **Render (a free hosting service)**.

1.  **Sign up for a Render account** and connect it to your GitHub account.
2.  **Create a new "Web Service"** on the Render dashboard.
3.  **Select your repository** for DailySpark.
4.  **Configure the settings:**
    -   **Name:** `DailySpark` (or your choice)
    -   **Region:** Choose a region near you.
    -   **Branch:** `main` (or your primary branch)
    -   **Root Directory:** Leave it blank (if your code is at the root).
    -   **Runtime:** `Node`
    -   **Build Command:** `npm install`
    -   **Start Command:** `npm start`
5.  **Add Environment Variables:**
    -   Go to the "Environment" tab for your new web service.
    -   Add two "Secret Files".
    -   Add a key-value pair for `ADMIN_USER` and `ADMIN_PASS` with the credentials you want to use in production.
6.  **Click "Create Web Service"**.

Render will automatically deploy your application. After the first build, any new `git push` to your main branch will trigger a new deployment. Your site will be live at the URL provided by Render (e.g., `dailyspark.onrender.com`).

**Note on File-Based Storage:** Free hosting services like Render have an ephemeral filesystem. This means any changes you make to the `quotes.json` and `quizzes.json` files via the admin panel will be **lost** when the server restarts or redeploys. For persistent storage, you should commit your updated JSON files to your Git repository.

## Customization

-   **Images:** Replace the placeholder images in `/public/images/` (`logo.png`, `bg1.jpg`, `bg2.jpg`) with your own. Keep them optimized for web use.
-   **Styling:** Modify `/public/style.css` to change the look and feel. CSS variables at the top of the file make it easy to change the color scheme.
-   **Content:** Add more quotes and quizzes to `/data/quotes.json` and `/data/quizzes.json`. Make sure to maintain the JSON structure.

---
