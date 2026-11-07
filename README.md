# PlutoHacks 2026 – GitHub Copilot Workshop Starter

Starter files for the PlutoHacks GitHub Copilot workshop. You'll warm up in `practice.js`, then use Copilot agent mode to build a hackathon countdown page and push it to your own GitHub.

## 1. Make your own copy

1. Click the green **Use this template** button at the top of this page, then **Create a new repository**.
2. Name it `plutohacks-countdown`, set it to **Public**, and click **Create repository**.
3. On your new repo, click the green **Code** button and copy the HTTPS link.

## 2. Clone it and open it in VS Code

```bash
cd ~/Desktop
git clone https://github.com/YOUR-USERNAME/plutohacks-countdown.git
cd plutohacks-countdown
code .
```

If `code .` doesn't work, open VS Code and use **File → Open Folder**.

## 3. Turn on Copilot

Click the Copilot icon in the VS Code status bar (bottom of the window) and sign in with GitHub.

Students: get the free Copilot Student plan at https://github.com/education/students. Until you're verified, the Free plan is enough for today.

## 4. Warm-up: inline suggestions (in `practice.js`)

Type each comment, press **Enter**, then press **Tab** to accept the gray suggestion (**Esc** dismisses it).

```js
// function that takes an end date and returns the days, hours, minutes and seconds left until then
```

```js
// format that result as a string like "2d 5h 12m 3s"
```

## 5. Copilot Chat

Open chat with **Ctrl + Alt + I** (Mac: **Cmd + Ctrl + I**). Select your function in `practice.js`, then send:

```text
/explain
```

```text
/fix what happens if the end date is already in the past? Return all zeros instead of negative numbers.
```

## 6. Agent mode: build the countdown page

In the chat panel, switch the mode dropdown to **Agent** and send:

```text
Create a single-page countdown website for the PlutoHacks hackathon in this folder. Use plain HTML, CSS and JavaScript in three files: index.html, style.css and script.js. Show the days, hours, minutes and seconds left until November 7, 2026 at 9:30 PM local time (PlutoHacks runs from November 6, 2026 at 5:00 PM to November 7, 2026 at 9:30 PM), updating every second. Use a dark space theme with purple and teal accents. Do not use any frameworks or build tools.
```

Click **Keep** on the changes, then open `index.html` in your browser (double-click it, or run `start index.html` on Windows / `open index.html` on Mac).

## 7. Add features, one at a time

Switch models with the picker at the bottom of the chat box if you like, then pick one:

```text
When the countdown reaches zero, hide the timer and show "Hacking is over! Submit your project" in big text.
```

```text
Make the page look good on a phone screen.
```

```text
Add a button that switches between light and dark themes and remembers the choice after a reload.
```

Finished early?

```text
Add a confetti animation when the countdown reaches zero, without using any libraries.
```

## 8. Commit and push

```bash
git add .
git commit -m "Add PlutoHacks countdown page built with Copilot"
git push
```

Refresh your repo on GitHub to see your files.

**Bonus – make it a live website:** in your repo go to **Settings → Pages**, set **Source** to **Deploy from a branch**, pick `main` and `/ (root)`, and click **Save**. After a minute it's live at `https://YOUR-USERNAME.github.io/plutohacks-countdown/`.

## Want to get more into Git?

[Essential Git](https://github.com/boxwrx/essential-git) goes further into Git than today's workshop.

## Stuck?

| Problem | Fix |
| --- | --- |
| No gray suggestions | Click the Copilot icon in the status bar and check you're signed in |
| No **Agent** option in chat | Update VS Code and restart it |
| "Author identity unknown" on commit | Run `git config --global user.name "Your Name"` and `git config --global user.email "you@example.com"` |
| `git push` asks for a password | Use **Sync Changes** in VS Code's Source Control panel |
| Page is blank | Press F12, copy the red error from the Console, and paste it into chat after `/fix` |
