# Personal Website — Naosher Mustakim

A single-file personal/academic website. Everything (HTML, styles, and
scripts) lives in **`index.html`**, so editing and deploying is simple.

Live site: **https://naosher98.github.io/NMA_website/**

---

## 1. How the file is organized

Open `index.html` and you'll see it's split into clearly labelled,
commented sections. To jump to any part, use your editor's search
(Ctrl/Cmd + F) for these banner words:

| Section            | Search for          | What it holds                                  |
| ------------------ | ------------------- | ---------------------------------------------- |
| Colors & fonts     | `DESIGN TOKENS`     | Site-wide color and font settings              |
| Top bar            | `NAVIGATION BAR`    | Menu links                                     |
| Name + photo       | `HERO SECTION`      | Your name, title, bio, photo, social links     |
| Research interests | `RESEARCH INTERESTS`| Interest cards                                 |
| Education          | `EDUCATION`         | Degree timeline                                |
| Publications       | `PUBLICATIONS`      | Paper list                                     |
| Test scores        | `STANDARDIZED TESTS`| GRE, IELTS, etc.                               |
| Jobs               | `WORK EXPERIENCE`   | Work history timeline                          |
| Hobbies            | `HOBBIES SECTION`   | Books, movies, football, cricket, chess        |
| Contact            | `CONTACT`           | Email, phone, location                         |

Every section has a `TO ADD…` comment telling you exactly which block
to copy when you want another entry.

---

## 2. Common edits

**The golden rule:** to add an item, copy one existing block, paste it,
and change the text inside. Nothing else needs to change.

- **Add a publication** → copy one `<article class="pub-card">` block
- **Add a test (e.g. TOEFL)** → copy one `<div class="test-card">` block
- **Add a job** → copy one `<div class="job-entry">` block
- **Add a book** → copy one `<div class="book-card">` block
  (set its color with `style="--spine:#hexcolor"`)
- **Add a team** → copy one `<div class="team-card">` block
  (set its color with `style="--crest:#hexcolor"`, change the initials)
- **Add a movie** → copy one `<div class="movie-card">` block

**Change the site colors** → edit the variables under `DESIGN TOKENS`
at the top of the `<style>` block:

```css
--accent:      #0a7a6a;   /* main teal highlight */
--accent-warm: #c8763e;   /* secondary orange */
--paper:       #f7f4ef;   /* page background */
--ink:         #1a1a1a;   /* main text */
```

**Change a nav menu link** → find `NAVIGATION BAR` and copy/edit a
`<li>`. The `href="#id"` jumps to the section with that `id`.

**Your details to fill in:** name & bio (hero), university & years
(education), paper titles & links (publications), GRE/IELTS scores &
dates (tests), job roles & companies (experience), and your
books/movies/teams/chess ratings (hobbies).

---

## 3. Adding your photo

1. In the repo, open the **`images`** folder
2. Click **Add file → Upload files**
3. Upload your picture named **`prof_pic.jpg`**

(Or, if your file has a different name, change `src="images/prof_pic.jpg"`
in the `HERO SECTION` of `index.html` to match.)

---

## 4. Deploying to GitHub Pages

### Option A — Edit on the GitHub website (easiest)

1. Go to the repo: `github.com/Naosher98/website`
2. Click **`index.html`** to open it
3. Click the **pencil icon** (Edit this file), top-right
4. Replace the contents with your updated file
5. Scroll down, add a message like `Update site`, click **Commit changes**
6. Wait 1–2 minutes, then visit the live site and **hard-refresh**
   (Ctrl/Cmd + Shift + R)

### Option B — Git command line

```bash
git clone https://github.com/Naosher98/website.git
cd website
# replace / edit index.html in your editor, then:
git add index.html
git commit -m "Update site"
git push
```

---

## 5. Checking Pages settings

The site already publishes automatically. If it ever stops working:

1. Repo → **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **main**, folder: **/ (root)**

---

## 6. Tips

- **Preview before committing:** double-click `index.html` on your
  computer to open it in a browser and check your edits first.
- **Changes not showing?** GitHub Pages takes 1–2 minutes, and browsers
  cache hard — always hard-refresh (Ctrl/Cmd + Shift + R).
- **Don't break a tag:** when copying a block, make sure you copy from
  its opening tag to its matching closing tag (the `<!-- /name -->`
  comments mark where blocks end).
- **Back up:** before a big edit, keep a copy of the working
  `index.html` so you can revert if needed.
