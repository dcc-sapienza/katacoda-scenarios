### Step 1 - Set environment

In this step we will initialize the environment required for following steps.
It will consist of:

- a remote repository containing revision history
- a remote working directory containing revision history and copies of project files
- a local working directory containing revision history and copies of project files

We will see three ways of initializing a *git* repository:

- with `git init` command, which creates an empty Git repository. Running `git init` in an existing repository will create a `.git` folder and will not overwrite contents of the folder
- with `git init --bare`, which creates a bare repository. Bare repos contain no working or checked out copy of your source files and are customarily given a *.git* extension
- with `git clone <url to clone from> <directory name>` command, which creates a local copy of the repository at `<url to clone from>`, version control information included. `<directory name>` is optional

---

#### Task

- Use `mkdir` to create directory `/s/<name_surname>/` 

*Create bare remote repository* 

- Use `mkdir` to create directory `/s/<name_surname>/remote_repository`, this will simulate the remote centralized repository
- Use `git init` with `--bare` option to initialize remote repository at location `/s/<name_surname>/remote_repository/project.git` 

*Create remote working directory*

- Use `mkdir` to create directory `/s/<name_surname>/working_dir`, this will simulate another user working on the same project
- Go to `/s/<name_surname>/working_dir`
- Initialize folder using `git clone /s/<name_surname>/remote_repository/project.git`
- Go to `/s/<name_surname>/working_dir/project`
- Create file `base_feature.py`
- Add `base_feature.py` to staging area using `git add`
- Commit modification using `git commit`
- Run `git push origin master`, we will see later what it means

*Create local working directory*

- Create folder `/home/scrapbook/tutorial/<name_surname>` using `mkdir`
- Go to `/home/scrapbook/tutorial/<name_surname>`
- Initialize *git* folder using `git init`