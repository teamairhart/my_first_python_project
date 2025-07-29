# 🚀 New Python Project Setup Checklist

Use this checklist every time you create a new Python project to ensure it’s organized, version-controlled, and linked to GitHub.

---

## ✅ 1. Create & Open Project Folder

```bash

        dev
        mkdir MyProject
        cd MyProject
        code .


## ✅ 2. Create a Virtual Environment

        python3 -m venv .venv
        source .venv/bin/activate

## ✅ 3. Upgrade pip

        python -m pip install --upgrade pip

## ✅ 4. Install Dependencies (if needed)

        pip install requests pandas matplotlib
        pip freeze > requirements.txt

## ✅ 5. Create a .gitignore File

Create a new file named .gitignore and then paste:

        __pycache__/
        *.pyc
        *.pyo
        *.pyd

        .venv/
        env/
        venv/

        .vscode/
        .idea/

        .DS_Store
        .ipynb_checkpoints/
        build/
        dist/
        *.egg-info/

## ✅ 6. Initialize Git

        git init
        git branch -M main
        git add .
        git commit -m "Initial commit"

## ✅ 7. Create Repo on GitHub

        Go to https://github.com/new,
        name it "Whatever_your_project_name_is", leave checkboxes unchecked, and create the repo.

## ✅ 8. Link Local Project to GitHub

        git remote add origin https://github.com/teamairhart/Whatever_your_project_name_is.git
        git push -u origin main
## ✅ 9. Ongoing Workflow

    # After making code changes
        git add .
        git commit -m "Describe changes"
        git push

        # After installing new packages
        pip freeze > requirements.txt
        git add requirements.txt
        git commit -m "Update dependencies"
        git push
      
## ✅ 10. Best Practices
        
        # Always create a .gitignore before your first commit
        # Always create requirements.txt if you install packages
        # Add a README.md to explain the project
        # Use branches for new features:
            
            git checkout -b feature-name




