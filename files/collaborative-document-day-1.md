![](https://i.imgur.com/iywjz8s.png)


# Day 1 Collaborative Document

2022-02-14 How to write good code: CodeRefinery

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

## 👮Code of Conduct

* Participants are expected to follow those guidelines:
* Use welcoming and inclusive language.
* Be respectful of different viewpoints and experiences.
* Gracefully accept constructive criticism.
* Focus on what is best for the community.
* Show courtesy and respect towards other community members.

## ⚖️ License

All content is publicly available under the Creative Commons Attribution License: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, type `/hand` in the chat window.

To get help, type `/help` in the chat window.

You can ask questions in the document or chat window and helpers will try to help you.

## 🖥 Workshop website

[link](https://esciencecenter-digital-skills.github.io/2022-02-14-ds-cr/)

🛠 Setup

[link]([<url>](https://esciencecenter-digital-skills.github.io/2022-02-14-ds-cr/#Setup))

## 👩‍🏫👩‍💻🎓 Instructors

Sven, Hanno, Leon

## 🧑‍🙋 Helpers
Aron, Robin, Jaro

## 🗓️ Agenda
| | |
|-|-|
|9:00| Welcome and icebreaker|
|9:30| Introduction to version control with Git|
|10:45| Coffee break|
|11:00|Introduction to version control with Git|
|12:00|Coffee break|
|12:15| Introduction to version control with Git|
|12:45| Wrap-up|
|13:00| END|

## 🧊 Icebreaker
What is your favourite sing-along (during a pub crawl, karaoke, in the shower, ...) ?
- Sven: Paradise by the dashboard light :car:
- Masa: All I Ask :microphone: :shower:
- Leon: Piano man :musical_keyboard:
- Khaleel: Hotel California, Bohemian Rhapsody
- Aron: Koningslied
- Ajey: Wish you were here
- Ecem: Dont stop me now
- Chiara: Wonderwall, Gianna
- Ediz: The Pot by Tool
- Arista: Walking in Memphis
- Meixin: You remember
- Jaro: Let it go (Frozen), all Britney Spears songs
- Ayda: The Heart Wants What it Wants, Selena Gomez
- Daniel: Wie Zuhause
- Duco: De Vlieger
- Kristi: Personal Jesus, Depeche mode
- Yanick: Iggy Pop, Passenger / many good options mentioned above
- Sjors: Raccoon - Feel Like Flying

## 🔧 Exercises

### Tracking changes exercise
Exercise in breakout rooms. Write down your (individual) answers to the next 3 questions in the collaborative notebook.

#### 1. Which command(s) below would save the changes of myfile.txt to my local Git repository?

1. ``$ git commit -m "my recent changes"``
2. ```
    $ git init myfile.txt
    $ git commit -m "my recent changes"
   ```
3. ```
    $ git add myfile.txt
    $ git commit -m "my recent changes"
   ```
6. ``$ git commit -m myfile.txt "my recent changes"``

#### 2. Committing Multiple Files
The staging area can hold changes from any number of files that you want to commit as a single snapshot.

Add some text to ``mars.txt`` noting your decision to consider Venus as a base
Create a new file ``venus.txt`` with your initial thoughts about Venus as a base for you and your friends
Add changes from both files to the staging area, and commit those changes.

#### 3. (optional) A new repository
Create a new Git repository on your computer called bio.
Write a three-line biography for yourself in a file called me.txt, commit your changes
Modify one line, add a fourth line
Display the differences between its updated state and its original state.

#### Answers

- Arista
    - Q1: 3
- Ayda
    - Q1:3
    - Q2:nano mars.txt; git add mars.txt; nano venus.txt; git add venus.txt; git commit -m "Multiple             changes in mars and venus";
    - Q3:mkdir bio; git init; nano me.txt; git add me.txt; git commit -m "Biography file was created";           nano me.txt; git diff;
- Diana
    - 3
- Esther
    - 3
- Duco
    - 3
- Khaleel
    - 3
    - nano mars.txt; nano venus.txt; git add mars.txt; git add venus.txt; git commit -m "Added Venus as a base"
    - mkdir bio; git init; touch me.txt; git add me.txt; git commit -m "Added bio"
- Yanick
    - 3
    -
    - Q3:
        `@@ -1,3 +1,4 @@`
        `I am a bioinformatician`
        `Doing a PhD``In Groningen`
        `+I prefer coding in Python`
- Ajey
    - Q1: Option 3
    - Q2:
        `git add venus.txt`
        `git commit -m "Considering Venus as base, created a file for Venus."`
    - Q3:
        `mkdir bio`
        `git init`
        `touch me.txt`
        `nano me.txt (to edit)`
        `git add me.txt`
        `git commit -m "Added my three line biography."`
        `nano me.txt (to edit again)`
        `git add me.txt`
        `git diff --staged`
- Chiara:
    - Q1: 3
    - Q2: git add mars.txt venus.txt; git commit -m "added considerations on using Venus as a base"
    - Q3: `` diff --git a/me.txt b/me.txt
    index 04cba14..50a1e02 100644
    --- a/me.txt
    +++ b/me.txt
    @@ -1,4 +1,5 @@
    -My name is Chiara
    +My name is Chiara, but friends call me Chiarella
     I am from Rome, Italy
     I am doing a PhD on MRI
    +I now live in Delft ``
- Masa:
    - Q1: 3
    - Q2: git add mars.txt; git add venus.txt; git commit -m "First thoughts about venus as a base, start notes on venus"
- Daniel
    - 3
    - git add .; git commit -m "thoughts on Venus as a base"
    - mkdir bio; git init; touch me.txt; git add me.txt; git commit -m "adds bio";
- Ecem: 3,  Q3: mkdir bio, git init; touch me.txt; git add me.txt; git commit -m"started bio"
- Luisa
    - 3
    - git add venus.txt ; git commit -m "Add venus as a posible base"
- Ediz
    - numbers change
    - done on local
    - done on local
- Krist
    - Q1: 3
- Meixin
    - 3
    - git add mars.txt; git add venus.txt; git comit -m "motified mars and venus"

#### Solution to first question
You first have to add a file to the staging area, then commit the changes. The correct answer is thus 3.:
```bash=
git add myfile.txt
git commit -m "my recent changes"
```

### Exploring history exercise
Exercise in breakout rooms. Write down your (individual) answers to the next 3 questions in the collaborative notebook.
#### 1. Recovering Older Versions of a File
Jennifer has made changes to the Python script that she has been working on for weeks, and the modifications she made this morning “broke” the script and it no longer runs. She has spent ~ 1hr trying to fix it, with no luck…

Luckily, she has been keeping track of her project’s versions using Git! Which commands below will let her recover the last committed version of her Python script called `data_cruncher.py?`

1. `$ git checkout HEAD`
2. `$ git checkout HEAD data_cruncher.py`
3. `$ git checkout HEAD~1 data_cruncher.py`
4.  ` $ git checkout <unique ID of last commit> data_cruncher.py`
5. Both 2 and 4

#### 2. Reverting a Commit

Jennifer is collaborating on her Python script with her colleagues and realizes her last commit to the project’s repository contained an error and she wants to undo it. `git revert [erroneous commit ID]` will create a new commit that reverses Jennifer’s erroneous commit. Therefore `git revert` is different to `git checkout [commit ID]` because `git checkout` returns the files within the local repository to a previous state, whereas `git revert` reverses changes committed to the local and project repositories.
Below are the right steps and explanations for Jennifer to use `git revert`, what is the missing command?

1. `________ # Look at the git history of the project to find the commit ID`
2. `Copy the ID (the first few characters of the ID, e.g. 0b1d055).`
3. `git revert [commit ID]`
4. Type in the new commit message.
5. Save and close

#### 3. Understanding Workflow and History

What is the output of the last command in
```
$ cd planets
$ echo "Venus is beautiful and full of love" > venus.txt
$ git add venus.txt
$ echo "Venus is too hot to be suitable as a base" >> venus.txt
$ git commit -m "Comment on Venus as an unsuitable base"
$ git checkout HEAD venus.txt
$ cat venus.txt #this will print the contents of venus.txt to the screen
```
1. Venus is too hot to be suitable as a base
2. Venus is beautiful and full of love
3. Venus is beautiful and full of love
   Venus is too hot to be suitable as a base
4. Error because you have changed venus.txt without committing the changes

#### Answers
- Arista
    - 5
    - git log
    - 2
- Ayda
    - 5
    - git log --oneline
    - 2
- Diana
- Esther
    - 5
    - Git log
    - 2
- Duco
    - 5
    - git log
    - 2
- Khaleel
    - 5
    - git log --oneline
    - 2
- Yanick
- Ajey
    - Q1 : Option 5
    - Q2 : `git log`
    - Q3 : Option 2
- Chiara:
    - Q1: 5
    - Q2: ``git log --oneline``
    - Q3: 2
- Masa
    - Q1: 5
    - Q2: ``git log (--oneline)``
    - Q3: 2
- Daniel
    - 5
    - git log
    - 2
- Ecem : Q1:5, Q3: Venu is beautiful and full of love, Q2: git log --oneline
- Luisa
    - 5
    - git log --oneline
    - 2
- Ediz
    - 5
    - git log
    - 2
- Krist
    - 5
    - git log
    - 2
- Meixin
    - 5
    - `git log --oneline`
    - 2
- Sjors
    - 5
    - `git log --oneline`
    - 2

#### Solution
1. Number 5 (both 2 and 4 are correct)
2. The missing command is `git log`, or `git log --oneline`
3. Number 2. The second line was not committed, so the file contains only the first line after the checkout.

### Exercises for Ignoring Things
#### Ignoring Nested Files
Given a directory structure that looks like:
```
results/data
results/plots
```
How would you ignore only `results/plots` and not `results/data`?

#### (optional) Including Specific Files

How would you ignore all `.dat` files in your root directory except for `final.dat`? Hint: Find out what `!` (the exclamation point operator) does

#### (optional) Ignoring all data Files in a Directory
Assuming you have an empty .gitignore file, and given a directory structure that looks like:
```
results/data/position/gps/a.dat
results/data/position/gps/b.dat
results/data/position/gps/c.dat
results/data/position/gps/info.txt
results/plots
```
What’s the shortest .gitignore rule you could write to ignore all .dat files in result/data/position/gps? Do not ignore the info.txt.

#### (optional) The Order of Rules
Given a .gitignore file with the following contents:
```
*.dat
!*.dat
```
What will be the result?

#### (optional) Log Files
You wrote a script that creates many intermediate log-files of the form log_01, log_02, log_03, etc. You want to keep them but you do not want to track them through git.

1. Write one .gitignore entry that excludes files of the form log_01, log_02, etc.

2. Test your “ignore pattern” by creating some dummy files of the form log_01, etc.

3. You find that the file log_01 is very important after all, add it to the tracked files without changing the .gitignore again.

4. Think about what other types of files could reside in your directory that you do not want to track and thus would exclude via .gitignore.

#### Answers
- Arista
    - In .gitignore: results/data
- Ayda
    - echo "results/plots" >>.gitingnore; git add .gitignore; git commit -m "Igonre files are created";
    - Q2: git add -f final.dat
    - Q3: Add 'results/data/position/gps/*.dat' to the .gitignore file
    - Q4: .dat files will not be ingnored anymore!
- Chiara:
    - Q1: Add to .gitignore only ``result/plots``
    - Q2: Add ``!final.dat`` to .gitignore
    - Q3: Add ``results/data/position/gps/*.dat`` to .gitignore
    - Q4: .dat files will not be ignored
    - Q5: Add to .gitignore ``log*``
- Diana
- Duco
    - `echo "results/plots/ >> .gitignore"`
    - `echo "*.dat >> .gitignore"`
    - `echo !final.dat >> .gitignore`
    -
- Esther
-
    - echo "results/plots" >> .gitignore
-
- Sjors
    - `echo "results/plots/" >> .gitignore`
    - `echo "*.dat\n!final.dat" >> .gitignore`
    - `echo "*.dat" >> ./results/data/position/gps/.gitignore`
    - Nothing is ignored
    - `echo "log_*" >> .gitignore`
    - `echo "!log_01" >> .gitignore`
- Yanick
    `echo 'results/plots/'       1>> "./.gitignore"; `
    `echo -e '*.dat\n!final.dat' 1>> "./.gitignore"; `
    `echo '**.dat' 1>> "./.gitignore"; `
    - Should not ignore anything
- Daniel
    - `echo "results/plots/" >> .gitignore'`
    - `echo "*.dat \n !final.dat" >> .gitignore`
    - `echo "*.dat" >> .gitignore`
    - Nothing will be ignored
    - `echo "log_??" >> .gitignore` - `git add log_01 -f`
- Luisa
    - echo "results/plots" >> .gitignore
    - echo "*.dat !final.dat" << .gitignore
- Ajey
    - Q1: `"results/plots" >> .gitignore`
    - Q2:
        - `*.dat >> .gitignore`
        - `!*final.dat >> .gitignore`

- Masa
    - Q1: `echo "results/plots/" >> .gitgnore`; `git add .gitgnore`;`git commit -m "..."`
    - Q2: `echo "results/*.dat \n !results/final.dat" >> .gitgnore`
    - Q3: `results/data/position/gps/*.dat`
- Meixin
    - Q1: `echo "results/plots" >> .gitignore`
    - Q2: `echo "*.dat \n !final.dat" >> .gitignore`
    - Q3: `echo "results/data/position/gps/*.dat" > .gitignore`
    - Q4:  Nothing
- Khaleel
    - echo "results/plots" >> .gitignore
    - echo "*.dat \n !final.dat" >> .gitignore
    - echo "results/data/position/gps/*.dat" >> .gitignore
    - Nothing is ignored
- Ecem
    - Q1:`echo "results/plots/" >> .gitignore ; git add .gitignore; git commit -m""`
    - Q2: `echo "*.dat \n !final.dat" >>.gitignore`
    - Q3: `echo "result/data/position/gps/*.dat" >> .gitignore
    -
- Ediz
    - 1: echo 'results/plots' >> .gitignore
    - 2: echo '*.dat' >> .gitignore && echo '!final.dat' >> .gitignore
- Krist
    - 1. echo 'results/plots' >> .gitignore
    - 2. echo '*.dat' >> .gitignore !final.data
    - 3.

#### Solution
```bash=
nano .gitignore
```
Instead of "results/", we should have "results/plots". Then results/plots is ignored, but results/data isn't.


## 🧠 Collaborative Notes

### Why version control?
- It is like an unlimited undo
- It allows many people to work in parallel

### Setting up Git
Op a terminal where you have Git available (e.g. git bash on Windows, or any terminal on Linux/Mac). Run the following command to check if Git is installed properly:
```bash=
git --version
```

First, we are going to do some configuration of Git itself.
```bash=
git config --global user.name "Your Name"
git config --global user.email "Email used for your Github account here"
git config --list
```

If you don't know a command, and you're not in a course where you can ask, Google is your friend!

Windows and Mac/Linux use different characters to indicate the end of a line in text. This can cause issues with Git. There is a setting to make it work properly.

For Mac/Linux:
```bash=
git config --global core.autocrlf input
```

For Windows:
```bash=
git config --global core.autocrlf true
```

Next, we will set the default text editor. Git wil open this for you when you commit changes to your files. You can use any editor you want. If you're unsure we recommend nano:

```bash=
git config --global core.editor "nano -w"
```

The following commands sets the name of the default branch (we will get into branches later). The recommended default, also used by Github, is "main"
```bash=
git config --global init.defaultBranch main
```

### Creating a repository
First, create a folder where the repository will be stored.

Note: The ~/Desktop folder points to a folder named "Desktop" in your home directory. You can pick any folder. This example is specific to Mac and Linux.
```bash=
cd ~/Desktop
mkdir planet-investigation
cd planet-investigation
pwd  # should print that you are in the planet-investigation directory
```

Now initalize a Git repository
```bash=
git init
```

What is a repository? It is a special kind of folder, that contains all different versions of the files you stored with Git.

```bash=
ls -a
```
This shows all files and folders, including hidden ones. You should see a hidden folder named ".git". This is where everything git-related is stored. Do not remove it!


```bash=
git status
```

If your repository has the "master" default branch, you can switch to a new branch called main with
```bash=
git checkout -b main
```

### Tracking changes
Let's create a file and see how we can record changes to it in Git.

```bash=
nano mars.txt
```

Write some random text, then save and close the file (ctrl+X, Y, enter in nano).

Now we have a file called mars.txt
```bash=
ls
cat mars.txt
```

This new file is not tracked by Git yet
```bash=
git status
```

Tell Git to keep track of the file
```bash=
git add mars.txt
git status
```

Git hasn't recorded these changes as a commit yet. To do that, we have to run another command. You then have to provide a comment to go with the commit. Try to describe your changes in your commit messages.

```bash=
git commit -m "Start notes on Mars as a base"
git status
```

The last git status command should say "nothing to commit, working tree clean", to indicate there are no pending changes.

Every time you run `git commit`, Git will store a new version of the files you added with `git add`. You can always got back to any previous commit.

You can see previous commit messages with
```bash=
git log
```

Now we can change the file. Open it again and some more text.
```bash=
nano mars.txt
cat mars.txt
git status
```

Git now sees that the file was modified. The change is not staged for commit.
Before we do that, we can ask Git to show the changes we made.
```bash=
git diff
```

```bash
git commit -m "Add concerns about effect of Mars' moons on Wolfman"
```

This didn't actully do anything! We first have to add the file to the stating area tell Git that we want to store the change.

```bash=
git add mars.txt
git commit -m "Add concerns about effect of Mars' moons on Wolfman"
```

![](https://i.imgur.com/6hxG6M4.png)

Add another line to the file
```bash=
nano mars.txt
git diff
git add mars.txt
git diff
```

The first `git diff` command should show the added text, while the second `git diff` should not give any output. Any already staged changes are not shown! If you want to see those as well, you can use
```bash=
git diff --staged
```

Commit the changes and look at the commit history
```bash=
git commit -m "Discuss concerns about Mars' climate for Mummy"
git status
git log
```

`git log` shows our three commit messages in reverse chronological order.
There are some options you can give to the `git log` command to make it look nicer, for example:
```bash=
git log --oneline --graph
```

Make a new directory in the repository.
```bash=
mkdir spaceships
git status
git add spaceships
git status
```
Git ignores empty directories, even `git add spaceships` doesn't work. Git actually only keeps track of files.
Create an empty file in the spaceships directory.

```bash=
touch spaceships/apollo-11 spaceships/sputnik-1
git status
```
Now Git sees the directory.
```bash=
git add spaceships
git status
```
Now Git is tracking both new files in the spaceships directory.
```bash=
git commit -m "Add some initial thoughts on spaceships"
```

![](https://i.imgur.com/WaW5JsT.png)


#### Exploring history
Let's change the mars.txt file once again
```bash=
nano mars.txt
cat mars.txt
```

Look at the changes. We explicitly compare the changes in mars.txt to HEAD. HEAD is where we currently are in the Git repository (think of HEAD as the current location of the playing head of a tape recorder)
```bash=
git diff HEAD mars.txt
```

We can also compare to earlier versions of the repository. For example one commit in the past, i.e. one commit before HEAD:
```bash=
git diff HEAD~1 mars.txt
```

Or 3 in the past:
```bash=
git diff HEAD~3 mars.txt
```

You can also look at the changes that were made in a specific commit:
```bash=
git show HEAD~3 mars.txt
```
It shows the changes made in the 3rd latest commit, but only those to mars.txt.

Instead of pointing to a commit using HEAD, tilde and a number, you can use git log to find the unique ID of a specific commit, and use that.

```bash=
git log --oneline
```
The unique IDs are the 7 characters before each commit message.
Using normal `git log`, it's the very long string shown above each commit.
You can use these in `git diff` and `git show` as well.

```bash=
git status
```
This still shows the modified mars.txt file. What if we want to discard the change we made? We can checkout the latest version of mars.txt as stored in Git.
```bash=
git checkout HEAD mars.txt  # NOTE: any changes that were not committed are lost!
```

`git restore` does the same thing, but is not available in older versions of Git. For now we will keep using `git checkout`.

We can restore and older versions of mars.txt with git checkout, e.g. using the ID of the older commit:
```bash=
git checkout db74c99 mars.txt  # db74c99 is the unique commit ID, it will be different for you
git status
git diff --staged
```
When you commit, the file would be reverted to its older version.
Let's go back to the latest version:
```bash=
git checkout HEAD mars.txt
```

### Ignoring things
Create a directory and some data files to mimic some real-world scenario where you have some input files (.dat files) and generated some output (.out files)
```bash=
mkdir results
touch a.dat b.dat c.dat results/a.out results/b.out
git status
```

Typically, you don't want to store data files as they can be big. Perhaps you don't want to store the results either.

Create a .gitignore file in the main folder of your repository
```
nano .gitignore
```
Add the following to it:
```
*.dat
results/
```
This will ignore any .dat files, and and files in the results directory.

Now, git only sees the .gitignore file as a change to the repository
```bash=
git status
git add .gitignore
git commit -m "Ignore data files and the results folder"
git status
```

Git warns you if you try to add a file that is ignored
```bash=
git add a.dat  # prints a warning and refuses to add the file
git add -f a.dat  # force addition of an otherwise igored file
git status --ignored  # shows ignored files
```


![](https://i.imgur.com/a4bmtAy.png)


### Remotes in Github
Open a browser, go to https://github.com and log in.
Create a new repository (use the plus sign in the top right corner)
Choose a repository name.
Put in a description (optional).
Choose between public and private. Everyone can read a public repository, but you control who can write (commit) to it. Unless you have a good reason, the default should be public.
For now we will ignore the extra options to add a README, gitignore, or license.
Finally, click create repository.

Github then gives you some options on how to add your files to the repository. The local repository (on our own computer) now needs to be connected to the remote repository on Github.

Look in the quick setup section and copy the URL to the repository. Make sure the SSH option is selected. The URL should start with `git@github.com`.

Go back to your terminal and the local repository.
Make sure you are in the main directory of the repository.
Add Github as remote with
```bash=
git remote add origin <paste URL here>
git remote -v  # shows the available remotes
```
You should see two lines: a fetch and a push remote. Fetching is for downloading code from Github, while push is for uploading your local code to Github.

We will now do some setup to configure SSH to work with Github.
```bash=
ls -al ~/.ssh
```
Check if the ~/.ssh folder exists and if there are files starting with `id_`. These files are called SSH keys.

If you don't have the SSH keys, run the following
```bash=
ssh-keygen -t ed25519 -C "your email address here"
```
Press enter a few times, the password is optional.
It will also tell you where the file is stored (e.g. `~/.ssh/id_ed25519`). Two files are generated: one ending in .pub, and one without it. The file without extension is private. Never share it, and definitely do not commit it to git! The public one is safe to share.

We can now copy the public key to Github. If you have this already set up, the following command will tell you that you have authenticated successfully:
```bash=
ssh -T git@github.com
```

To add the key to Github, first copy your _public_ key:
```bash=
cat ~/.ssh/id_ed25519.pub
```
Copy the output.

Then go back to Github.com. Click your account in the top right corner and go to settings. In the left menu, click "ssh and gpg keys". Click add new ssh key and copy your public key. You can put a descriptive title for the key. Finally click "add ssh key".

Then try the ssh command again, this time it should work.
```bash=
ssh -T git@github.com
```

With this connection set up, we can push our local repository to Github.
```bash=
git push origin main
```
This pushes the branch called "main" to the remote called "origin" (which is what we called the Github remote).

To download remote changes, run
```bash=
git pull origin main
```

Go back to your browser and your Github profile. Go to your repositories. You should now see there the files we added, and part of some of the commit messages.

## Feedback

### Tips
- Pace could be higher, but not really annoying now
- was a bit unclear if start time was 8:45 or 9:00
- Pace was a bit slow, but I still learned new commands
- If possible, make the breaks more evenly spaced apart (now: 2h till first break, but only 1h till 2nd break)
- I agree with the break remark
- The .gitignore questions could be shown better.
    - People tried to write bash code, but clearly many bash answers show the right .gitignore patterns but they added the mto the file in ways that would not work. I understand this is not a bash course. So instead maybe just ask what pattern(s) they would as to the .gitignore file.
- Questions could be a bit more challenging
-

### Tops
- Very clear instructions, step by step, good to have a learn by doing
- I liked the pace and step-by-step/code-along approach, very clear explanations. Also I like the detailed setup instructions, it makes everything so much more smoth
- very clear
- Nice idea to have the smaller break-out groups where there can be more discussion
- I like the helpers being present, it really helps keep the flow going.
- I like that random questions were asked during the coffee break regarding to what have we learned and how would we apply them to our own cases.
- Being able to ask questions really helped in my understanding of the git system

## 📚 Resources
[Example gitignore files](https://github.com/github/gitignore)
[Patterns allowed in gitignore files](https://git-scm.com/docs/gitignore#_pattern_format)
[\[advanced\] Some extra information about ways to stop tracking changes in a file that is already tracked by git](https://nwdthemes.com/2019/05/09/git-ignore-changes-in-tracked-file/)
