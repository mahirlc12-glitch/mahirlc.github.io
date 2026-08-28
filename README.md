# Portfolio — Mahir Labib Chowdhury

A single-file, dependency-free personal website (CFD/aerospace themed) ready to host free on **GitHub Pages**. Includes a light/dark toggle, figure slots for project images, and a résumé download button.

The whole site is one file: `index.html`. Fonts load from Google Fonts; the animated hero is plain canvas JavaScript. No build step, no framework.

---

## 1. Edit your details (2 minutes)

Open `index.html` and search for `EDIT` — the only spots you need to change:

| What | Where |
|---|---|
| Email | `mailto:you@example.com` (hero + contact) |
| GitHub URL | `https://github.com/your-username` |
| LinkedIn URL | `https://linkedin.com/in/your-handle` |
| Résumé file | `href="Mahir_Labib_Chowdhury_CV.pdf"` in the hero |

Your name is already set throughout.

## 2. Add your résumé

Drop your CV PDF into the repo root named exactly `Mahir_Labib_Chowdhury_CV.pdf` (or rename the link to match your file). The **Résumé ↓** button then downloads it.

## 3. Add project figures (optional but recommended)

Each project and program card has a placeholder figure box:

```html
<div class="fig"><span class="fig-cap">figure — grid fin CFD</span></div>
```

To use a real image (CFD contour, CAD render, FEA plot):

1. Make an `assets/` folder in the repo and add your images.
2. Replace the whole `<div class="fig">…</div>` with:
   ```html
   <img class="fig" src="assets/gridfin.png" alt="Grid fin CFD contour" />
   ```

The `img.fig` styling already matches the placeholder box (16:9, framed). Leave any card as a placeholder if you don't have an image yet — it still looks intentional.

---

## 4. Put it on GitHub Pages

**Option A — site at `https://<username>.github.io`:**

1. Create a repo named **exactly** `<your-username>.github.io`.
2. Upload `index.html`, `README.md`, your CV PDF, and any `assets/` — via "Add file -> Upload files", or:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. Wait ~1 minute — live at `https://<your-username>.github.io`.

**Option B — any repo name (site at `https://<username>.github.io/<repo>`):**

1. Push `index.html` to a repo with any name (e.g. `portfolio`).
2. **Settings -> Pages -> Build and deployment -> Source:** *Deploy from a branch*.
3. Branch **main**, folder **/ (root)**, **Save**.
4. Wait ~1 minute, reload — the live URL appears at the top.

---

## Notes

- The light/dark toggle remembers your choice and follows your system preference on first visit.
- Palki Motors work is described at a high level — reverse-engineering for simulation plus chassis/body design — without internal specifics. Keep it that way unless something is cleared for public sharing.
- Responsive, keyboard-accessible, and respects `prefers-reduced-motion` (the hero renders a static streamline frame instead of animating).
