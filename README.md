Mara Voss — Portfolio Site

A single-file HTML/CSS/JS portfolio site (no build step, no dependencies to install).

Files
index.html — the entire site (structure, styles, and content data all in one file)
Run it locally

Option A — just open it Double-click index.html. It opens in your default browser. Good enough for quick checks.

Option B — VS Code + Live Server (recommended while editing)

Open this folder in VS Code (File > Open Folder)
Install the Live Server extension (by Ritwick Dey)
Right-click index.html → Open with Live Server
Edit and save — the browser auto-refreshes
Edit the content

Everything content-related (services, projects, articles, testimonials, marquee words) lives in small JS arrays near the bottom of index.html, inside the <script> tag. Look for objects like:

js
const services = [
  { name: "SEO Strategy", desc: "..." },
  ...
];

Edit the values directly — no rebuild needed, just save and refresh.

Placeholder photography is CSS gradient blocks (.ph / .g1–.g4 classes). Replace those <div class="ph g1"></div> elements with real <img src="..."> tags once you have your own photos.

Deploy for free with GitHub Pages
Create a new GitHub repository (e.g. mara-voss-portfolio) and push this folder to it:
bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
On GitHub, go to your repo → Settings → Pages
Under Build and deployment, set Source to Deploy from a branch
Set Branch to main and folder to / (root), then Save
Wait 1–2 minutes, then your site will be live at: https://YOUR-USERNAME.github.io/YOUR-REPO/

Since the file is already named index.html, GitHub Pages will serve it automatically at the repo root — no extra config needed.

Custom domain (optional)

In the same Pages settings section, you can add a custom domain (e.g. maravoss.com) under Custom domain, then follow GitHub's instructions to point your domain's DNS at GitHub Pages.
