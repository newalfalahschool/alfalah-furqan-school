# Alfalah Furqan High School — Website Starter

A responsive school website project for Visual Studio Code, with English / Dari / Pashto interface, school gallery, video area, admission enquiry form, teacher job application form and a demo admin panel.

## Important truth about this version
This project is complete as a **front-end website demo**. The gallery uploads and form records are stored in the current browser using `localStorage`. They do **not** automatically appear on another computer and forms are **not sent** to the school. The demo admin password is `admin123`; it is not secure enough for a public production website. Do not publish this demo admin password or collect real sensitive data with it.

For a genuinely live multi-user site, connect a backend such as Supabase, configure database tables, private admin authentication, file storage policies, spam protection and deploy the site. Never put a Supabase `service_role` key in browser JavaScript.

## Run in VS Code
1. Extract the ZIP to a normal folder, for example `Desktop/Alfalah_Furqan_Professional_Website`.
2. Open VS Code → **File → Open Folder** → choose that extracted folder.
3. Install the **Live Server** extension if needed.
4. Right-click `index.html` → **Open with Live Server**.
5. The browser should open the site. You can also open `index.html` directly, but Live Server is recommended.

## Replace school pictures
Place your own pictures in `assets/images/` and use these exact filenames:
- `hero-school.jpg` — wide hero/banner photo (recommended 1800×1000 or larger)
- `school-campus.jpg` — school building / campus
- `students-1.jpg` — students photo
- `teachers-1.jpg` — teachers photo
- `school-activity.jpg` — school activity photo
- `school-logo.svg` — the included starter logo; replace with your logo if desired

The page has built-in placeholder images if the JPG photos are missing. Use JPG or update the corresponding paths in `index.html`. Please only publish photos when you have permission, especially for students.

## Add gallery photos and videos
- Scroll to **Moments worth remembering** and choose **Add photos (Admin)**.
- Choose video files in the video section with **Add a video (Admin)**.
- Current browser demo accepts image/video files up to 8 MB each. Videos are particularly large, so compress them first.
- The demo browser storage has limits; for a real website, use hosted storage (e.g. Supabase Storage) rather than browser storage.

## Demo admin panel
- Click **Admin panel** in the footer.
- Demo password: `admin123`
- The panel displays enquiry / job application records saved in this browser, can export records as JSON, and can clear locally uploaded media.
- This is a demo convenience, **not real security**. Anyone who can inspect the JavaScript can see the password. Do not use it for private or production administration.

## Forms and production launch
The forms currently save demo submissions in the browser only. Before using this for real admissions or recruitment:
1. Set up Supabase project and tables for admission enquiries, job applications and website content.
2. Add Supabase Auth for administrators, enable row-level security (RLS), and configure policies carefully.
3. Use Supabase Storage with upload size/type limits for photos and videos.
4. Connect form submissions to the database and show success only after the server confirms the save.
5. Add spam protection, privacy notice, backups and a way to securely review/delete records.
6. Test with real devices and a test account, then deploy to HTTPS hosting.
7. Update the school phone, address, notices, calendar, and legal/privacy wording before launch.

## Contact information included
- School: Alfalah Furqan High School
- Location: Mazar-e-Sharif, Afghanistan
- Phone: 0796677000

## Project files
- `index.html` — page sections and forms
- `styles.css` — responsive design
- `app.js` — language switch, browser-demo uploads, forms and demo admin panel
- `assets/images/` — logo and fallback illustrations
- `assets/videos/` — place local video files here if you later wire them into the page
