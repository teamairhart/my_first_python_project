# 🚀 New Python Project Setup Checklist

Use this checklist every time you create a new Python project to ensure it’s properly organized, version-controlled, and ready to use with VS Code and GitHub.

---

## ✅ 1. Create & Open Project Folder
```bash
dev                # jumps to ~/DevProjects
mkdir MyProject
cd MyProject
code .

✅ 2. Create a Virtual Environment

# Create the virtual environment (only the first time)
python3 -m venv .venv

# Activate the virtual environment (every time you work on the project)
source .venv/bin/activate

# You will see (.venv) at the beginning of the terminal prompt

# To deactivate when done:
deactivate


✅ 3. Upgrade pip
python -m pip install --upgrade pip

✅ 4. Install Dependencies
pip install requests pandas matplotlib

Track dependencies:
pip freeze > requirements.txt

✅ 5. Initialize Git
git init
git branch -M main
git add .
git commit -m "Initial commit"

✅ 6. Create Repo on GitHub
        Go to https://github.com/new

        Name it MyProject (same as folder)

        Leave README unchecked

✅ 7. Link Local Project to GitHub
git remote add origin https://github.com/YourUsername/MyProject.git
git push -u origin main

✅ 8. Verify Setup
    Check Source Control tab in VS Code

    Run your code:
        python file.py

✅ 9. Ongoing Workflow

After changes:
        git add .
        git commit -m "Describe changes"
        git push

After new packages:
        pip freeze > requirements.txt
        git add requirements.txt
        git commit -m "Updated dependencies"
        git push

✅ 10. Optional Best Practices
    Add .gitignore to ignore .venv/ and __pycache__/

    Create a README.md with project details

    Use branches for features:
            git checkout -b feature-name


