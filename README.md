# Sandpiper Run - Unit Access Request Form

This is a dynamic, interactive web form designed for owners at Sandpiper Run in Pawleys Island, SC. It provides a digital means for owners to request and authorize unit access for vendors, contractors, or other personnel.

The form is built with HTML, Tailwind CSS for styling, and JavaScript for interactive features. It connects to a Supabase backend to store all submissions in a secure database.

![Unit Access Form Screenshot](https://i.postimg.cc/Yq5FM0C7/form-background.jpg))

---

## Features

- **Dynamic and Responsive:** The form is fully responsive and works on desktops, tablets, and mobile devices.
- **Interactive Calendars:** Custom-built date pickers for easy date selection.
- **Flexible Signature Options:**
    - **Type-to-Sign:** Type your name for a cursive signature.
    - **Draw Signature:** Use a mouse or touchscreen to draw your signature.
    - **Upload Signature:** Upload an image of your signature.
- **Auto-Formatting:** The phone number field is automatically formatted for a better user experience.
- **Database Integration:** All form submissions are securely saved to a Supabase database.
- **Success Notifications:** Users receive a confirmation modal after a successful submission.

---

## How to Use

This project is a single `index.html` file that can be hosted on any static web hosting service (like Netlify, Vercel, or GitHub Pages).

### Backend Setup (Supabase)

To enable form submissions, you must connect the form to your own Supabase project.

1.  **Create a Supabase Project:** If you haven't already, create a new project at [supabase.com](https://supabase.com).
2.  **Create a Table:** In your Supabase project's Table Editor, create a new table named `access_requests`. Add columns corresponding to the form fields (e.g., `owner_name`, `unit_number`, `date_requested`, `signature`, etc.).
3.  **Get API Credentials:**
    - Go to your project's **Settings > API**.
    - Find your **Project URL** and your **anon public key**.
4.  **Update the Code:**
    - Open the `index.html` file.
    - Find the `<script>` section at the bottom.
    - Replace the placeholder values for `SUPABASE_URL` and `SUPABASE_ANON_KEY` with your actual credentials.

```javascript
// IMPORTANT: To enable form submission, you must replace these placeholder values.
const SUPABASE_URL = 'YOUR_SUPABASE_URL';
const SUPABASE_ANON_KEY = 'YOUR_SUPABASE_ANON_KEY';
