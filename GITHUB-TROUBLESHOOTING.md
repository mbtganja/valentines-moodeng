# GitHub Troubleshooting – Valentine's Page

Copy the **exact error message** you see and use the matching fix below. Your files are small enough (cat.gif is ~6 MB; GitHub allows up to 100 MB), so the problem is usually setup or authentication.

---

## 1. "Support for password authentication was removed" / "Authentication failed"

**Fix:** Use a **Personal Access Token (PAT)** instead of your password.

1. On GitHub: **Profile (top right) → Settings → Developer settings → Personal access tokens → Tokens (classic)**.
2. **Generate new token (classic)**. Give it a name, set expiry, and check **repo**.
3. Copy the token (you won’t see it again).
4. When you `git push`, use:
   - **Username:** your GitHub username  
   - **Password:** paste the token (not your account password)

---

## 2. "failed to push some refs" / "Updates were rejected"

**Fix:** Someone else changed the repo, or you created the repo with a README. Pull first, then push:

```powershell
cd "c:\Users\Snow\Downloads\Valentines day"
git pull origin main --rebase
git push origin main
```

If the branch on GitHub is `master` instead of `main`, use `master` in both commands.

---

## 3. "remote: Repository not found" / "Permission denied"

**Fix:** The repo name or URL is wrong, or you don’t have access.

- Check the repo URL: **GitHub → your repo → Code → HTTPS** and copy the URL.
- Set it again:
  ```powershell
  git remote set-url origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
  git push -u origin main
  ```
- Replace `YOUR-USERNAME` and `YOUR-REPO-NAME` with your real username and repo name.

---

## 4. "branch 'main' does not exist" / "src refspec main does not match any"

**Fix:** Your local branch might be named `master`. Check and push the right one:

```powershell
git branch
```

If you see `master`, push that:

```powershell
git push -u origin master
```

Then on GitHub: **Settings → Pages → Source**: choose **master** (not main) and Save.

---

## 5. GitHub Pages: "404" or "Page not found" after push

**Fix:** Give it 1–2 minutes, then:

- **Settings → Pages**: Source = **Deploy from a branch**; Branch = **main** (or **master**), folder **/ (root)**; Save.
- Open: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`  
  (must match your username and repo name; no typo, no extra slash).

---

## 6. "File size too large" (e.g. cat.gif)

Your current files are under GitHub’s limit. If you ever see this, reduce the GIF size (e.g. with [ezgif.com](https://ezgif.com/optimize)) or use a smaller image.

---

**To get the right fix:** Copy the **full error** from PowerShell or the GitHub page and share it (or a screenshot), and we can fix it step by step.
