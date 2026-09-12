# 30 Days of Conversation

A self-contained 30-day English coursebook and interactive practice website. Each lesson includes a teaching note, useful phrases, three model dialogues, nine categorized alternative phrases, four scored multiple-choice questions with feedback, three open responses, a role-play, notes, and a speaking timer. Four daily checklist steps track progress. Day 7, 14, 21, and 28 are review lessons.

## Use locally

Run `python3 -m http.server 8000` in this folder and open `http://localhost:8000`. A local server is needed because the site loads `lessons.json`; opening `index.html` directly as a `file://` URL may block it.

## Deploy to GitHub Pages

1. Create a GitHub repository and upload the files in this folder to its root, keeping `index.html`, `styles.css`, `app.js`, `lessons.json`, and `COURSEBOOK.md` together. You can also push this directory with Git.
2. In the repository, open **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, then choose the default branch and **/(root)**. Save.
3. Open the Pages URL GitHub reports after deployment. It will usually resemble `https://YOUR-USERNAME.github.io/REPOSITORY/`.

No build command, server, API key, or dependency installation is needed. `index.html` uses relative asset paths and works under a repository subpath.

## Progress and privacy

The suggested day is calculated from the Day 1 date you choose (the first visit defaults to today). Any day remains available. Checklists, quiz responses, and notes are stored only in the current browser's `localStorage`; they do not sync between devices, and clearing site data removes them. Quiz completion requires all four answers correct; the other steps can be checked manually. The coursebook can be downloaded from the site or read as `COURSEBOOK.md`.

## Content source

`build_content.py` and `extra_content.py` contain the authored lesson material and generates `lessons.json` and `COURSEBOOK.md` from the previous 30-day topic plan. To regenerate after editing the authoring script, edit the included `ORIGINAL_30_DAY_PLAN.txt` if needed and run `python3 build_content.py`. The generated files are already included for deployment.
