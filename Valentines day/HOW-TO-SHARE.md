# How to Share Your Valentine's Page with a Link or QR Code

Your site is just HTML, CSS, and JS—no server needed. To share it, you only need to put it online and get a URL. Here are simple options.

---

## Option 1: Netlify Drop (no account, very fast)

1. Go to **[https://app.netlify.com/drop](https://app.netlify.com/drop)** in your browser.
2. **Drag and drop** your whole project folder (`Valentines day`) onto the page.
3. Netlify will upload it and give you a **link** like:  
   `https://random-name-12345.netlify.app`
4. Copy that link and send it to your friend. They open it like any website.
5. **QR code:** Go to **[https://www.qr-code-generator.com](https://www.qr-code-generator.com)** (or search “free QR code generator”), paste your link, and download the QR image. Your friend can scan it with their phone camera to open the page.

*Note: Without a Netlify account the link may expire after a while. Creating a free account and “claiming” the site keeps the link permanent.*

---

## Option 2: GitHub Pages (free, permanent link)

1. Create a **GitHub** account at [github.com](https://github.com) if you don’t have one.
2. Create a **new repository** (e.g. name: `valentines-moodeng`). Don’t add a README.
3. On your computer, open a terminal in your project folder and run:
   ```bash
   git init
   git add .
   git commit -m "Valentine page"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/valentines-moodeng.git
   git push -u origin main
   ```
   (Replace `YOUR-USERNAME` and `valentines-moodeng` with your GitHub username and repo name.)
4. On GitHub: **Settings → Pages**. Under “Source” choose **main** branch, then **Save**.
5. After a minute, your site will be at:  
   `https://YOUR-USERNAME.github.io/valentines-moodeng/`
6. Send that link to your friend. Use a [QR code generator](https://www.qr-code-generator.com) and paste this URL to make a QR code.

---

## Option 3: Surge (link from the command line)

1. Install **Node.js** from [nodejs.org](https://nodejs.org) if you don’t have it.
2. Open a terminal in your project folder (`Valentines day`) and run:
   ```bash
   npx surge
   ```
3. When it asks for email/password, you can sign up or log in. For “project path” press Enter (current folder). It will suggest a URL like `valentines-day.surge.sh`.
4. Use that URL as your link. Create a QR code from it using any free QR generator.

---

## Making the QR code

1. Get your **live link** from Netlify, GitHub Pages, or Surge (as above).
2. Open a site like:
   - [qr-code-generator.com](https://www.qr-code-generator.com)
   - [goqr.me](https://goqr.me)
3. Paste your link into the “URL” or “Website” field.
4. Download the QR image and send it to your friend (e.g. WhatsApp, email). They scan it with their phone camera to open the Valentine’s page.

---

## Quick comparison

| Method        | Best for              | Account? | Link permanent? |
|---------------|------------------------|----------|------------------|
| Netlify Drop  | Fastest, no setup     | Optional | Yes if you claim |
| GitHub Pages  | Permanent, free       | Yes      | Yes              |
| Surge         | If you like terminal  | Yes      | Yes              |

**Easiest path:** Use **Netlify Drop**, get the link, then generate a QR code from that link and send either the link or the QR to your friend.
