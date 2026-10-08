# Cheat Sheet: Build Your Own Course Journey Repo

Follow top to bottom. Takes about 20 minutes.

## 1. Create the repo (GitHub website)

1. Go to github.com, click **+** (top right), then **New repository**
2. Name it `cs1073` (short, lowercase, no spaces)
3. Pick **Private** if you're unsure, or Public if it's only notes
4. Check **Add a README file**
5. Click **Create repository**

## 2. Get it on your computer

```bash
git clone https://github.com/<your-username>/cs1073.git
cd cs1073
```

## 3. Make the .gitignore first

Create a file called `.gitignore` and put in anything you must never push:

```
assignments/
labs/
quizzes/
course-materials/
*.pdf
*.class
.DS_Store
```

Do this before adding any files so nothing slips in.

## 4. Build your README, section by section

Open `README.md` in a text editor and add these, in order:

1. **Title and one-line intro:** what the course is, term, why you're doing this
2. **Warning box:** one line saying what's NOT in the repo (graded work, course materials)
3. **Course info table:** course, term, instructor, lecture/lab times, textbook, LMS
4. **Marking scheme table:** components and weights from your outline
5. **Rules I'm tracking:** attendance limits, missed-assignment limits, lab rules, tech policy
6. **Weekly log:** one block per week (see template below)
7. **Key dates table:** midterm, final, deadlines
8. **Grades tracker:** your own marks as you get them
9. **Concepts checklist:** topics as checkboxes you tick off
10. **Reflections:** a spot for midterm and end-of-term thoughts

Pull everything for sections 3 to 5 straight from your course outline.

## 5. Weekly log template

```markdown
### Week N (date)
- **Topics:**
- **What clicked:**
- **What I struggled with:**
- **Lab quiz / assignment status:**
- **TA / tutorial help used:**
```

Copy it, paste it, fill it in. Newest week on top.

## 6. Markdown cheat sheet

| You want | You type |
|---|---|
| Big heading | `# Title` |
| Section | `## Section` |
| Bold | `**text**` |
| Bullet | `- item` |
| Checkbox | `- [ ] task` / `- [x] done` |
| Code block | three backticks, then code, then three backticks |
| Inline code | `` `code` `` |
| Quote / warning | `> text` |
| Link | `[label](https://url)` |
| Table | `\| A \| B \|` then `\|---\|---\|` then rows |

## 7. Save your work to GitHub

```bash
git add .
git commit -m "Week 5 notes"
git push
```

Do it every time you finish a study session.

## 8. Weekly routine (10 minutes)

1. Type up your handwritten notes into `notes/week-N.md`
2. Fill in that week's log block in the README
3. Tick off concepts you learned
4. Update the grades tracker if you got marks back
5. `git add .`, `git commit`, `git push`

## 9. Before every push, check

- [ ] No assignment, lab, or quiz code in the commit (`git status` shows what's going up)
- [ ] No instructor slides or posted materials
- [ ] No passwords or student number in any file
- [ ] Everything in the repo is something you wrote yourself

## 10. Handy git commands

| Command | What it does |
|---|---|
| `git status` | See what changed |
| `git diff` | See exact changes |
| `git log --oneline` | See your history |
| `git pull` | Get latest from GitHub |
| `git restore <file>` | Undo changes to a file |
| `git rm --cached <file>` | Stop tracking a file you added by mistake |

If you accidentally push something you shouldn't, delete it and tell me. Removing it from history needs extra steps, and it's better to fix it early.
