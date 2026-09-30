# DEVnetwork (frontend foundation)
React + TypeScript + Vite + Tailwind CSS. Mock data lives in `src/data/`.

## Run locally
    npm install
    npm run dev

## Build
- Build command: `npm run build`
- Output directory: `dist`

## Deploy to Cloudflare Pages
1. Push this folder to a GitHub repo.
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git.
3. Select the repo. Framework preset: Vite (or None).
4. Build command: `npm run build` · Build output directory: `dist`
5. (Optional) Add env vars under Settings → Environment variables. Only `VITE_*` vars reach the browser, so never put secrets there.
6. Deploy. SPA routing is handled by `public/_redirects` (`/* /index.html 200`).

## Notes
Auth forms are UI only; no credentials are handled. `/admin` and `/dashboard` are not protected until a backend exists.
