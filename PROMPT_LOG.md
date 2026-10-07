# Activity 12: AI Prompting & Iterative Refinement Log

This document records the exact progression from content brief to generation prompt, along with every follow-up refinement prompt and the specific modifications made to the output.

---

## Generation Prompt 1: Initial Structured Briefing
```text
You are an expert frontend software engineer and technical designer. Build a complete, responsive, single-page portfolio blog for Ashwin Rajesh Sam, a 3rd-semester B.Tech CSE student at REVA University (SRN: R25EJ019).

The website must be written in clean semantic HTML5, modern CSS3 (with CSS variables and dark/light mode toggle support), and vanilla JavaScript.

Structure the page with these sections:
1. Navigation Bar with logo, smooth-scroll links, and theme toggle button.
2. Hero Section: Name, branch, university, 2-line bio highlighting systems programming in C, algorithms, and cloud, plus CTA buttons.
3. About Me: Detailed summary of engineering background and a 4-card metric counter (Verified Repos, LeetCode Solved, HackerRank Badge, Test Passing Rate).
4. Featured Projects: Cards for C Line Editor, LeetCode Algorithmic Suite, HackerRank 3-Star Portfolio, and Live Share Collaborative Program. Each card must include tech badges and direct GitHub repository links.
5. Skills: Categorized pill badges for Languages, Developer Tools, and Core Methodologies.
6. Contact: Cards for Email (ashwinrajeshsam@gmail.com), GitHub (AshwinRajeshSam), and LinkedIn.

Design Aesthetic: Modern, minimalist dark theme inspired by GitHub/Linear, with clean monospace accents and subtle hover transitions.
```
- **Result:** Generated the initial complete layout including `index.html`, `style.css`, and `script.js`.

---

## Refinement Prompt 1: Project Links and GitHub Accuracy
```text
The generated Projects section has generic placeholder URLs. Please update every project card to link directly to Ashwin's actual GitHub repositories:
- C Line Editor -> https://github.com/AshwinRajeshSam/activity-7-c-line-editor
- LeetCode Suite -> https://github.com/AshwinRajeshSam/activity-6-leetcode-solutions
- HackerRank Portfolio -> https://github.com/AshwinRajeshSam/activity-8-hackerrank-portfolio
- Live Share Program -> https://github.com/AshwinRajeshSam/activity-5-gitlens-liveshare
Also ensure external links open in a new tab with rel="noopener noreferrer".
```
- **Before/After Change:** Replaced all placeholder anchor tags (`#`) with fully qualified, verified repository URLs and added security attributes.

---

## Refinement Prompt 2: Dark/Light Mode Persistence & Polish
```text
Enhance the theme toggle function in script.js so that the user's theme selection (dark or light) is persisted in browser localStorage across page reloads. Also ensure the button icon switches dynamically between ☀️ and 🌙.
```
- **Before/After Change:** Added `localStorage.getItem('theme')` on initialization and updated the event listener to store the user preference.

---

## Refinement Prompt 3: Metric Highlights Counter & Styling
```text
In the About section, add a responsive metric grid highlighting 10+ Verified Repos, 9 LeetCode Solutions, ★★★ HackerRank Badge, and 100% Test Passing Rate. Ensure the cards have subtle borders and match the dark theme aesthetic.
```
- **Before/After Change:** Implemented `.highlights-grid` and styled the metric numbers with the cyan/blue accent color.
