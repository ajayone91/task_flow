# TaskFlow AI ⚡

A personal productivity app I built to actually *use* — not just look pretty. It tracks your tasks, habits, skills, and focus time, all in one place. No accounts, no subscriptions, no data leaving your browser.

---

## What it does

**Tasks** — Add tasks with a title, category, priority, due date, and estimated time. You can also break any task into subtasks. Mark things done, delete them, filter by category or priority. Everything you'd expect, nothing you don't.

**Habits** — Track your daily habits with a 7-day grid. Add your own habits (with an emoji), tap the day dots to check them off, and watch your streak grow. Delete ones you've stopped caring about.

**AI Assistant** — A real Claude-powered chat that knows your tasks. Ask it to help you prioritize, analyze your progress, or just add a task by typing something like `add task: Review docs, work, high priority`. It actually reads your data, not fake demo responses.

**Analytics** — Charts built from your real task history. Weekly activity bar chart, monthly completion trend, category breakdown, and a GitHub-style activity heatmap — all reflecting what you've actually done.

**Focus Mode** — A full-screen Pomodoro timer with ambient sounds (rain, ocean, lo-fi). Hit start and get to work.

**Skills & Roadmap** — Track your learning progress across different skills with a visual roadmap.

**Rewards** — XP and levels based on how many tasks you complete. Badges unlock when you hit real milestones.

---

## How to use it

Just open the HTML file in any browser. That's it.

1. Download `taskflow-ai-v3.html`
2. Open it in Chrome, Firefox, Safari, or Edge
3. Enter your name and start adding tasks

Everything saves automatically to your browser's localStorage, so your data is there the next time you open it.

---

## The AI chat

The AI assistant uses the Anthropic Claude API. If you're running this locally without an API key wired up, it'll still work — it just falls back gracefully and shows your task stats without calling the API.

If you want live AI responses, you'll need to set up the API key in the fetch headers inside the `sendAI()` function.

---

## No dummy data

Starting fresh means starting empty. The app doesn't pre-fill fake tasks or habits to make it look busier than it is. Everything you see came from you. Analytics charts will fill up as you actually use it.

---

## Tech

Single HTML file. No build step, no npm install, no framework. Just:

- Vanilla JavaScript
- Chart.js (loaded from CDN) for the charts
- Google Fonts for typography
- Anthropic Claude API for the AI assistant
- localStorage for persistence

Works offline (except the AI chat, which needs internet).

---

## Customization

There's a **Customize** panel on the right edge — click it to:

- Change your display name
- Switch between dark and light mode
- Pick an accent color
- Set your focus ambient sound

---

## File structure

```
taskflow-ai-v3.html   ← the whole app, one file
README.md             ← you're reading it
```

---

## Known limitations

- Data is stored in the browser — clearing site data will wipe everything. Consider exporting tasks manually if you need a backup.
- The AI context window includes up to your last 8 pending tasks, so very large task lists won't fully reflect in AI suggestions.
- Focus Mode ambient audio requires browser permission and may not work in all environments.

---

Built for personal use. Feel free to fork, modify, and make it yours.
