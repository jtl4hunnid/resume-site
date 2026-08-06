# Lesson 16 — Working Together: Pull Requests

So far, every repo has been *yours*. But real software is built by **teams** — lots of people
changing the same project without stepping on each other. Today you learn the tool that makes that
possible: the **Pull Request**.

As a group, you'll build one **Class Summary Page** — each of you adds your own piece to it, the way
a real dev team adds features to a shared product.

> ⭐ **A Pull Request (PR) is how you say: "here's a change I'd like to make — can someone check it
> before it goes in?"** Nothing lands until a human reviews it. This is exactly how professional
> teams protect their shared code, and it's the last big GitHub skill you need.

---

## Step 1 — Get today's lesson

**▶ Try it**
```
cd Documents\SummerYouthProject
```

**▶ Try it**
```
git pull --no-edit lessons main
```

---

## Step 2 — What a Pull Request actually is

Picture the shared project as a group document. You don't just scribble on the master copy — that
would be chaos with six people. Instead:

1. You make your **own copy of a branch** to work on.
2. You make your change there.
3. You open a **Pull Request** — a polite "please pull my change into the main project."
4. Someone **reviews** it (your instructor, maybe a classmate) and either asks for tweaks or
   approves.
5. When approved, it gets **merged** — now your change is part of the shared project.

Nobody's work gets overwritten, and every change gets a second set of eyes. That's the whole idea.

---

## Step 3 — Get the shared repo

Your instructor will give you the link to the **class summary repo** (it's different from your own
site). Clone it next to your other work — you know this from Lesson 1:

**▶ Try it** *(use the real link your instructor gives you)*
```
git clone https://github.com/cjackson-coc/THE-SUMMARY-REPO.git
```

**▶ Try it**
```
cd THE-SUMMARY-REPO
```

Open it in VS Code with `code .` and look around. There's an `entries` folder — that's where each
person's piece goes.

---

## Step 4 — Make your own branch

You never work directly on `main` in a shared repo. You make a **branch** — your own safe workspace.
Name it `add-YOURNAME`:

**▶ Try it** *(use your name, lowercase)*
```
git checkout -b add-jordan
```

`checkout -b` means "make a new branch and switch to it." Anything you do now happens on *your*
branch, not the shared `main`.

> ⭐ **A branch is your own lane.** You can change whatever you want on it without affecting anyone
> else, until it's reviewed and merged.

---

## Step 5 — Add your piece

In the `entries` folder, **make a new file** named `yourname.md` (lowercase, e.g. `jordan.md`).
Nobody else has this file, so you can't collide with anyone.

Put your summary in it — a few lines about your experience. For example:

```markdown
## Jordan Rivera

I came in knowing nothing about code. This summer I built a real website with HTML, Tailwind, and
JavaScript, put it live on the internet, and learned to use the developer tools. My favorite part
was building the dark mode button.

My site: https://jordan.github.io/resume-site/
```

Save it.

---

## Step 6 — Send your branch up

Save your work to your branch:

**▶ Try it**
```
git add .
```

**▶ Try it**
```
git commit -m "Add my summary entry"
```

**▶ Try it** *(this pushes your branch, not main)*
```
git push -u origin add-jordan
```

*(Use your own branch name.)* Your branch is now on GitHub, waiting to become a Pull Request.

---

## Step 7 — Open the Pull Request

1. Go to the summary repo on **GitHub** in your browser.
2. You'll see a banner: **"add-jordan had recent pushes — Compare & pull request."** Click it.
   *(No banner? Click the **Pull requests** tab → **New pull request** → pick your branch.)*
3. Give it a title like **"Add Jordan's summary"** and a short description.
4. Click **Create pull request.**

That's it — you've opened a PR. Your change is now proposed, not yet merged. It's waiting for review.

> ⭐ **Look at what you just made:** a page showing your file, your change highlighted in green, and a
> space for people to comment. This is where real code review happens, every day, at every software
> company.

---

## Step 8 — Review and merge

This part is done **together**, out loud:

- Your instructor (and maybe a classmate) opens your PR and **reviews** it — reads your change,
  maybe leaves a comment.
- If something needs fixing, you fix it on your branch and push again — the PR updates automatically.
- When it's approved, it gets **Merged**. Your entry is now part of the shared summary page. 🎉

Watch a couple of classmates' PRs get reviewed too. Notice: everyone added a *different* file, so
six people changed the same project at the same time with **zero conflicts.** That's not luck —
that's the point of good structure.

---

## If it didn't work

**`git push` says something about "no upstream branch."**
Use the full version with `-u origin`: `git push -u origin add-yourname`. Git is just asking where to
put your branch the first time.

**I don't see the "Compare & pull request" banner.**
Go to the **Pull requests** tab on the repo → **New pull request** → set "compare" to your branch →
**Create pull request.**

**My PR shows changes to files I didn't touch.**
You probably branched after someone else's merge. That's usually fine — but flag it to your
instructor before merging so nothing unexpected goes in.

**I made a mistake in my entry after opening the PR.**
Just fix the file, `git add .`, `git commit`, and `git push` again on the same branch. The PR
updates itself — no need to open a new one.

> **Still stuck?** The concept is the prize here: propose → review → merge. Even if the git steps
> get tangled, understanding *why* teams work this way is what matters. Ask for a hand and keep going.

---

## When you get stuck (and you will)

Read the error out loud. Ask a classmate. Google the exact message.

Googling an error and reading the answers is the actual skill — every professional developer does it
daily, all day. Getting stuck isn't a sign you're behind. It's the job.

---

## Before you move on

Add a couple of sentences to `reflections.md` under **Lesson 16**.

*What's the point of a Pull Request instead of just changing the shared project directly? How did it
feel to have your change reviewed before it went in?*

**Done looks like:** your entry is merged into the class summary page through a Pull Request that
someone reviewed — and you can explain, in your own words, why teams work this way.

Next up: **getting ready to show off what you built** — `docs/lesson-17-present.md`.
