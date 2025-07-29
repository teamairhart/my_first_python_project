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
pip install requests pandas matplotlib openai

Track dependencies:
pip freeze > requirements.txt

✅ 5. Create a .gitignore File
touch .gitignore
code .gitignore

                #Paste the following into .gitignore:

                # Ignore virtual environment
                .venv/

                # Ignore Python cache files
                __pycache__/
                *.pyc
                *.pyo
                *.pyd

                # Ignore macOS system files
                .DS_Store

                # Ignore environment variables
                .env

                # Ignore Jupyter notebook checkpoints
                .ipynb_checkpoints/

                # Ignore build/dist folders
                build/
                dist/
                *.egg-info/

                # Optional: VS Code settings
                .vscode/
                .idea/


#   ****Save the file (Cmd+S).****


✅ 6. Initialize Git
git init
git branch -M main
git add .
git commit -m "Initial commit"

✅ 7. Create Repo on GitHub
        
        Go to https://github.com/new

        Name it MyProject (same as folder)

        Leave checkboxes unchecked

        Click Create repository
        

✅ 8. Link Local Project to GitHub
git remote add origin https://github.com/YourUsername/project_name_goes_here.git
git push -u origin main

✅ 9. Verify Setup
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

✅ 10. Final Best Practices
        Always create a .gitignore before your first commit (Step 5).

        Always create requirements.txt when you install packages.

        Add a README.md to explain the project.

        Use branches for new features:

                git checkout -b feature-name

