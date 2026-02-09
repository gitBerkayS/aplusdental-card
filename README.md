# A Plus Dental – Digital Business Card

Mobile-optimized business card for **aplusdental.ca**, ready for **GitHub Pages** (or Netlify).

## What’s included

- **Call** – `tel:` link for (604) 606-4202  
- **Email** – `mailto:` (set to `info@aplusdental.ca`; edit in `index.html` if different)  
- **Website** – Link to https://aplusdentalclinic.com  
- **Maps / Address** – Google Maps directions link and address (1288 Commercial Dr, Vancouver, BC V5L 3X4)  
- **Add to Contacts** – Downloads a vCard (`.vcf`) so users can add the business to their phone contacts  
- **Hours** – Sunday closed; Mon–Fri 10–5; Saturday 11–5  
- **Reviews** – Link to [Google reviews](https://g.page/r/CR7IIDc4Y8l3EBM/review)

---

## Deploy on GitHub Pages

1. **Create a GitHub repo** (e.g. `aplusdental-card` or `aplusdental.ca`).

2. **Push this folder** to the repo:
   ```bash
   cd aplusdental-card
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

3. **Turn on GitHub Pages**
   - Repo → **Settings** → **Pages**
   - Under **Source**: choose **Deploy from a branch**
   - **Branch**: `main` (or `master`) → **/ (root)** → **Save**

4. **Wait a minute or two.** The site will be at:
   - **Project site:** `https://YOUR_USERNAME.github.io/YOUR_REPO/`
   - **Custom domain:** After adding `aplusdental.ca` (see below), it will be `https://aplusdental.ca`

### Custom domain (aplusdental.ca)

- A **CNAME** file is already in the repo with `aplusdental.ca`.
- In the repo **Settings → Pages**, set **Custom domain** to `aplusdental.ca` and save.
- In your domain DNS (where you bought aplusdental.ca), add:
  - **A records** pointing to: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`  
  - **OR** a **CNAME** record: `aplusdental.ca` → `YOUR_USERNAME.github.io`
- GitHub will then offer **Enforce HTTPS** once DNS is correct.

If you are **not** using a custom domain yet, you can delete the `CNAME` file so GitHub doesn’t expect that domain.

---

## Deploy on Netlify (alternative)

1. Push this folder to a Git repo, or use **Netlify Drop**.
2. In [Netlify](https://app.netlify.com): **Add new site** → **Import an existing project** (or drag the folder).
3. Build command: leave empty. Publish directory: `.`
4. Add custom domain `aplusdental.ca` in **Domain settings** and follow Netlify’s DNS steps.

---

## Edit contact details

- **Email:** Search for `info@aplusdental.ca` in `index.html` and update both the `mailto:` link and the vCard block (inside the `<script>` at the bottom).
- **Phone / address / URL:** Same file; update the buttons/links and the vCard string. Directions link: https://maps.app.goo.gl/3do12rpBqmgCN2rL7.

## Local preview

```bash
cd aplusdental-card
npx serve .
```

Open the URL (e.g. http://localhost:3000) on your phone or in dev tools’ device mode.
