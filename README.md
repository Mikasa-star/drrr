# Dr. Ulrike K. Steiner website

Static site. All content is in the `CONFIG` block near the top of the `<script>` in `index.html`.

## Put it on GitHub Pages
1. On github.com click **New repository** (e.g. `steiner-gynecology`), then **uploading an existing file**, and drag in every file from this folder (including `.nojekyll`). Commit.
   Or with git:
   ```
   git init && git add . && git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/steiner-gynecology.git
   git push -u origin main
   ```
2. Repository **Settings → Pages → Build and deployment**: Source "Deploy from a branch", branch `main`, folder `/ (root)`. The site goes live at `https://YOUR-USERNAME.github.io/steiner-gynecology/`.

## Custom domain
1. In **Settings → Pages → Custom domain** enter your domain and save (GitHub creates a `CNAME` file).
2. At your domain registrar add DNS records:
   - Apex domain (`example.com`): four `A` records to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `www`: a `CNAME` record to `YOUR-USERNAME.github.io`
3. After DNS updates (minutes to hours) tick **Enforce HTTPS**.

## Before launch
- Forms: set `formEndpoint` in `CONFIG` to a form service URL (e.g. Formspree). Until then forms show "Not sent" and offer an email draft. Test with a real submission.
- Replace placeholder text marked "confirm before publication" and have the privacy and booking policy reviewed.
- Confirm the address, hours, credentials and board certification with Dr. Steiner.
