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

### Next session
- [ ] Personalise portfolio with real content
- [ ] Learn `git stash`, `git log`, `git diff`
- [ ] Add more GitHub Actions automation
