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

---

## Session 5 — April 4, 2026

### What I completed
| # | Concept | Command |
|---|---|---|
| 1 | Undo a pushed commit safely | `git revert <SHA>` |
| 2 | Revert the most recent commit | `git revert HEAD` |
| 3 | Accept revert commit message | `Esc` → `:wq` → `Enter` in vim |
| 4 | Abort a failed revert | `git revert --abort` |
| 5 | Unstage last commit | `git reset HEAD~1` |
| 6 | Discard unstaged changes | `git restore <file>` |
| 7 | Add viewport meta tag | `<meta name="viewport" ...>` |
| 8 | Add media queries | `@media (max-width: 600px)` |
| 9 | Test mobile in Chrome | DevTools → phone icon |

### Key lessons
- `git revert` is safe for pushed commits — adds a new undo commit, never deletes history
- `git reset` removes commits from history — only use before pushing
- Reverting old commits causes merge conflicts — always revert recent commits
- `git revert --abort` cancels a failed revert cleanly
- `git reset HEAD~1` unstages the last commit but keeps file changes
- Viewport meta tag is required for mobile — without it, phones zoom out
- `@media` queries apply CSS only below a certain screen width

### Issues completed
- [x] #23 Learn git revert and git reset
- [x] #24 Make portfolio responsive for mobile

---

## Session 6 — April 4, 2026

### What I completed
| # | Concept | Tool |
|---|---|---|
| 1 | Branch protection rules | GitHub Settings → Branches |
| 2 | Require PR before merging | Branch protection UI |
| 3 | Bypass rules as solo dev | Uncheck "Require approvals" |
| 4 | Add profile image | HTML `<img>` tag |
| 5 | Create images folder | `mkdir images` |
| 6 | Move file in Terminal | `mv source destination` |
| 7 | Handle filenames with spaces | Wrap in quotes or rename first |
| 8 | Style circular image | `border-radius: 50%` in CSS |
| 9 | Stage image file | `git add images/profile.jpg` |

### Key lessons
- Branch protection blocks direct pushes to main — everything goes through a PR
- Approval requirement is optional for solo projects — keep the PR requirement, drop approvals
- `git add` remembers staged files until commit — like a shopping basket
- Filenames with spaces or apostrophes break Terminal — always rename before moving
- `mv` moves files, `cp` copies files
- `border-radius: 50%` makes any square image a circle
- `object-fit: cover` ensures image fills the circle without distortion

### Issues completed
- [x] #26 Set up branch protection rules
- [x] #27 Add profile image

---

## Session 7 — April 5, 2026

### What I completed
| # | Concept | Tool |
|---|---|---|
| 1 | GitHub Projects Kanban board | GitHub UI → Projects tab |
| 2 | Create board columns | To Do, In Progress, Done |
| 3 | Link issues to board | Add item → `#` to reference issues |
| 4 | Drag cards across columns | Visual progress tracking |
| 5 | Smooth scroll | `scroll-behavior: smooth` |
| 6 | CSS transitions | `transition: property duration ease` |
| 7 | Hover scale effect | `transform: scale(1.05)` |
| 8 | Background hover | `li:hover { background: #f8f8f8 }` |
| 9 | Page fade in animation | `@keyframes fadeIn` |

### Key lessons
- GitHub Projects is a Kanban board linked to your issues — real teams use this daily
- Drag issues across columns to track progress visually
- `transition` makes CSS changes animate smoothly instead of jumping
- `transform: scale()` grows or shrinks an element on hover
- `@keyframes` defines a reusable animation sequence
- `scroll-behavior: smooth` requires no JavaScript — pure CSS

### Issues completed
- [x] #29 Set up GitHub Projects Kanban board
- [x] #30 Add CSS hover effects and animations

---

## Session 8 — April 12, 2026

### What I completed
| # | Concept | Command |
|---|---|---|
| 1 | Fork a repo | GitHub UI → Fork button |
| 2 | Clone your fork | `git clone https://github.com/jiaying425/Hello-World.git` |
| 3 | Add upstream remote | `git remote add upstream <original-repo-url>` |
| 4 | View all remotes | `git remote -v` |
| 5 | View all branches | `git branch -a` |
| 6 | Create branch on fork | `git checkout -b add-greeting` |
| 7 | Push to fork | `git push origin add-greeting` |
| 8 | Open PR to original repo | GitHub UI → PR from fork to upstream |
| 9 | Leave code review comment | Files changed → click blue + icon |
| 10 | Sync fork with upstream | `git pull upstream master` |
| 11 | Push sync to fork | `git push origin master` |

### Key lessons
- Fork when you don't have write access to a repo — branch when you do
- `origin` = your fork, `upstream` = the original repo
- A remote is just a saved URL nickname — like a contact in your phone
- `git remote -v` shows fetch and push URLs (usually identical)
- Older repos use `master`, newer repos use `main` — just a naming convention
- Fork sync cycle: `git pull upstream master` → `git push origin master`
- `-a` flag on `git branch` shows all branches (local + remote)
- PR review comments attach to specific lines of code — this is how teams give feedback

### Issues completed
- [x] #39 Session 8: Learn collaborative workflow (fork, PR review)

---

## Session 9 — April 12, 2026

### What I completed
| # | Concept | Command |
|---|---|---|
| 1 | Create annotated tag | `git tag -a v1.0 -m "First portfolio release"` |
| 2 | List all tags | `git tag` |
| 3 | Push tag to GitHub | `git push origin v1.0` |
| 4 | Push all tags at once | `git push origin --tags` |
| 5 | View tag details | `git show v1.0` |
| 6 | Create GitHub Release | GitHub UI → Releases → New release |

### Key lessons
- Tags are fixed bookmarks on a specific commit — they never move
- Branches move forward with new commits — tags don't
- Lightweight tags are quick bookmarks; annotated tags store author, date, and message
- Annotated tags are the standard for production releases
- `git push` does NOT push tags by default — you must push them explicitly
- GitHub Releases add a download page with release notes on top of a tag

### Issues completed
- [x] #40 Session 9: Learn Git tags and releases

---

## Session 10 — April 12, 2026

### What I completed
| # | Concept | Tool |
|---|---|---|
| 1 | Run Lighthouse audit | Chrome DevTools → Lighthouse tab |
| 2 | Understand Performance score | Measures load speed, image optimization |
| 3 | Understand Accessibility score | Checks alt text, color contrast, semantic HTML |
| 4 | Understand Best Practices score | HTTPS, no console errors, web standards |
| 5 | Understand SEO score | Meta description, title tag, mobile-friendly |

### Key lessons
- Lighthouse is a built-in Chrome tool that scores sites on 4 categories (0–100)
- Green (90+) is the goal for all categories
- Lighthouse tells you exactly what to fix and why — standard check before shipping
- Keep Chrome in the foreground during the audit or it fails (NO_FCP error)
- Alternative: use https://pagespeed.web.dev for online Lighthouse audits
- TODO: Run full Lighthouse audit on Windows and fix any issues found

### Issues completed
- [x] #41 Session 10: Lighthouse audit and final portfolio polish

---

## Course Complete!

### Skills mastered
- **Git fundamentals**: clone, branch, add, commit, push, pull, merge
- **Collaboration**: fork, upstream remotes, PR review, code comments
- **History & undo**: log, diff, stash, revert, reset, restore
- **Releases**: tags (lightweight & annotated), GitHub Releases
- **GitHub features**: Issues, PRs, Actions CI, Projects Kanban, branch protection, Pages
- **Web development**: HTML, CSS, responsive design, animations, navigation
- **Tools**: VS Code, Terminal (Mac & Windows), Chrome DevTools

### Portfolio
- **Live site**: https://jiaying425.github.io/my-portfolio/
- **Repository**: https://github.com/jiaying425/my-portfolio
- **Release**: v1.0
