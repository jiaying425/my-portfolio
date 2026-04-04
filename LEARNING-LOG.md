# GitHub Learning Log

## Session 1 — March 29, 2026

### What I completed
| # | Concept | Command |
|---|---|---|
| 1 | Clone repo | `git clone <url>` |
| 2 | Create branch | `git checkout -b feature/homepage` |
| 3 | Create file | `echo '<h1>...</h1>' > index.html` |
| 4 | Stage changes | `git add index.html` |
| 5 | Commit | `git commit -m "Add homepage"` |
| 6 | Push to GitHub | `git push origin feature/homepage` |
| 7 | Pull Request | Via GitHub UI |
| 8 | Sync local main | `git pull origin main` |
| 9 | Deploy | GitHub Pages |

### Live site
https://jiaying425.github.io/my-portfolio/

---

## Session 2 — April 1, 2026

### What I completed
| # | Concept | Command |
|---|---|---|
| 1 | Create GitHub Issues | Via GitHub UI |
| 2 | Auto-close issues on merge | `Closes #N` in PR description |
| 3 | Check current branch | `git branch` |
| 4 | Stage multiple files | `git add file1 file2` or `git add .` |
| 5 | Stage nested file | `git add .github/workflows/deploy.yml` |
| 6 | Write file in Terminal | `cat > file << 'EOF' ... EOF` |
| 7 | Delete junk file | `rm index.htmlC` |
| 8 | Add to .gitignore | `echo ".DS_Store" >> .gitignore` |
| 9 | Update token scope | GitHub Settings → Tokens (classic) → workflow |
| 10 | GitHub Actions workflow | `.github/workflows/deploy.yml` |

### Key lessons
- Always run `git branch` before committing and pushing
- `git push origin <branch>` sends to wherever you specify — commits attach to the branch you are ON
- `>` overwrites a file, `>>` appends to it
- `git checkout -b` creates the branch locally only — `git push` uploads it to GitHub
- `.git` folder is the brain of the repo — git only works inside the repo folder
- Each file needs its own `git add` — HTML linking CSS means nothing to git

### Issues completed
- [x] #4 Add About section
- [x] #5 Add Projects section
- [x] #6 Add Contact section
- [x] #7 Style with CSS
- [x] #8 Set up GitHub Actions CI

---

## Session 3 — April 2, 2026

### What I completed
| # | Concept | Tool |
|---|---|---|
| 1 | Real portfolio content | HTML |
| 2 | Improved CSS styling | CSS |
| 3 | VS Code Terminal | `Ctrl+`` ` |
| 4 | VS Code Explorer | `Cmd+Shift+E` |
| 5 | Emmet shortcut | `!` + Tab = HTML boilerplate |
| 6 | Quick open file | `Cmd+P` |
| 7 | Comment/uncomment | `Cmd+/` |
| 8 | Multi-cursor editing | `Opt+Click` |
| 9 | Select next match | `Cmd+D` |
| 10 | Git panel in VS Code | Branch icon in sidebar |

### Key lessons
- VS Code Terminal is identical to Mac Terminal — same zsh, same git commands
- VS Code opens already inside your project folder — no need to `cd` first
- Emmet generates HTML from shorthand — `section#about` + Tab = `<section id="about"></section>`
- Git panel in VS Code shows visual diff — green = added, red = removed
- `code .` opens the entire project folder in VS Code

### Issues completed
- [x] #15 Update portfolio with real bio and content
- [x] #16 Improve CSS styling
- [x] #17 Learn VS Code shortcuts

---

## Session 4 — April 3, 2026

### What I completed
| # | Concept | Command |
|---|---|---|
| 1 | View commit history | `git log` |
| 2 | Compact commit history | `git log --oneline` |
| 3 | See uncommitted changes | `git diff` |
| 4 | See staged changes | `git diff --staged` |
| 5 | Compare to last commit | `git diff HEAD index.html` |
| 6 | Stash work temporarily | `git stash` |
| 7 | List stashes | `git stash list` |
| 8 | Restore stashed work | `git stash pop` |
| 9 | Discard local changes | `git restore index.html` |
| 10 | Add navigation bar | HTML + CSS |
| 11 | Clone repo on Windows | `git clone <url>` |

### Key lessons
- `git log --oneline` is the most readable way to view history
- `git diff` compares working file to last commit — green = added, red = removed
- `git restore` resets a file to its last committed state
- `git stash` saves work without committing — `git stash pop` brings it back
- Mismatched quotes in commit messages cause `quote>` prompt — use `Ctrl+C` to cancel
- Always press `Ctrl+S` in VS Code to confirm file is saved before staging
- Windows needs git installed separately — Mac has it pre-installed

### Issues completed
- [x] #20 Learn git log, git diff, git stash
- [x] #21 Add navigation bar

### Next session
- [ ] Responsive design (mobile-friendly CSS)
- [ ] Add a profile image
- [ ] git revert and git reset
