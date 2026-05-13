# Lewis & Gould Architects — Website

Static HTML/CSS website for Lewis & Gould Architects, New York.

## Project Structure

```
lewis-gould-architects/
├── index.html                  # Home
├── aboutus.html                # About Us — Overview
├── aboutus_jan.html            # Bio: Jan Gould
├── aboutus_michele.html        # Bio: Michele Lewis
├── aboutus_publications.html   # Publications & Press
├── ourperspective.html         # Our Perspective
├── ourwork.html                # Portfolio / Our Work
├── contactus.html              # Contact
├── css/
│   └── style.css               # All styles
├── images/
│   ├── our-work-sample.jpg     # Drop project photos here
│   ├── jan.jpg                 # Jan Gould portrait
│   ├── michele.jpg             # Michele Lewis portrait
│   └── project-1.jpg … project-8.jpg
└── README.md
```

## Adding Images

Drop image files into the `/images/` folder. File names expected by the site:

| File | Used on |
|------|---------|
| `jan.jpg` | Jan Gould bio page |
| `michele.jpg` | Michele Lewis bio page |
| `our-work-sample.jpg` | Portfolio — featured slot |
| `project-1.jpg` … `project-8.jpg` | Portfolio grid |

Images will display automatically once files are present — no code changes needed.

## Deploying to GitHub Pages

### Option A — Repository root (simplest)

1. Create a new GitHub repository (e.g. `lewis-gould-architects`).
2. Push all files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git remote add origin https://github.com/YOUR_USERNAME/lewis-gould-architects.git
   git push -u origin main
   ```
3. Go to **Settings → Pages** in the GitHub repository.
4. Under **Source**, select **Deploy from a branch**, choose `main` and `/ (root)`.
5. Click **Save**. The site will be live at:
   ```
   https://YOUR_USERNAME.github.io/lewis-gould-architects/
   ```

### Option B — Custom domain

1. Follow Option A above.
2. In **Settings → Pages → Custom domain**, enter your domain (e.g. `www.lewisgould.com`).
3. Add a `CNAME` file to the repo root containing just your domain name.
4. Update your DNS provider to point to GitHub Pages (see GitHub's docs for the exact records).

## Local Preview

No build step required. Open any `.html` file directly in a browser, or use a simple local server:

```bash
# Python 3
python3 -m http.server 8000
# then open http://localhost:8000
```

## Updating Content

- **Copy / text** — edit the relevant `.html` file directly.
- **Styles** — all styles live in `css/style.css`.
- **Contact form** — add a `action="..."` attribute to the `<form>` in `contactus.html` once a backend or form service (e.g. Formspree) is set up.
- **Email address** — search for `[email to be added]` in `contactus.html` and replace.
- **Street address** — search for `Exact address to be confirmed` in `contactus.html` and replace.
