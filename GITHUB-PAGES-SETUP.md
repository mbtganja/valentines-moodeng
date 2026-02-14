# GitHub Pages – Where to Find "Source" / Deploy from Branch

GitHub's Pages settings can look different depending on account and repo. Use the steps that match what you see.

---

## If you only see "Add domain" (no Source option)

A **workflow file is already in your project**: `.github/workflows/pages.yml`. It deploys your site when you push—you don't need to set "Source" or "Deploy from a branch".

**Do this:**

1. **Commit and push** the whole project (including the `.github` folder):
   ```powershell
   cd "c:\Users\Snow\Downloads\Valentines day"
   git add .
   git commit -m "Add Pages workflow"
   git push origin main
   ```
   (Use `master` instead of `main` if that's your branch name.)

2. On GitHub, open your repo → **Actions**. Wait for the "Deploy to GitHub Pages" run to finish (green checkmark).

3. Your site will be at: **`https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`**

"Add domain" is only for custom domains—you can ignore it.

---

## Step-by-step (when Source is visible)

1. Open **your repository** on GitHub (the Valentine's one).
2. Click **Settings** (repo menu, not your profile).
3. In the **left sidebar**, under **"Code and automation"**, click **Pages**.
4. On the right you should see a **"Build and deployment"** section.
5. In that section, look for **"Source"**:
   - It may be a **dropdown** that currently says **"GitHub Actions"**.
   - Click that dropdown and choose **"Deploy from a branch"**.
6. After you select it, **Branch** and **Folder** options appear:
   - **Branch:** choose **main** (or **master** if that's your default).
   - **Folder:** choose **/ (root)**.
7. Click **Save**.

Your site will be at: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

---

## If you don't see "Source" but you see other options

- **Check the sidebar:** Make sure you're in **Settings → Pages** (under "Code and automation"), not "Actions" or "Environments".
- **Scroll:** "Build and deployment" and "Source" are often below the "Pages" header; scroll down on the right side.
