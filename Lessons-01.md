### Collaborating with Git

#### QUESTIONS TO ASK PARTICIPANTS TO GAUGE KNOWLEDGE LEVEL
1. How familiar are you with the unix command line? How often do you work with it?
2. Have you used git before?
2. On a scale of 1-5 (1=novice/beginner, 5=expert) what kind of git user are you?  (how often do you use git in your work? once a week, once a day, once a month)
3. Have you used GitHub before?
4. Have you collaborated on a project on GitHub before?

### Git vs GitHub
#### Git
- Git is the command line version control system (VCS) software which works on your local computer.
- Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development.
- You need Git to use GitHub. You can use Git locally without GitHub.

#### GitHub
- GitHub is an internet hosting service for git repositories. Public repos are free; private repos are paid.
- As a shared space for repos, it allows you to do collaborative work.


### Two Common Collaborative Work Flows
#### Shared Repository Model
- For small projects where you are basically in the same physical space (e.g. lab with offices near each other).
- Be careful! You are cloning the main repository.
- Everyone has push and pull access to the central repo.
- Never commit to the master directly.
- Always do your work on branches and then .
-

#### Basic Shared Repository Workflow
- update your local repo with `git pull origin master`,
- create a working branch with `git checkout -b MyNewBranch`
- make your changes on your branch and stage them with `git add`,
- commit your changes locally with `git commit -m "description of your commit"`, and
- upload the changes (including your new branch) to GitHub with `git push origin MyNewBranch`
- Go to the main repo on GitHub where you should now see your new branch
- click on your branch name
- click on "Pull Request" button (URC)
- click on "Send Pull Request"



#### Fork and Pull Model
- This is the model used by U of T Coders on its own website and repos.
- The "owner"/"Project Leader" of the upstream repo assigns rights to "Collaborators"
- Collaborators do not have push access to main (upstream) repo
- Project Lead accepts Pull Requests (PRs) fro collaborators, reviews them, then merges them into main repo.


#### Some Git Terminology/Jargon
**Repos and Branches**
Term | Description
-----|------------
Origin (repo) | Your remote repo; it is the "origin" for your local copy. Either it is a repo you created yourself or it is a fork of someone else's GitHub repo.
Upstream (repo)| The main repo from which you forked your GiHub repo.
Local (repo) | The repo on your local computer.
Master | The main branch (version) of your repo.


**Basic Commands/Actions**
Term | Explanation
---| ---
Fork | Make a copy of someone else's GitHub repo in your own GitHub repo.
Clone | Make a copy of the your GitHub repo on your local computer.  In CLI: 'git clone' copies a remote repo to create a local repo with a remote called `origin` automatically set up.
Pull | Term used in collaboration. You incorporate other people's changes into your repo.
Add | Adding snapshots of your changes to the "Staging"  area.
Commit | Takes the files as they are in your staging area and stores a snap shot of your files (changes) permanentaly in your Git directory.
Push | Term used in collaboration. You "push" your files (changes) to the remote repo.
Merge | Incorporate changes into the branch you are on.
Pull Request | Term used in collaboration. You "issue a pull request" to the owner of the upstream repo asking them to pull your changes (accept your work).



#### Configuring git global settings on your local computer
(You only have to do this once; global settings apply to all your git repos)
Note: Any Local settings you initiate within individual git repositories will over ride global settings.
- username
- email
- display colours
- preferred text editor


Command line git syntax is: ```git verb```

>```$ git config --global user.name "Albert Einstein"```
>```$ git config --global user.email   "bertie@worlduniversity.edu"```
>```$ git config --global color.ui "auto"```

Use your own name and email address instead of Einstein's. This user name and email will be associated with your subsequent Git activity, which means that any changes pushed to a Git host server will include this information.

For this lesson, we will be interacting with GitHub and so the email address used should be the same as the one used when setting up your GitHub account. If you are concerned about privacy, please review GitHub’s instructions for keeping your email address private. If you elect to use a private email address with GitHub, then use that same email address for the ```user.email``` value, e.g. ```username@users.noreply.github.com``` replacing ```username``` with your GitHub one. You can change the email address later on by using the ```git config``` command again.

Set up your favorite text editor (default editor):

>```$ git config --global core.editor "nano -w"```
>```$ git config --global core.editor "atom --wait"```

See https://swcarpentry.github.io/git-novice/02-setup/ for settings for other text editors


### Solo Practise
This is mainly the 10 mins GitHub "Hello World" tutorial
https://guides.github.com/activities/hello-world/

#### A. Create a Remote Repo in your GitHub Account

  1. In URC, click **+**, then select **New repository**
  2. Name your repository ```Kathy's Project```.
  3. Write a short description.
  4. Select **Initialize this repository with a README**.

#### B. Create a Branch

1. Click drop down at top of file list that says *branch: master*.
2. Type a branch name, `readme-edits`, into the new branch text box.
3. Select the blue *Create branch* box or hit "Enter" on your keyboard. Notice you are now on the code view of your `readme-edits` branch, which is a copy of `master`.

#### C. Make and commit changes










#### Create a Local Repo




##### Add Files to Your Local Repo





#### Clone Your GitHub Repo onto Your Local Computer



#### Forking Someone Else's Repo (via GitHub website)



#### Command Line Set Up for Cloning a Repo
