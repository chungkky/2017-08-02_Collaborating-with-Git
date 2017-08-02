## Collaborating with Git

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
- Everyone has push and pull access to the central repo, so be careful and:
  - Never commit to the master directly.
  - Always do your work on a different branch from master.

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


### Some Git Terminology/Jargon
#### Repos and Branches

Term | Description
----- | ------------
Origin (repo) | Your remote repo; it is the "origin" for your local copy. Either it is a repo you created yourself or it is a fork of someone else's GitHub repo.
Upstream (repo)| The main repo from which you forked your GiHub repo.
Local (repo) | The repo on your local computer.
Master | The main branch (version) of your repo.


#### Basic Commands/Actions

Term | Explanation
---| ---
Fork | Make a copy of someone else's GitHub repo in your own GitHub repo.
Clone | Make a copy of the your GitHub repo on your local computer.  In CLI: 'git clone' copies a remote repo to create a local repo with a remote called `origin` automatically set up.
Pull | You incorporate changes into your repo.
Add | Adding snapshots of your changes to the "Staging"  area.
Commit | Takes the files as they are in your staging area and stores a snap shot of your files (changes) permanentaly in your Git directory.
Push | You "push" your files (changes) to the remote repo.
Merge | Incorporate changes into the branch you are on.
Pull Request | Term used in collaboration. You "issue a pull request" to the owner of the upstream repo asking them to pull your changes into their repo (accept your work).



### Configuring git global settings on your local computer
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


### Solo Practise via the GitHub GUI
This is mainly the 10 mins GitHub "Hello World" tutorial
https://guides.github.com/activities/hello-world/

#### A. Create a Remote Repo in your GitHub Account

  1. In URC, click **+**, then select **New repository**
  2. Name your repository ```Kathy's Project```.
  3. Write a short description.
  4. Select **Initialize this repository with a README**.

#### B. Create a Branch

1. Click drop down at top of file list that says **branch: master**.
2. Type a branch name, `readme-edits`, into the new branch text box.
3. Select the blue **Create branch** box or hit "Enter" on your keyboard. Notice you are now on the code view of your `readme-edits` branch, which is a copy of `master`.

#### C. Make and commit changes
You are now on your `readme-edits` branch.  

  1. Select the `README.md` file.
  2. Click on the pencil icon (URC) of the file view.
  3. Edit the file. Write something about yourself and your project.
  4. Write a commit message at bottom of screen.
  5. Click the **Commit changes** button.

#### D. Open a Pull Request (PR)

1. Click on the **Pull Request** TAB, which takes you to the PR page
2. Click on the green **New Pull Request** button.
3. Select the branch you made, `readme-edits`, to compare with the original, `master`.
4. Review your work.
5. Name your pull request and give it a brief description. You can use @mention in your description to ask for feedback by specific persons.
6. Click on the green **Create Pull Request** button.

#### E. Merge your Pull Request
You will merge your  `readme-edits` branch into your `master` branch.  

1. Click on the green **Merge pull request** button.
2. Click **Confirm merge**.
3. You can now delete the branch


### Two Person Practise via GitHub guides  
One of you is the Project Lead. The other will be the Contributor.

#### A. Project Lead: Create a Remote Repo in your GitHub Account

  1. In URC, click **+**, then select **New repository**
  2. Name your repository ```Kathy's Project```.
  3. Write a short description.
  4. Select **Initialize this repository with a README**.\
  5. Give your partner the URL to your repo.

#### B. Project Lead: Add a File
1. Click **New file**
2. Give the file a name.
3. Put some content in the file.
4. Write a commit message at bottom of screen.
5. Click the **Commit changes** button.

#### C. Project Lead: Make a Label
1. Click on **Issues** tab.
2. Click on the **Labels** box.
3. Add a label called ".............."

#### D. Project Lead: Make an Issue
1. Click on **New Issue** button.
2. Give it a title and brief description. You can use @mention in your description to ask for specific feedback.
3. Give it a label.

#### E. Contributor: Comment on an Issue
1. Go to the PL's repo.
2. Click on the **issues** button to see all the issues.
3. Select the one you wish to respond to.
4. Make a comment, introduce yourself and volunteer to work on the issue.

#### F. Project Lead: Reply to a comment
1. From your own repo, select the commented issue.
2. Write a reply.
3. Assign the issue to yourself so you can monitor it and answer questions, etc.

#### H. Contributor: Fork and Branch
1. Go to your own GitHub account.
2. Find the Lead's repo and fork it.
3. Create a branch in your forked repo (see previous Solo practise for instructions)
4. Give the branch a name which indicates the feature or change you're working on.

#### I. Contributor: Do Work and Commit
1. Make changes in this branch.
2. When you are done, write a commit message, and click on the **Commit changes** button.

#### J. Contributor: Make a Pull Request to the Upstream Repo
1. Select **Pull Request** tab.
2. Click on **New Pull Request**
3. Make sure you've selected the correct branch where you've made your edits.
4. Name your pull request and provide a brief description (you might wish to include a reference to the related issue #).
5. Click on the green **Create Pull Request** button.

#### K. Project Lead: Review the Pull Request
1. Review changes made by contributor.
2. You can send comments back and forth to discuss the work. Thank your contributor.

#### L. Project Lead: Merge the changes
1. Click on the **Merge pull request** button.
2. Close the issue; additional remarks and thanks.





### Miscellaneous Tasks
#### Create a Local Git Repo (via CLI)
1. Go to the directory which you wish to make into a Git repo: `$ cd ~/GitRepos/MyProject`  
2. Initialize the directory as a Git repo: `git init`.
3. Confirm that it worked by looking for the hidden `.git` file in your directory: `ls -a`


#### Forking Someone Else's Repo (via GitHub website)
1. Go to someone else's repo and click on the **fork** button on the URC.
2. Wait while GitHub does its work.
3. Check that you now have a new repo in your GitHub account.


#### Cloning a Repo onto Your Local computer (via CLI)
```git clone URL-of-Origin-Repo Directory-Address-of-Local-Repo```  
e.g.  
```git clone https://github.com/chungkky/2017-08-02_Collaborating-with-Git.git ~/GitHubRepros_KC/2017-08-02_Collaborating-with-Git```  
