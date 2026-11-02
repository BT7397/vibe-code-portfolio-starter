# 🚀 Vibe Code Your Portfolio

Welcome to the workshop! This repo is a **starter skeleton** for your personal portfolio website. You'll clone it, use **GitHub Copilot in VS Code** to make it *yours*, push it to GitHub, and then put it live on the internet with **Render**.

No frameworks and no installs needed. It's just HTML, CSS and JavaScript.

---

## 📁 What's inside

```
.
├── index.html            ← The page itself (all your content lives here)
├── css/style.css         ← How it looks (colours, fonts, layout)
├── js/main.js            ← Small interactive bits (dark mode, footer year)
├── assets/images/        ← Put your photo and project screenshots here
├── assets/resume/        ← Put your resume PDF here (optional)
├── docs/setup-guide.pdf  ← Printable install guide with screenshots
├── .github/copilot-instructions.md ← Rules Copilot reads automatically. Don't delete!
├── render.yaml           ← Hosting settings for Render
├── PROMPTS.md            ← Prompt ideas for vibe coding
├── CHECKLIST.md          ← Tick these off before you call it done
└── README.md             ← You are here
```

---

## ✅ Before the workshop

> 📄 **New to all this?** Follow the printable **[Setup Guide with screenshots (PDF)](docs/setup-guide.pdf)**. It walks you through every install step below.

1. **Make a GitHub account**: <https://github.com/signup>
2. **Install Git**: <https://git-scm.com/downloads>
3. **Install VS Code**: <https://code.visualstudio.com/>
4. **Set up GitHub Copilot** in VS Code:
   - Click the **Copilot icon** at the top of VS Code (or the accounts icon, bottom left) and **sign in with GitHub**
   - Everyone gets **Copilot Free**. Students can get **Copilot Pro for free** by verifying with [GitHub Education](https://education.github.com/pack)
5. **Make a Render account**: <https://render.com>. Choose **Sign up with GitHub**, it makes Step 7 easier.
6. **Tell Git who you are** (one time only, use the same email as your GitHub account):

   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "you@example.com"
   ```

---

## Step 1: Get your own copy of this repo

On this repo's GitHub page, click **Fork** (top right). This makes **your own copy** under your account, which you're allowed to push to.

## Step 2: Clone it to your computer

On **your copy's** page, click the green **Code** button and copy the HTTPS URL. Then in a terminal:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
code .
```

🎉 You now have the project on your computer, open in VS Code.

> Prefer clicking? In VS Code: **Ctrl+Shift+P** (Mac: **Cmd+Shift+P**) → **Git: Clone** → paste the URL.

## Step 3: Open your website in the browser

When you open the project in VS Code for the first time:

1. VS Code asks **"Do you trust the authors of the files in this folder?"** Click **Yes, I trust the authors**. If you see a blue **Restricted Mode** bar at the top instead, click **Manage → Trust**. Copilot can't edit your files until you do this.
2. VS Code pops up *"This workspace has extension recommendations"*. Click **Install**. This installs **Live Server** (and Copilot, if you don't have it yet).

### How does a website "run"?

There is nothing to compile or install. Your website is just files: `index.html` is the page, and it loads `css/style.css` and `js/main.js`. **Your web browser reads these files and draws the page.** "Running" your site just means opening `index.html` in a browser.

There are two ways to do it. **Use Option A (Live Server)** while you're working. Option B is a backup.

### Option A: Live Server (recommended) ⭐

Live Server opens your site and **refreshes the browser by itself every time you save a file**, so you see Copilot's changes straight away.

1. In the **Explorer** on the left of VS Code, **right-click `index.html`** → click **Open with Live Server**
   - Or click **Go Live** in the blue bar at the **bottom-right** of VS Code
2. Your browser opens at an address like `http://127.0.0.1:5500/index.html`. That's your site, running on your own computer. Only you can see it.
3. Make a change and **save it** (**Ctrl+S**, Mac: **Cmd+S**). The browser updates by itself.
4. To stop Live Server, click the same button in the bottom-right of VS Code. While it's running, the button shows **Port : 5500** instead of **Go Live**.

> Don't see **Open with Live Server** or **Go Live**? Live Server isn't installed. Click the **Extensions** icon on the left of VS Code (four squares), search for **Live Server** (by Ritwick Dey), click **Install**, then try again.

### Option B: Open the file directly

No extension needed. Open a terminal **in your project folder** (in VS Code: **Terminal → New Terminal**) and type:

| Your computer | Command |
|---|---|
| Windows (Command Prompt, PowerShell or Git Bash) | `start index.html` |
| Mac (Terminal) | `open index.html` |

Your default browser opens the page. The address starts with `file:///`, which means it's reading the file straight from your computer.

You can also just **double-click `index.html`** in File Explorer (Mac: Finder).

⚠️ With Option B the browser **doesn't refresh by itself**. After you save a change, click the browser and press **F5** (Mac: **Cmd+R**) to see it.

### Which one should I use?

| | Option A: Live Server | Option B: `start index.html` |
|---|---|---|
| Setup | Install one extension | Nothing |
| Shows your changes | By itself, on save | Only after you press F5 |
| Address bar | `http://127.0.0.1:5500/...` | `file:///C:/...` |
| Best for | Working on your site | A quick look |

### Something wrong?

| What you see | Fix |
|---|---|
| My change doesn't show up | Did you **save**? A white dot ● on the file's tab means it isn't saved. Press **Ctrl+S**. Tip: turn on **File → Auto Save**. |
| The page is plain black text with no colours | The browser can't find `css/style.css`. Make sure you opened the `index.html` inside your project folder, and that you didn't move or rename the `css` folder. |
| `npm error Missing script` after `npm start` or `npm run dev` | This project doesn't use npm (that's for other kinds of projects). Use Option A or Option B above. If Copilot created a `package.json`, you can delete it. |
| `start` is not recognized / file not found | Your terminal isn't in the project folder. Run `cd your-repo-name` first, or use **Terminal → New Terminal** in VS Code. |
| Live Server opens a list of files instead of my site | You opened the wrong folder. Use **File → Open Folder** and pick the folder that has `index.html` directly inside it. |

## Step 4: Vibe code it with Copilot ✨

1. Open Copilot Chat: click the **chat icon** at the top of VS Code, or press **Ctrl+Alt+I** (Mac: **Ctrl+Cmd+I**)
2. At the bottom of the chat box, switch the mode to **Agent**. In Agent mode Copilot edits your files for you.
3. Describe what you want. Not sure what to ask? Open **[PROMPTS.md](PROMPTS.md)**.
4. Copilot shows its changes. Look at the browser, then click **Keep** if you like it or **Undo** if you don't.

Copilot automatically follows the rules in `.github/copilot-instructions.md` (plain HTML/CSS/JS, explain changes, etc.), so you don't need to repeat them.

Golden rules:
- **Start with your real content** (name, about, projects), then make it pretty
- **Make one change at a time** and check the browser after each one
- **Commit when something works** (see Step 5). It's your save point.
- Point Copilot at a file by typing `#` in chat, e.g. `#style.css make the buttons rounder`

## Step 5: Save your work with Git

Every time you reach a version you're happy with:

```bash
git status                             # see what changed
git add .                              # stage all changes
git commit -m "Add my about section"   # save a snapshot with a message
```

> Prefer clicking? Use the **Source Control** tab in VS Code (the branch icon on the left, or **Ctrl+Shift+G**). Type a message and click **Commit**. Copilot can even write the message for you: click the ✨ sparkle in the message box.

Good commit messages say **what** you changed: `Add projects section`, `Change colour scheme to green`, `Fix mobile layout`.

## Step 6: Push to GitHub

```bash
git push
```

(Or click **Sync Changes** in the Source Control tab.) Refresh your repo on GitHub and your changes should be there.

> 🔐 The first time you push, VS Code or Git may ask you to sign in to GitHub. That's normal.

## Step 7: Put it live on Render 🌍

1. Go to the [Render Dashboard](https://dashboard.render.com) and click **+ New → Static Site**
2. Connect your GitHub account if asked, then pick **your portfolio repo**
3. Fill in the settings:

   | Setting | Value |
   |---|---|
   | **Name** | something unique, e.g. `yourname-portfolio` (this becomes your URL) |
   | **Branch** | `main` |
   | **Root Directory** | *leave empty* |
   | **Build Command** | *leave empty* (if Render insists, type `echo "no build"`) |
   | **Publish Directory** | `.` |

4. Click **Deploy Static Site** and wait about a minute
5. Your live link appears at the top: `https://yourname-portfolio.onrender.com` 🎉

From now on, **every `git push` updates your live site automatically.**

> Prefer the shortcut? This repo includes a `render.yaml`. In Render choose **+ New → Blueprint**, pick your repo, and it fills in the settings for you. Change the `name:` in `render.yaml` first so it's unique.

---

## 🆘 Common problems

| Problem | Fix |
|---|---|
| `git: command not found` | Git isn't installed, or restart VS Code / your terminal after installing |
| `Permission denied` / `403` on push | You cloned the original repo, not your copy. Fork it, then run `git remote set-url origin <your-copy-url>` |
| `Please tell me who you are` | Run the two `git config` commands from "Before the workshop" |
| `rejected ... fetch first` | The repo on GitHub has changes you don't have. Run `git pull`, then `git push` |
| Copilot isn't changing my files | Make sure the chat mode is set to **Agent**, and that the folder is trusted (no blue **Restricted Mode** bar) |
| Copilot says I hit my limit | Copilot Free has a monthly limit. Apply for free Pro via GitHub Education, or make smaller, more specific requests |
| Render can't see my repo | In Render go to **Account Settings → GitHub** and give Render access to that repo |
| Render shows "Not Found" | Publish Directory must be `.` and `index.html` must be in the **root** of the repo, not a subfolder |
| Image works locally but not on Render | File names are **case-sensitive** online: `Me.JPG` ≠ `me.jpg` |
| Live site didn't update | Check you actually pushed (`git status`), then look at the **Events** tab in Render for the deploy |

## 📚 Git cheat sheet

| Command | What it does |
|---|---|
| `git clone <url>` | Download a repo to your computer |
| `git status` | Show what's changed |
| `git add .` | Stage all changes for the next commit |
| `git commit -m "msg"` | Save a snapshot |
| `git push` | Upload your commits to GitHub |
| `git pull` | Download new commits from GitHub |
| `git log --oneline` | See your commit history |
| `git restore <file>` | Throw away uncommitted changes to a file |

---

Have fun, and make it look like **you**. 💜
