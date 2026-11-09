# Learning Hub: Python → Data Science → ML → MLOps → LLMs

My single home for notes, practice and projects on the road to becoming an ML / MLOps / Data Science practitioner.

**Daily routine (4 hours):**
| Block | Time | What |
|---|---|---|
| Learn | 1.5 hrs | Course lessons |
| Practice | 1.5 hrs | Write code myself, tutorial closed |
| Review | 45 min | Redo yesterday's and last week's exercises from memory |
| Document | 15 min | Update notes and cheat sheet, then commit and push |

**Rules:** never skip Review · push to GitHub every day · one course at a time · Sunday review (30 min).

---

## Repo layout

```
learning-hub/
├── README.md          <- this file (roadmap + checklist)
├── notes/             <- one short file per topic, in my own words
├── cheatsheets/       <- commands and syntax I keep forgetting
├── exercises/         <- daily practice code
├── projects/          <- bigger builds, one folder each
└── interview-prep/    <- solved problems with my explanations
```

---

## Day 1 setup (exact commands)

### 1. Install
- Python 3.12 or newer: https://www.python.org/downloads/ (on Windows, tick **"Add Python to PATH"** during install)
- VS Code: https://code.visualstudio.com/ then install the **Python** extension
- Git: https://git-scm.com/downloads
- Create a free account at https://github.com

### 2. Check everything works (open a terminal; in VS Code use Terminal > New Terminal)
```
python --version      # on Mac/Linux, if this fails, use: python3 --version
git --version
```

### 3. Tell Git who you are (one time only)
```
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### 4. Create the project folder
```
mkdir learning-hub
cd learning-hub
mkdir notes, cheatsheets, exercises, projects, interview-prep
```

### 5. Create a virtual environment
```
python -m venv .venv
```
Activate it (do this every time you open a new terminal in this project):
```
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# Windows (Command Prompt)
.venv\Scripts\activate.bat

# Mac / Linux
source .venv/bin/activate
```
You'll see `(.venv)` at the start of the line. Stop using it with `deactivate`.

Try it:
```
pip install requests
pip freeze > requirements.txt
```

### 6. Tell Git to ignore the environment
Create a file named `.gitignore` containing:
```
.venv/
__pycache__/
.ipynb_checkpoints/
```

### 7. First commit
```
git init
git add .
git commit -m "Set up learning hub"
```

### 8. Put it on GitHub
1. On github.com click **New repository**, name it `learning-hub`, do **not** add a README (you already have one), and click Create.
2. Copy the commands GitHub shows you under "push an existing repository"; they look like:
```
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/learning-hub.git
git push -u origin main
```
(GitHub may ask you to sign in through the browser the first time.)

### 9. Your everyday loop
```
git status
git add .
git commit -m "Describe what you did"
git push
```

### 10. Terminal commands to learn first
| Command | What it does |
|---|---|
| `pwd` | show the current folder |
| `ls` (Mac/Linux) or `dir` (Windows) | list files |
| `cd folder` | go into a folder |
| `cd ..` | go up one folder |
| `mkdir name` | make a folder |
| `python file.py` | run a Python file |
| `clear` | clean the screen |

---

## 12-week checklist

### Weeks 1–2: Tools + Python start
**Week 1**
- [ ] Day 1: Install everything, complete the setup above, first push
- [ ] Day 2: Learn the 10 terminal commands; practise navigating folders
- [ ] Day 3: Learn Git Branching, first levels (https://learngitbranching.js.org)
- [ ] Day 4: Finish the Learn Git Branching "Main" intro levels
- [ ] Day 5: Virtual environments: create, activate, install, freeze, deactivate. Write `notes/venv.md`
- [ ] Day 6: CS50P Week 0 (Functions, Variables) — https://cs50.harvard.edu/python
- [ ] Day 7: Sunday review; write `notes/git-github.md` and `notes/terminal.md`

**Week 2**
- [ ] GitHub Skills: "Introduction to GitHub" (https://skills.github.com)
- [ ] CS50P Week 1 (Conditionals)
- [ ] Start Exercism Python track (https://exercism.org/tracks/python), 1–2 exercises a day
- [ ] Create `cheatsheets/python.md` (variables, if/else, functions, in your own words)
- [ ] Add one small script to `exercises/` every day and push

### Weeks 3–8: Python foundations (CS50P)
| Week | CS50P topic | Extra practice |
|---|---|---|
| 3 | Week 2: Loops | Rewrite 3 old exercises from memory |
| 4 | Week 3: Exceptions | Add error handling to an older script |
| 5 | Week 4: Libraries | Practise `pip install` inside your venv |
| 6 | Week 5: Unit Tests | Write tests for one of your exercises |
| 7 | Week 6: File I/O | Build a script that reads and cleans a text/CSV file |
| 8 | Week 7: Regular Expressions, Week 8: OOP | Finish CS50P final project |

Each week:
- [ ] Finish lectures, problem sets and notes
- [ ] 2 Exercism exercises per day
- [ ] Update `cheatsheets/python.md`
- [ ] Sunday: redo 5 earlier problems from scratch without looking

### Weeks 9–12: Python for data + Jupyter + SQL
**Week 9: Jupyter + pandas**
- [ ] Install Jupyter in your venv: `pip install jupyterlab pandas matplotlib seaborn`
- [ ] Open notebooks in VS Code or run `jupyter lab`
- [ ] Kaggle Learn: Python (quick revision) and Pandas — https://www.kaggle.com/learn

**Week 10: Data cleaning + visualization**
- [ ] Kaggle Learn: Data Cleaning
- [ ] Kaggle Learn: Data Visualization

**Week 11: SQL**
- [ ] SQLBolt (https://sqlbolt.com)
- [ ] Mode SQL tutorial (https://mode.com/sql-tutorial)
- [ ] 5 SQL practice questions every day

**Week 12: First project**
- [ ] Pick a free dataset (Kaggle or a government open-data portal)
- [ ] Clean it, explore it, make 3–4 charts and write down 3 insights
- [ ] Publish it in `projects/first-data-analysis/` with its own README (what it is, how to run it, what you found)
- [ ] Update this README's checklist and plan the Machine Learning phase

---

## After week 12: the main roadmap

| Phase | Weeks (approx., at 4 hrs/day) | Focus |
|---|---|---|
| 1 | 13–16 | Data science foundations and statistics (StatQuest, *Think Stats*) |
| 2 | 17–22 | Classical ML (Andrew Ng's Machine Learning Specialization, scikit-learn) |
| 3 | 23–30 | Deep learning and transformers (Karpathy *Zero to Hero*, fast.ai, Hugging Face LLM Course) |
| 4 | 31–36 | MLOps (MLOps Zoomcamp, Made With ML: Docker, MLflow, FastAPI, CI/CD) |
| 5 | 37–44 | LLMs, RAG, agents, evaluation (DeepLearning.AI short courses, LLM Zoomcamp) |
| 6 | ongoing | Portfolio, papers, community |

---

## Progress log

| Date | What I did | Hours | Notes |
|---|---|---|---|
| | | | |
