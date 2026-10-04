# Deploying PLKC Cross Country

Two parts, done once:

1. **GitHub** holds the files, so publishing an update means uploading one file.
2. **Netlify** puts the site at a real web address and connects to the repo. Every
   time the repo changes, Netlify republishes the site within about a minute.

You don't need the command line. Setup takes about 15 minutes.

---

## 1. Put the files on GitHub

1. Go to **github.com**, click the **+** in the top right, then **New repository**.
2. Name it `plkc-xc` (or anything you like).
   - Choose **Private**. The site will still be public through Netlify, but the
     repo and its history stay private. Netlify's free plan works with private repos.
   - Leave all the "Initialize this repository with" boxes **unchecked**, so the
     repo starts empty.
3. Click **Create repository**.
4. On the empty repo's page, click the **uploading an existing file** link.
5. Drag in all the files from this package: `index.html`, `netlify.toml`,
   `README.md`, `DEPLOY.md`, `CHANGELOG.md` and `.gitignore`.
   - On a Mac, `.gitignore` is hidden in Finder. Press **Cmd + Shift + .** to show
     it, or skip it. The site works without it.
6. Type a commit message (for example "First version") and click **Commit changes**.

---

## 2. Connect Netlify to the repo

1. Go to **netlify.com** and sign in. **Sign up with GitHub** is easiest, and if you
   already use Netlify for the Sion site, use that same account.
2. Click **Add new site**, then **Import an existing project**, then **GitHub**.
3. Approve access if GitHub asks, and pick the `plkc-xc` repo. If it isn't listed,
   click **Configure the Netlify app on GitHub** and give it access to that repo.
4. Leave the build settings as they are: no build command, and the publish
   directory `.` (it's already set in `netlify.toml`). Click **Deploy**.
5. After about 30 seconds you'll have a live address like
   `random-name-123.netlify.app`.
6. Optional: under **Site configuration > Change site name**, rename it to
   something like `plkc-xc`, which gives you **plkc-xc.netlify.app**.

Share that address with anyone. They don't need an account.

---

## Publishing updates

When new results come in (for example 2026 Race 3):

1. Send the new PDFs to Claude and ask for an updated `index.html`.
2. In the GitHub repo, click **Add file > Upload files**, drag in the new
   `index.html` and click **Commit changes**. A file with the same name replaces
   the old one.
3. Optional: add a line to `CHANGELOG.md` (pencil icon, edit, commit).

Netlify sees the commit and republishes on its own. Anyone who reloads the page
gets the new version; `netlify.toml` stops browsers from showing an old copy.

To check that it worked, open **Netlify > Deploys**. The newest entry should say
**Published** with the time of your commit.

---

## Good to know

- **Who can see it:** anyone with the link. Search engines can find it too once
  the link is shared publicly. The page has kids' names and times. Those are
  already public in the meet results, but this page gathers them in one place, so
  share the link with that in mind. Netlify's site-wide password protection
  requires a paid plan.
- **Going back:** every upload is saved in GitHub's history. In Netlify, the
  **Deploys** list lets you republish any earlier version with one click
  (**Publish deploy**).
- **Cost:** GitHub and Netlify are both free for a site like this.
