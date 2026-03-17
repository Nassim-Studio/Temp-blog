# Corporate Blog - Hugo & Tailwind CSS

A high-performance, multi-language corporate blog built with **Hugo** and **Tailwind CSS v4**. Deployed automatically to **GitHub Pages**.

## 🚀 Getting Started

### Local Development
1. Install dependencies:
   ```bash
   npm install
   ```
2. Start the development server (runs Tailwind & Hugo):
   ```bash
   npm run dev
   ```

### Deployment (GitHub Actions)
This project is configured to deploy automatically to GitHub Pages on every push to the `main` branch.
- See workflow: `.github/workflows/hugo.yml`

---

## 🔐 CMS Setup (Netlify Authentication)

To enable content editing via the `/admin` dashboard, you must set up an authentication gateway on Netlify.

### 1. Create a Netlify Site
1. Log in to [Netlify](https://app.netlify.com/).
2. Click **"Add new site"** > **"Import an existing project"**.
3. Connect to **GitHub** and select this repository (`Temp-blog`).
4. **Note**: Build settings don't need to succeed; we only need the site identity.

### 2. Enable Identity & Git Gateway
1. Go to **Site Configuration** > **Identity** and click **"Enable Identity"**.
2. Scroll to **Services** > **Git Gateway** and click **"Enable Git Gateway"**.
3. Under **Registration preferences**, it is recommended to set it to **"Invite only"**.

### 3. Final Step
1. Get your Netlify site name (e.g., `nassim-blog-admin.netlify.app`).
2. Update the `site_id` in `static/admin/index.html` (or provide it to the developer).

---

## 🛠 Project Structure
- `content/`: Multi-language posts (EN/FR).
- `assets/css/main.css`: Tailwind CSS source.
- `layouts/`: Hugo templates.
- `static/admin/`: Sveltia CMS configuration.
