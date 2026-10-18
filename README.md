Hireflow — Mini Applicant Tracking System

Live Demo:https://mellow-moxie-74d443.netlify.app/

A responsive, self-contained Mini ATS prototype built with HTML, CSS, and vanilla JavaScript. No build step or API keys are required.

## Features
- Dashboard metrics: total candidates, interviews, offers, hires
- Candidate CRUD: add, edit, delete, update hiring stage
- Hiring pipeline board grouped by stage
- Search by candidate name, email, or role; filter by stage and position
- Open positions overview
- Export candidates to CSV
- Starts with zero candidates; dashboard metrics reflect only records you add
- Browser `localStorage` persistence and duplicate-email protection
- Responsive desktop and mobile layouts

## Run locally
Open `index.html` in a modern browser. For a local server, run `python -m http.server 8000` from this directory and open `http://localhost:8000`.

## Deploy free on GitHub Pages
1. Create a public repository named `mini-ats` on GitHub.
2. Upload `index.html` and `README.md` to the repository root.
3. In GitHub, open **Settings → Pages**.
4. Under Build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
5. Wait for the Pages deployment. Your public URL will be `https://YOUR-GITHUB-USERNAME.github.io/mini-ats/`.

## Demo video outline (60–90 seconds)
1. Show the dashboard metrics and applications chart (10 sec).
2. Open Candidates and search for “Aarav”; filter by Interview (15 sec).
3. Add a new candidate and save (15 sec).
4. Change a candidate's stage using the stage dropdown (10 sec).
5. Show the pipeline board and open positions (15 sec).
6. Export CSV and finish on the dashboard (10 sec).

## Notes
This is a front-end demo. It starts with an empty candidate list and uses a versioned storage key so older sample data from a previous version is not loaded. The chart is calculated from actual candidate application dates; no fabricated chart values are used. Candidate records are stored in the current browser only; they are not shared across users/devices and there is no authentication or server-side database. Use fictional/demo data only until a backend and access controls are added.


### Duplicate candidate protection
On startup, candidate records are de-duplicated by normalized email address (or by name + position if an email is missing). The cleaned list is saved back to browser storage.
