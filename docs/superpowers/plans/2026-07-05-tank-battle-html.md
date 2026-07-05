# Tank Battle HTML Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a playable single-file HTML tank battle game and publish it to GitHub.

**Architecture:** The game lives in `index.html` with embedded CSS and JavaScript. Game state is stored in small plain objects and arrays, updated by one animation loop, and rendered to Canvas.

**Tech Stack:** HTML, CSS, JavaScript Canvas, Git, GitHub CLI.

---

## File Structure

- `index.html`: Game UI, styles, state, update loop, collision logic, rendering, and input handling.
- `README.md`: Short project description, controls, and how to run.
- `.gitignore`: Ignore local preview and temporary files.

### Task 1: Project Metadata

**Files:**
- Create: `.gitignore`
- Create: `README.md`

- [ ] **Step 1: Create `.gitignore`**

```gitignore
.superpowers/
*.log
```

- [ ] **Step 2: Create `README.md`**

```markdown
# Tank Battle HTML

A small browser tank battle game built with a single HTML file.

## Play

Open `index.html` in a browser.

## Controls

- Move: Arrow keys or WASD
- Fire: Space
- Restart: Button on screen
```

- [ ] **Step 3: Verify metadata**

Run: `git status --short`
Expected: `.gitignore` and `README.md` appear as untracked files.

### Task 2: Game Page

**Files:**
- Create: `index.html`

- [ ] **Step 1: Write a minimal page test**

Check after file creation with:

```powershell
Select-String -Path index.html -Pattern '<canvas id="game"'
Select-String -Path index.html -Pattern 'function resetGame'
Select-String -Path index.html -Pattern 'function updateGame'
Select-String -Path index.html -Pattern 'function drawGame'
```

Expected before implementation: commands fail because `index.html` does not exist.

- [ ] **Step 2: Implement `index.html`**

Create a complete single-file Canvas game with controls, enemy movement, bullets, destructible bricks, steel walls, score, lives, restart, and win/loss states.

- [ ] **Step 3: Verify page structure**

Run the same `Select-String` commands.
Expected: each command returns one or more matching lines.

### Task 3: Browser Verification

**Files:**
- Use: `index.html`

- [ ] **Step 1: Serve the folder locally**

Run: `python -m http.server 8000`
Expected: local server starts and serves the project folder.

- [ ] **Step 2: Open the page and verify**

Open: `http://localhost:8000/index.html`
Expected: Canvas board renders, player tank is visible, controls respond, and restart works.

### Task 4: Publish

**Files:**
- Use: all project files

- [ ] **Step 1: Commit**

```powershell
git add .
git commit -m "feat: create html tank battle game"
```

- [ ] **Step 2: Create GitHub repository and push**

```powershell
gh repo create tank-battle-html --public --source . --remote origin --push
```

Expected: GitHub creates a public repository and pushes `main`.

## Self-Review

- The plan covers the confirmed game scope, local verification, commit, and GitHub upload.
- No placeholder tasks remain.
- File names and commands are consistent across tasks.
