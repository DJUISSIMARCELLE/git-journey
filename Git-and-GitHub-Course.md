
Git and GitHub Course
________________________________________
1. What is Git?
•	Git is a powerful tool that constantly keeps track of every change you make to your files. Git records what changed, when it changed, who changed it and even where it happened.
________________________________________
2. What kind of file are we talking about?
•	Any kind it could be an image php, video python no matter what you are working on Git tracks every single change.
________________________________________
3. Key Benefits of Git
•	Git saves every version of your file. Imagine you wrote some code and then made a few changes to it after a few days. Know you want to make sure that the old version doesn’t get lost. That’s exactly where git comes to the rescue. It lets you keep multiple versions of the same file effortlessly, and whenever you want you can roll back to any previous version in just a moment.
•	Git is most commonly used in coding projects but its power goes beyond just code. You can use git to keep track of changes and maintain different versions of almost any file
•	Git is also known as a version control system because it keeps every version of your file or code safely stored
________________________________________
4. Creator of Git
•	Git was created by LINUS TORVALDS the same brilliant mind behind Linux
________________________________________
5. Difference between Git and GitHub
•	Git is a tool that runs locally on your own computer.it tracks all the changes you make to your files and makes every thing organized while GitHub takes that organized history, uploads it to the cloud, and adds a web interface so you can easily share it, back it up, and collaborate with others.
•	GitHub acts as an online server where your team’s entire project lives, making it easy for everyone to see, edit and share updates in one place without any confusion. GitHub isn’t the only place where you can host your Git repositories there are other popular platform, too like GitLab Bitbucket.
•	GitHub is now own by Microsoft
________________________________________
6. Git Architecture
•	Git is mainly divided into two major parts Local and Remote.
•	The Local part refers to your own computer, where you do all your work. This is where your files, code and every change you make are stored. The Remote part, on the other hand lives in the cloud. Its where you push or upload your local work.
________________________________________
7. Local Git workflow
7.1 Working Directory
•	In Your computer the folder where you are working on your project is called the working directory. This is where all the action happens (Write code, create new files, modify existing ones)
7.2 Stage
•	In this phase you say to to git that your changes are ready and that they can move to the next step
7.3 Local repository
•	Here we take the staged files and send them to the local repository. you can think of this staging area as a middle ground, a temporary area where files sits between working directory and repository save and the final save in the repository.
•	Once you have reviewed everything and you are sure you work is correct you Commit it.
•	Committing means permanently saving those changes to your local repository.
________________________________________
8. What is a repository?
•	A repository is a place where all the versions of your files and their complete change history are stored
________________________________________
9. How to Install Git
9.1 Check if Git is Already Installed
Open your terminal and type:

git --version
•	If you see a version number, Git is installed.
•	If you get an error, follow the steps below.
9.2 Install Git on Windows
Method 1: Official Installer (Recommended)
1.	Go to https://git-scm.com/download/win
2.	The download will start automatically.
3.	Double-click the .exe file and follow the installation wizard.
4.	Keep most settings as default, clicking "Next" until completion.
5.	Open a new Command Prompt and type git --version to verify.
Method 2: Winget (Windows Package Manager)
winget install --id Git.Git -e --source winget
9.3 Install Git on macOS
Method 1: Xcode Command Line Tools (Recommended)
xcode-select --install
Follow the pop-up window instructions.
Method 2: Official Installer
1.	Go to https://git-scm.com/download/mac
2.	Download and run the installer.
Method 3: Homebrew
brew install git
9.4 Install Git on Linux (Ubuntu/Debian)
sudo apt update
sudo apt install git
9.5 Install Git on Linux (Fedora)
sudo dnf install git
9.6 Configure Git After Installation
After installing, introduce yourself to Git:
git config --global user.name "Your Full Name"
git config --global user.email "your-email@example.com"
Verify your configuration:
git config --list

9. Steps for Creating a Local and Remote Repository (For Absolute Beginners)
If you have never created a repository before, follow these two parts carefully. Part A is done entirely on your own computer. Part B is done on a website like GitHub.
________________________________________
Part A: Creating a Local Repository (On Your Computer)
A local repository is just a normal folder on your computer that Git is watching. Here is how to create one from scratch:
Step 1: Create a new project folder
Open your terminal (Command Prompt, Git Bash, or Terminal) and type:
mkdir my-new-project
(This makes a new, empty folder called "my-new-project")
Step 2: Move into that folder
cd my-new-project
(This changes your current location to inside that new folder)
Step 3: Initialize Git (Turn it into a repository!)
git init
(This creates a hidden. git folder inside your project. Your normal folder is now a Git repository!)
Step 4: Create a file to track
echo "Hello World" > readme.txt
(This makes a simple text file)
Step 5: Stage the file
git add readme.txt
(This tells Git to start watching this specific file)
Step 6: Commit the file (Save it to your local repository)
git commit -m "My first commit: added readme.txt"
________________________________________
Part B: Creating a Remote Repository (On the Cloud - e.g., GitHub)
Now you will make an identical copy of your local repository and put it on GitHub so it is backed up and shareable.
Step 1: Log in to GitHub
Go to github.com and log into your account. (Create a free account if you don't have one).
Step 2: Create a new remote repository
•	Click the "+" icon in the top-right corner of the GitHub page.
•	Select "New repository" from the dropdown menu.
Step 3: Fill in the details
•	Type a name for your repository (e.g., my-new-project - it doesn't have to match your local folder name, but it helps).
•	Leave it as Public (or choose Private if you prefer).
•	DO NOT check the box that says "Add a README file" (since you already have a local readme.txt, checking this will cause confusion later).
•	Click the green "Create repository" button.
________________________________________
Part C: Cloning a Remote Repository (Downloading a GitHub Project to Your Computer)
What if the repository already exists on GitHub and you just want to bring a copy of it down to your machine? That is called cloning. You do not need to run git init when cloning—Git does it automatically for you.
Follow these steps to clone any existing GitHub repository to your computer:
Step 1: Find the repository URL on GitHub
•	Go to the GitHub page of the repository you want to copy.
•	Click the green "Code" button.
•	In the dropdown menu, make sure the "HTTPS" tab is selected.
•	Copy the URL (it looks like https://github.com/username/repository-name.git).
Step 2: Open your terminal
Open your Command Prompt, Git Bash, or Terminal.
Step 3: Navigate to where you want to put the folder
Decide where on your computer you want the project to live. For example, to put it on your Desktop, type:
cd Desktop
(Or stay in your home folder if you prefer)
Step 4: Run the clone command
Type git clone followed by the URL you copied, then press Enter:
git clone https://github.com/username/repository-name.git
(Git will now download the entire project—every file, every folder, and the complete history of all changes—straight to your computer!)
Step 5: Move into your newly cloned project
After the download finishes, a new folder with the repository's name will appear. Go inside it:
cd repository-name
(Replace repository-name with the actual name of the folder that was just created)
Step 6: Verify everything is there
Check the downloaded files and history:
dir
(This lists all the files. You can also run git log --oneline to see the full commit history that was downloaded!)
________________________________________
10. How to Check for Modifications and See Exactly What Changed
After you edit, delete, or add files to your project, Git gives you two powerful commands to check your work: git status and git diff. They work together but tell you different things.
________________________________________
10.1 Checking if Git Detected Your Modification (git status)
This is your first check. It tells you which files have been changed, but it does not show you the actual lines of text or code that were modified.
How to use it: type this in your terminal
git status
What you will see:
•	If Git has detected your change, the file will appear in red under a section called:
o	"Changes not staged for commit:" (if it's a file Git already knows about)
o	"Untracked files:" (if it's a brand new file Git has never seen before)
How to tell git to keep those changes
You tell Git to keep your changes by saving them permanently to your repository's history. In Git terms, this is called committing.
However, it is a two-step process (Stage + Commit). Here is exactly how to do it right now:
________________________________________
Step 1: Stage the changes (Tell Git which changes to keep)
If you have modified a file (like one.txt) and you want to keep it, you must first add it to the Staging Area.
The process of moving changes from the working directory to staging area is called adding
Command:
git add one.txt
(Or, if you want to keep all the changes you made in the entire folder, use git add –all or git add -A or git add .)
Command	Stages New Files?	Stages Modified Files?	Stages Deleted Files?	Includes Hidden Files (e.g., .gitignore)?	Affects
git add *	 Yes	 Yes	 No (ignores them)	No (ignores them)	Only current folder
git add .	 Yes	 Yes	 Yes	Yes	Only current folder
git add -A (or --all)	 Yes	 Yes	Yes	Yes	Entire repository

What this does: It tells Git, "Hey, I want these specific changes to be included in my next save."
If you want to go back to the previous state that is remove everything from the staging area and return them to the working directory
Command:
git reset
A normal reset only brings back the stage changes not the actual files. I f you want to restore everything ie both the changings and the deleted files then run git reset --hard 
________________________________________
Step 2: Commit the changes (Permanently save them)
Once the file is staged (turning green in git status), you lock it in by creating a commit.
Command:
git commit -m "Your descriptive message here"
What this does: It takes everything that is green (staged) and permanently burns it into your local repository's history. Git will now remember this version forever.
If you want to undo a commit type this command git reset HEAD~. This command will undo the last commit and bring it back to the working directory
If you want to delete a file and stage that deletion Instead of deleting the file manually (with del in Windows or rm in Mac/Linux) and then running git add separately, git rm does both steps in one shot:
•	It deletes the file from your working directory (your actual computer folder).
•	It stages that deletion (adds it to the Staging Area) so it's ready to be committed.
Just type the command: git rm filename.txt
How to view Commits
Viewing commits means checking the commit logs. And doing that is very simple. In the terminal just type git log 
________________________________________
Branching
11. What is Branching in Git?
Branching is like a separate line of development where you can work independently.
________________________________________
11.1 The Simple Analogy (Think of a Tree)
•	Imagine your project is a tree trunk (the main or master branch). This is the safe, working version of your code.
•	A branch is like a new branch growing out of that trunk. You can climb onto this new branch and do whatever you want—experiment, build new features, try crazy ideas—without affecting the main trunk.
•	Once you are happy with your work on the new branch, you can merge it back into the main trunk, bringing all your new changes with it.
________________________________________
11.2 Why Do We Use Branches?
•	To work on new features without breaking the main project.
•	To experiment safely—if the experiment fails, you just delete the branch, and the main project stays perfectly safe.
•	To fix bugs without disturbing other work.
•	To collaborate with teams—each developer can work on their own branch and merge later.
________________________________________
11.3 Key Branching Terms
Term	Meaning
Main (or Master)	The default, primary branch. Usually contains the stable, production-ready version of your project.
Feature Branch	A separate branch you create to work on a specific feature or fix (e.g., add-login, fix-bug-123).
Checkout / Switch	The action of moving from one branch to another.
Merge	The action of bringing the changes from one branch into another (e.g., merging your feature branch back into main).
Delete Branch	Removing a branch after it has been merged (keeps your repository clean).
________________________________________
11.4 The Basic Branching Workflow (Step-by-Step)
Here is exactly how you use branches as a beginner:
Step 1: Check which branch you are on right now
git branch
(The branch with a * star next to it is your current branch.)
Step 2: Create a new branch
git branch new-feature
NB. Whenever you create a new branch it inherits the current state of the branch you are in.
(This creates a new branch called new-feature, but you are still on your old branch.)
Step 3: Switch to your new branch
git switch new-feature
(Or use the older command: git checkout new-feature)
Pro Tip: You can create AND switch in one command:
git switch -c new-feature
(The -c means "create and switch"
To switch back to the main branch, type the same command “git checkout main”. And when switching back to the main branch what ever file you created in the new branch will not be found in the main branch 
Why? 
Because the changes maid in the new branch exist only in that branch. Those changes haven’t been merged into the main branch yet.
NB always commit the changes maid In the new branch
The moment you switch to the main branch git automatically hides the changes made in the new branch, showing you only what exist in that main branch.
Step 4: Merge 
1.	Merge the main branch to the new branch: this takes all the commits in the main branch and apply it to the new branch. To do that type this command in your new branch git merge main -m “merging main into new branch name”
2.	Merge the new branch to the main branch. git merge new branch name -m “merging main with new branch name
________________________________________
12. Handling Merge Conflicts (What Happens When Two Branches Clash!)
A merge conflict happens when two different branches change the exact same line in the exact same file, and Git does not know which change to keep.
________________________________________
12.1 The Simple Analogy (The "Two Editors" Problem)
Imagine you and a friend are both editing the same paragraph of a book:
•	You change the sentence to: "The cat sat on the mat."
•	Your friend changes the exact same sentence to: "The dog sat on the rug."
When you try to combine (merge) your work, Git gets confused and says: "Wait! You both changed the same line! Which one is correct? I need you to decide!"
That confusion is a merge conflict.
________________________________________
12.2 Why Do Merge Conflicts Happen?
•	Two branches modify the same line(s) of the same file.
•	One branch deletes a file while another branch modifies that same file.
•	Git cannot automatically decide which change is correct—so it asks you to make the decision.
________________________________________
12.3 What Does a Merge Conflict Look Like?
When you try to merge and a conflict happens, Git gives you this message:
text
Auto-merging one.txt
CONFLICT (content): Merge conflict in one.txt
Automatic merge failed; fix conflicts and then commit the result.
Git stops the merge and marks the conflicted file.
When you open that file (e.g., one.txt) in your text editor, you will see something like this:
text
<<<<<<< HEAD
The cat sat on the mat.
=======
The dog sat on the rug.
>>>>>>> feature-branch
Here is what each symbol means:
Symbol	Meaning
<<<<<<< HEAD	The start of the changes from your current branch (the one you are on).
=======	The dividing line between the two conflicting versions.
>>>>>>> feature-branch	The end of the changes from the other branch (the one you are trying to merge).
________________________________________
12.4 How to Resolve a Merge Conflict (Step-by-Step)
Follow these exact steps when you hit a conflict:
________________________________________
Step 1: Check which files have conflicts
git status
Git will show you the conflicted files in red, under a section called: "Unmerged paths:"
________________________________________
Step 2: Open the conflicted file in your text editor
Open the file (e.g., one.txt). You will see the conflict markers (<<<<<<<, =======, >>>>>>>).
________________________________________
Step 3: Decide what to keep
You have three choices:
•	Keep your current branch's changes (the HEAD version).
•	Keep the other branch's changes (the feature-branch version).
•	Keep BOTH (combine them into something new).
________________________________________
Step 4: Edit the file and remove the markers
Manually edit the file to look exactly how you want it to look in the final version.
Make sure to DELETE:
•	The <<<<<<< HEAD line
•	The ======= line
•	The >>>>>>> feature-branch line
Example:
If you want to keep the dog version, your final file should just look like:
text
The dog sat on the rug.
If you want to keep both, it could look like:
text
The cat sat on the mat. The dog sat on the rug.
________________________________________
Step 5: Stage the resolved file
Once you have saved the file and removed all the conflict markers, tell Git you have fixed it:
git add one.txt
(This tells Git: "I fixed the conflict in this file. It is ready to be committed.")
________________________________________
Step 6: Commit the merge
Complete the merge by creating the final commit:
git commit -m "Resolved merge conflict in one.txt"
Git will automatically create a merge commit, and you are done! 🎉
________________________________________
12.5 Emergency Exit: Abort the Merge
If the conflict is too confusing, or you just want to start over completely, you can abort (cancel) the merge entirely. Git will take you back to exactly how things were before you tried to merge.
The Command: git merge –abort
What it does: It cancels the merge and returns your repository to the state it was in before the git merge command was run. All your files go back to normal.
________________________________________
13. Switching to a Particular Commit (Traveling Back in Time)
Sometimes you want to go back to an exact moment in your project's history—not just to look, but to actually be in that moment. Git lets you do this by checking out a specific commit.
________________________________________
13.1 The Analogy (The "Time Machine")
Imagine your project is a book with many chapters. Each commit is a chapter.
•	Switching to a specific commit is like opening the book to Chapter 5 instead of reading the latest Chapter 10.
•	You can read it, explore it, and even start writing a new story from that exact point!
________________________________________
13.2 The Important Warning: "Detached HEAD"
When you switch to a specific commit (not a branch), Git puts you in a state called "Detached HEAD".
What does that mean?
•	HEAD in Git means "where I am right now".
•	Normally, HEAD points to the latest commit on your branch (like main).
•	When you switch to an old commit, HEAD detaches from the branch and points directly to that specific old commit.
The Danger:
•	If you make new commits while in a detached HEAD state, they are not connected to any branch.
•	If you switch away without creating a branch, those new commits can get lost forever (Git will eventually delete them).
The Golden Rule:
If you want to make changes from an old commit, always create a new branch first!
________________________________________
13.3 Step 1: Find the Commit Hash (The "Address")
Before you can switch, you need the commit's unique ID (hash).
Command:
git log --oneline
Example output:
text
af0d4c5 (HEAD -> main) Resolved conflict: kept Branch version2
3b18e51 Changed one.txt on main branch
c4e0b3d Changed one.txt on test-conflict branch
2a1b3c4 My first commit
The hash is the first 7 characters (e.g., 3b18e51). This is your time machine's "address".
________________________________________
13.4 Step 2: Switch to That Commit
Once you have the hash, type:
git switch --detach 3b18e51
(Replace 3b18e51 with your actual commit hash.)
Older alternative (still works):
git checkout 3b18e51
What happens:
•	Your entire project folder instantly changes to look exactly as it did at that moment.
•	Your terminal will warn you: "You are in 'detached HEAD' state."
________________________________________
13.5 How to Go Back to Normal (Attach HEAD Again)
To go back to your latest work on main, simply switch back to your branch:
git switch main
(Your project instantly returns to the latest version. All your old commits are still safely there.)
________________________________________
14. How to Compare Two Commits (Spot the Difference)
Sometimes you want to see exactly what changed between two different points in your project's history—without actually traveling back in time. Git lets you do this easily with the git diff command.
________________________________________
14.1 The Analogy (The "Spot the Difference" Game)
Imagine you have two photos of the same room, taken at different times.
•	One photo is from January (Commit A).
•	The other photo is from February (Commit B).
You want to see what moved, what was added, and what was removed between the two photos. Git's git diff does exactly this—but for your files and code!
________________________________________
14.2 The Basic Command
To compare two commits, you need their commit hashes (the unique IDs you see in git log).
The Command: git diff commit-hash-A commit-hash-B
Example:
git diff 3b18e51 af0d4c5
What it does: Git shows you the exact lines that are different between Commit A and Commit B.
Every thing we’ve seen so for is inside our local repository meaning we have staged files, made commits and stored everything locally. But our main goal is to send those local changes to a remote repository, that process is called a Push. And if any changes have been made in the remote repository that you want to bring into a local repository, we use Fetch. 
When you run git fetch, the remote changes are downloaded into your local repository memory, but it won’t appear in your directory yet. To actually update your working directory and see those changes in your files, you need to run git pull.
So in short:
 push means sending local changes to the remote
 Fetch means bringing remote changes into your local repository, but not merging them yet.
 Pull means fetching plus merging-so your working directory immediately reflects the remote changes
To push you local changes to the remote type git push origin main
Typing this you also have to push your different branches. First move to that branch by typing git checkout branch name then git push origin branch name
If there is an update is the remote repository and you want to bring the latest changes from the remote to the local main branch first make sure you are in the local main branch then run git fetch after run git merge.
Git pull command automatically performs both the fetch and merge commands
Git restore command
Imagine you are working on a project you start developing a new feature writing a lot of code and modify several existing files after some time you realize that the approach you too isn’t working at all by the you have already make changes to 10 0r 15 files some with new code some heavily modify. in this situation you want to discard every thing and go back to the previous state.Now think about it will you really upon those ten to fifteen files manually remove all the new lines and try to restore the old code one by one. How even could that possibly be probably not at all. In this case the simplest answer is not possible and this is where the magic of the git restore command comes in
What is git restore?
git restore is Git's modern, safer way to undo changes. It helps you revert any file or directory back to its previous state that is to the state of the last commit. It is mainly used to undo local uncommitted changes or remove changes that were added to the staging area using git add. It was introduced to make two common tasks much simpler and less confusing:
1.	Unstage files (remove them from the Staging Area).
2.	Discard changes (throw away your edits and go back to the last committed version).
Before git restore, beginners had to use git reset for unstaging and git checkout -- for discarding—which was confusing because those commands did many other things too. git restore does exactly what it says: it restores files to a previous state.
If you want to restore...	You type...
A single file	git restore one.txt
A whole directory (folder)	git restore myFolder
Everything in the current directory (all files + subfolders)	git restore .

If you want to unstage...	You type...
A single file	git restore --staged filename
A whole directory	git restore --staged myFolder
Everything in the current directory	git restore --staged .
15. Git Stash (Temporarily Saving Your unfinished Work)
Sometimes you are in the middle of working on a new feature, and you realize you need to switch to a different branch to fix a bug or to do some thing immediately.
But you haven't finished your work yet. You do NOT want to commit half-written, broken code.
Git Stash is the solution! It takes all your uncommitted changes, saves them in a safe. "storage closet" (like a drawer), and then puts your working directory back to the state of your last commit.
To do this first move to the the branch you want to work on git will show you an error. Git it self will tell you to either commit or stash your file before switching
 
After you stash them you will now be able to move to the new branch.you will notice that your unfinished feature isn’t there any more.it is save in the stash. To bring it back you just need to pop it out of the stash using the command git stash pop  
Difference between pop and app commands
Command	What it does	Does it delete the stash after applying?
git stash pop	Applies the stash AND deletes it from the stash list.	 Yes (removes it)
git stash apply	Applies the stash BUT keeps it in the stash list.	No (keeps it saved)
To see your stash list type git stash list 

16. Git Revert (Safely Undoing a Commit)
Sometimes you make a commit and realize: "This was a mistake! I need to undo it."
But the problem is: other people might already have your commit (if you pushed it to GitHub).
If you use git reset to delete the commit, you are rewriting history—and if others have already pulled your changes, this will cause chaos for your team.
git revert is the solution! Instead of deleting the commit, it creates a brand new commit that undoes the changes from the old commit. History stays intact, and everyone stays happy.
________________________________________
16.1 The Analogy (The "Correction" vs "Eraser")
Imagine you are writing a book, and you already published Chapter 10.
•	git reset → You rip out Chapter 10 from every copy of the book and pretend it never happened. Anyone who already has the book is confused because their copy has Chapter 10 but yours doesn't.
•	git revert → You leave Chapter 10 exactly as it is, but you write a new Chapter 11 that says: "Ignore everything written in Chapter 10. Here is the correct version."
Now everyone has the same history. The mistake is still visible in the book, but it has been corrected.
git revert is the safe, team-friendly way to undo commits.
________________________________________
16.2 The Basic Command
Step 1: Find the commit hash you want to undo
git log --oneline
Step 2: Revert that commit
git revert commit-hash
Example:
git revert 3b18e51
What happens:
1.	Git looks at
2.	 commit 3b18e51 and figures out what changed.
3.	Git creates a new commit that does the exact opposite.
o	If the old commit added "Hello" → the new commit removes "Hello".
o	If the old commit deleted "Goodbye" → the new commit adds "Goodbye" back.
4.	Git opens your text editor so you can write a commit message.
5.	You save and close the editor, and Git creates the new commit.
Revert vs Reset
Command	What it does	Does it rewrite history?	Is it safe if you already pushed?
git revert	Creates a new commit that undoes the old one.	 No (history stays intact).	 YES! Safe for shared branches.
git reset --hard	Deletes the commit completely and moves HEAD back.	✅ Yes (rewrites history).	 NO! Dangerous if others have your commits.
The Golden Rule:
•	If you have NOT pushed to GitHub → you can use reset.
•	If you HAVE pushed to GitHub → always use revert to avoid breaking your teammates' work.



