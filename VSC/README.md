# CYBERWISE 🛡️ - Cybersecurity Awareness
**Stay Smart. Stay Secure.**

A website that teaches students how to protect their accounts and personal
information online. Built with **HTML, CSS and JavaScript** for ITEL 1 - Web
Systems and Technologies (Final Examination), Cristal e-College.

## Team
- Genevalyn Bulingkit - Member 1: System Analyst and Pitch Presenter
- Kelly Sumampong - Member 2: Front-End Developer
- Aluise Vincent Clenista - Member 3: JavaScript Developer
- All members - Member 4: QA Tester and System Demonstrator

## Problem
Many students use weak or reused passwords, click suspicious links and share too
much personal information online. This puts their accounts and identity at risk.

## Solution
CYBERWISE teaches cybersecurity in a simple, interactive way and lets students
test what they learned in a quiz game.

## Features
1. **Cybersecurity Awareness** - the basics, why students are targeted, 5 golden habits.
2. **Password Security Guide** - live strength checker, rough crack-time estimate, random password generator, do's and don'ts.
3. **Common Cyber Threats** - 8 threats (phishing, smishing, malware, ransomware...) with search, filters, warning signs and safety steps.
4. **Online Privacy Tips** - 10-item checklist with progress bar, saved in the browser.
5. **Cybersecurity Quiz Game** - 10 random questions, 15-second timer, speed and streak bonus, 3 lives, 50/50 lifeline, rank titles, leaderboard.

## Files
| File | Purpose |
|------|---------|
| index.html | Page structure (Member 2) |
| style.css | Design and layout (Member 2) |
| script.js | All interactive features (Member 3) |
| TEST_CASES.md | Test table and bug log (Member 4) |

## Run locally
Double-click `index.html`. No server and no database needed.

## Publish on GitHub Pages (Output: Working Website on GitHub)
1. Create a GitHub account and click **New repository**. Name it `cyberwise`, set it to Public.
2. Click **uploading an existing file**, drag `index.html`, `style.css`, `script.js`, `README.md`, then **Commit changes**.
3. Go to **Settings > Pages**. Under Branch choose `main` and `/ (root)`, then **Save**.
4. Wait 1 to 2 minutes. Your link will be `https://YOUR-USERNAME.github.io/cyberwise/`.

---

# Quick Q&A guide (the instructor may ask each member)

## Member 2 - Kelly (HTML/CSS)
- **Why a `<section>` for every page?** Each page is a section. JavaScript adds the class `active` to one. CSS: `.page { display:none } .page.active { display:block }`.
- **Change the color theme?** Edit the variables at the top of `style.css` (`--accent`, `--good`, `--bad`, `--warn`).
- **Which tags make the expandable threat cards?** `<details>` and `<summary>` (created in JavaScript).
- **How is the layout in 3 columns?** `.grid-3 { display:grid; grid-template-columns: repeat(3, 1fr); }`.
- **How is it responsive?** `@media (max-width: 700px)` makes the columns stack.
- **Modification example:** add a new menu button in `index.html` and a matching `<section id="...">`.

## Member 3 - Aluise (JavaScript)
- **Variables / data:** arrays of objects `THREATS`, `PRIVACY_TIPS`, `QUESTIONS`; the `quiz` object (score, lives, streak).
- **Functions:** `validateName()`, `runChecks()`, `scorePassword()`, `generatePassword()`, `renderThreats()`, `renderPrivacy()`, `startQuiz()`, `answer()`, `endQuiz()`, `saveScore()`.
- **Events:** `click`, `submit`, `input` (password box), `change` (checkboxes), `keydown`.
- **Conditions:** `if (isCorrect) {...} else {...}` in `answer()`. `if (quiz.lives <= 0)` ends the game.
- **Loops:** `forEach`, `for` in the shuffle and `isCommon()`.
- **Validation:** `validateName()` checks empty, length 2-15 and allowed characters (regular expression). The generator checks that at least one option is ticked.
- **localStorage:** `saveJSON()` and `loadJSON()` store the name, scores, stats and checklist. No database.
- **How is the password score computed?** Length gives up to 48 points. Each type (upper, lower, number, symbol) gives 13. Common words or patterns cap the score at 25.
- **Why does the quiz data have the correct answer first?** `options[0]` is always correct, then `shuffle()` mixes them when the game starts.
- **Modification examples:**
  - 5 lives instead of 3: change `quiz.lives = 3` in `startQuiz()` and the `3 - quiz.lives` in `updateQuizHUD()`.
  - 20 seconds per question: change `QUESTION_TIME = 15`.
  - 5 questions per game: change `QUIZ_LENGTH = 10`.
  - Minimum password length rule: change `pw.length >= 12` in `runChecks()`.
  - Add a question: add an object to `QUESTIONS` (correct answer first).
  - Add a threat or privacy tip: add an object to `THREATS` or `PRIVACY_TIPS`.

## Member 1 - Genevalyn (Pitch)
- **Problem:** weak passwords, phishing and oversharing put student accounts at risk.
- **Why a website?** Anyone can open it on a phone or laptop, no install needed.
- **Why a quiz game?** Practice and instant feedback help people remember.
- **Target users:** high school and college students.
- **Objectives:** teach the basics, help users test and create strong passwords, recognise threats, improve privacy habits, and check learning with a quiz.
- **Why no database?** It keeps the project simple and works offline. localStorage is enough for scores and the checklist.
- **Is the password checker safe?** It runs only in the browser. Nothing is sent or stored.

## Member 4 - QA and Demo (everyone)
- Use `TEST_CASES.md`. Suggested demo order: Home (wrong name first, then valid) > Awareness > Passwords (type "123456", then a strong one, then Generate) > Threats (search "phishing", open a card) > Privacy (tick items, refresh to show saved) > Quiz (answer correct and wrong, use 50/50) > Ranks (refresh to show saved scores).
