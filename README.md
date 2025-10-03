# Adding model-act as a Git Submodule

To include [model-act](https://github.com/LarryMarzanJr/model-act.git) in your project, follow these steps:

1. Navigate to your main repository:
   ```bash
   cd /path/to/your/main-repo
   ```

2. Add the model-act repo as a submodule:
   ```bash
   git submodule add https://github.com/LarryMarzanJr/model-act.git libs/model-act
   ```
   
   > Here, `libs/model-act` is the folder where the submodule will be placed.
   You can change this path to fit your project structure.

3. Initialize and fetch the submodule:
   ```bash
   git submodule update --init --recursive
   ```

4. Commit the changes to your repository:
   ```bash
   git add .gitmodules libs/model-act
   git commit -m "Add model-act as submodule"
   ```

---

## Updating the Submodule

To pull the latest changes from the model-act repository:
```bash
cd libs/model-act
git pull origin main   # or another branch
cd ../..
git add libs/model-act
git commit -m "Update model-act submodule"
```

---

## Cloning a Repo with Submodules

When cloning a repository that already contains submodules (like model-act), use:
```bash
git clone --recurse-submodules <repo-url>
```

If you've already cloned the repo without submodules, run:
```bash
git submodule update --init --recursive
```
