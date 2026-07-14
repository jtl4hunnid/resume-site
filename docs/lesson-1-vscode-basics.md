# Lesson 1 — VS Code + connecting to GitHub

## What is VS Code?

VS Code (Visual Studio Code) is a code editor — like Google Docs, but for
writing code instead of essays. It's free, and it's one of the most-used
editors by professional developers.

## Install it

1. Download from [code.visualstudio.com](https://code.visualstudio.com).
2. Open it. You'll see a welcome screen — close that for now.
3. Install one extension: **Live Server** (search the Extensions icon on the
   left sidebar — looks like four squares). This lets you preview a webpage
   instantly as you edit it.

## Connect GitHub to VS Code

1. Open the **Source Control** icon on the left sidebar (looks like a branch).
2. Click **Clone Repository** and sign in with your GitHub account when
   prompted.
3. Paste the **lessons repo URL** your mentor gives you, and pick a folder
   on your computer to save it to.
4. Open that folder in VS Code (**File → Open Folder**).

## Important — set up your own personal repo too

Your mentor's repo is where lessons come *from* — you'll never push your own
work there. Instead:

1. On GitHub, create a new **empty** repository under your own account
   (e.g. `your-username/my-resume-site`). Don't add a README — leave it
   fully empty.
2. Back in VS Code, open the built-in terminal (**Terminal → New Terminal**)
   and run these two commands (your mentor will help the first time):
   ```
   git remote rename origin lessons
   git remote add origin https://github.com/your-username/my-resume-site.git
   git push -u origin main
   ```
3. From now on: `origin` = your own repo (where **your work** goes),
   `lessons` = your mentor's repo (where **new lessons** come from). Two
   separate remotes, so your work and your mentor's lessons never mix up
   with anyone else's.

## Why we set it up this way

This might feel like extra steps for no reason — here's the actual reason.
This exact pattern (a "lessons" source you only pull from, and "origin" as
your own space you push to) is how real professional developers contribute
to shared projects every day. You're not learning a workaround, you're
learning the real workflow.

```
                 ┌─────────────────────┐
                 │   Mentor's repo     │   <- read-only to you.
                 │   ("lessons")       │      you can only PULL from it.
                 └──────────┬──────────┘
                             │ pull
                             ▼
        ┌───────────────────────────────────────┐
        │           Your computer                │
        │   (one folder, two remotes inside it)  │
        └───────────────────┬─────────────────────┘
                             │ push
                             ▼
                 ┌─────────────────────┐
                 │   Your own repo     │   <- yours alone.
                 │   ("origin")        │      nobody else can push here.
                 └─────────────────────┘
```

Later (Lesson 8), there's a third repo — a shared "showcase" repo everyone
joins for the finale. That's the *only* time everyone's in the same repo.
Until then, your work and your mentor's lessons flow in two separate one-way
directions, so nobody can ever bump into anyone else's work by accident.

## Optional: let your mentor see your progress

If you'd like feedback along the way (not required), you can add your
mentor as a collaborator on your own repo: **Settings → Collaborators →
Add people**. This only gives them the ability to *view* — they still can't
push anything into your repo without your say-so. It also means your
commits and reflections can be included in the program's end-of-summer
report — keeping your repo public works too, same effect, your call.

## Your task

1. Get VS Code installed, the lessons repo cloned, and your own repo set up
   as `origin` per above.
2. Open `README.md` in the file explorer on the left. Click on it once —
   VS Code shows you the raw text. There's a "Open Preview" button (top
   right, looks like a magnifying glass with a book) — click it to see it
   rendered nicely.
3. Read `docs/lesson-2-markdown.md` next.

## From here on: two different buttons

- **Saving your own work** → commit, then **Push** (this goes to your
  `origin` — your own repo, nobody else touches it).
- **Getting the next lesson** → open the terminal and run
  `git pull lessons main` (this only ever brings in your mentor's next
  lesson — never anyone else's work, since nobody else is in this repo).

## Before you move on

Add a couple sentences to `reflections.md` (at the root of the repo) under
**Lesson 0** and **Lesson 1**.
