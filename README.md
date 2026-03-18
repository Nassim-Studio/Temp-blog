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

## 🔐 CMS Setup (GitHub Authentication)

To enable content editing via the `/admin` dashboard, you must authenticate using a GitHub Personal Access Token (PAT). Since the site is deployed to GitHub Pages, Sveltia CMS uses direct repository access.

### Generating a Personal Access Token
1. Go to your GitHub account settings: **Developer settings** > **Personal access tokens** > **Tokens (classic)**.
2. Click **Generate new token (classic)**.
3. Give it a descriptive name (e.g., "Sveltia CMS Auth") and select your preferred expiration.
4. Under "Select scopes", check the **`repo`** box (this is required to read and save posts).
5. Click **Generate token** and copy it immediately.
6. *(Important for Organizations)*: If the repository belongs to an organization that uses SSO, click **Configure SSO** next to your new token and authorize the organization.

### Logging In
1. Navigate to your live site's `/admin/` page.
2. Below the main "Login" button, click the **"Continue with Access Token"** link.
3. Paste your generated token and click the button to log in.

---

## 🛠 Project Structure
- `content/`: Multi-language posts (EN/FR).
- `assets/css/main.css`: Tailwind CSS source.
- `layouts/`: Hugo templates.
- `static/admin/`: Sveltia CMS configuration.
