# Shadab Ahad: Portfolio

Static site (HTML, CSS, vanilla JS). No build step, no dependencies.

## Run locally
    cd portfolio
    python3 -m http.server 8000     # then open http://localhost:8000
(or `npx serve`, or the VS Code "Live Server" extension)

## Add your photo
Save a portrait as `assets/photo.jpg` (4:5 ratio, ~800x1000px). Until then, an "SA" placeholder shows.

## CV
Your CV is already at `assets/Shadab_Ahad_CV.pdf`. To update it, replace that file with the same name.

## Contact form
It validates input and opens the visitor's email app via `mailto:`. No messages are sent by a server.
For real delivery, create a free form at formspree.io, then in `index.html` replace the mailto line in the submit handler
with a `fetch('https://formspree.io/f/YOUR_ID',{method:'POST',headers:{Accept:'application/json'},body:new FormData(F)})` call
and show the success/error state from the response.

## Deploy (Vercel)
1. Push this folder to a GitHub repo.
2. At vercel.com click Add New > Project, import the repo.
3. Framework preset: Other. No build command; output directory is the root. Deploy.
(Netlify and GitHub Pages work the same way.) Update the `<title>`/Open Graph tags if you add a custom domain.
