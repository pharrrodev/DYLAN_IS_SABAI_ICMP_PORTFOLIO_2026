# DYLAN_IS_SABAI_ICMP_PORTFOLIO_2026

Static audition / link-in-bio page: open `Start_here.html` locally, or deploy to Netlify.

## Deploy to Netlify from GitHub

1. **Push this repo** (without the `.mp4` — it is gitignored because GitHub’s limit is **100MB per file**; your mix is ~**2GB**).

   ```bash
   cd DYLAN_IS_SABAI_ICMP_PORTFOLIO_2026
   git init
   git add .
   git commit -m "Add portfolio site for Netlify"
   git branch -M main
   git remote add origin https://github.com/pharrrodev/DYLAN_IS_SABAI_ICMP_PORTFOLIO_2026.git
   git push -u origin main
   ```

2. In **[Netlify](https://app.netlify.com/)**: **Add new site** → **Import an existing project** → **GitHub** → pick `DYLAN_IS_SABAI_ICMP_PORTFOLIO_2026`.

3. Build settings: **leave blank** — `netlify.toml` already sets `publish = "."` (no build command).

4. **Video on the live site** (pick one):

   - **Recommended:** Upload the mix to **YouTube (Unlisted)** or **Vimeo**, then replace the `<video>` block in `Start_here.html` with their embed iframe (reliable streaming, no 2GB deploy).

   - **Direct MP4:** Host a **smaller** export (e.g. under 95MB) in the repo with a new filename, or use a **GitHub Release** binary / cloud storage with a **direct HTTPS** link to the file. Paste that URL into `REMOTE_MP4_URL` in `Start_here.html` and push again.

   - **Whole folder including the huge MP4:** Use **[Netlify Drop](https://app.netlify.com/drop)** and drag the **entire** folder (HTML + MP4). That bypasses GitHub for the video, but updates are manual unless you later switch to CLI.

   - **Netlify CLI** (optional): `npm i -g netlify-cli`, then `netlify deploy --prod --dir .` from this folder with the MP4 present — can deploy large assets without Git, but not ideal for every small HTML edit.

## Local preview

Double-click `Start_here.html` or `index.html` with the `.mp4` in the same folder.
