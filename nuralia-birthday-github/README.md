# Nuralia Birthday Website ❤️

A mobile-first, cinematic birthday experience for GitHub Pages.

## Important: how the two-photo setup works

GitHub Pages is static hosting. A browser page cannot write uploaded photos into your GitHub repository. This project therefore uses a safe, GitHub-only handoff:

1. Deploy the project once **without** `config.json` and without the photos. The setup screen will appear.
2. Open the website and select exactly two photos.
3. Click **PREPARE MY TWO PHOTOS**. Your browser downloads `photo1.jpg`, `photo2.jpg`, and `config.json`.
4. In your GitHub repository, create an `images` folder and upload the two downloaded photos there.
5. Upload `config.json` into the repository root (same level as `index.html`).
6. Commit the changes and wait for GitHub Pages to redeploy.
7. Refresh the website. The setup screen will disappear and every visitor will see the same two photos.

The setup page does not contain a GitHub token, password, or write access. A visitor can select files in their own browser, but cannot change the published website. Only someone with repository write access can publish changed files.

**Do not upload private or intimate photos to a public repository.** A public GitHub Pages website and its repository assets may be accessible to anyone.

## Project files

- `index.html` — complete website
- `images/` — add `photo1.jpg` and `photo2.jpg` here after setup
- `music/` — optional `song.mp3`
- `.github/workflows/deploy.yml` — automatic GitHub Pages deployment

## Music

Add your own audio file at `music/song.mp3`. The visitor must tap MUSIC OFF to start playback; browsers block reliable autoplay. Use music you have permission to use.

## Publish with GitHub Pages

1. Create a GitHub repository, for example `nuralia-birthday`.
2. Upload all project files.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **GitHub Actions**.
5. The included workflow deploys the site after each push to `main`.
6. After the first deployment, open the Pages URL shown in Settings → Pages.

## Updating photos later

To replace the two photos, replace `images/photo1.jpg` and `images/photo2.jpg` in the repository and commit. The setup screen is hidden after `config.json` is published.
