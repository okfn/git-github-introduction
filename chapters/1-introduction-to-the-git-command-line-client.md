Introduction to the GIT command line client
===========================================

Let's get started with git - the git command line client. If you're on Mac
OS X you should just be able to open a terminal, if you're on windows: the
git client comes with something called the git bash - start that one.

In both cases you should be able to type ```git``` in your terminal and get
some output (other than command not found). You'll see a help page.

Creating a repository
---------------------

Let's create a repository first: this is usually the first step to start
working on a *new* project. It's really simple and quick: just make a new
directory, change to the new directory and initialize git

```
mkdir my-new-project
cd my-new-project
git init
```

Adding files
------------

Next thing you want to do is to add a file to the repository. Simply create
a new text-file (e.g. with notepad) and save it to the directory where you
initialized your git repo. Then add it using git add. 

```
git add myfile.txt
```

Committing changes
------------------

Next we need to let git know of the changes you did. This is called
"committing". We'll call git commit and add a message to what we are
committing. - Our first commit is the initial commit - so I'll just call it
that

```
git commit -m "initial commit"
```

note the quotation marks around the message. We do need to commit changes
everytime to do this. If you change your file again you either need to
add the file again for committing or use ```git commit -a -m "my message"```

Looking back
------------

Now it's time to look back to what we did.

```
git log
```

gives you an overview of the last commits that were made (and by whom).
Notice the commit ids (the long strings of numbers and letters) - they are
quite useful. e.g. if you want to know what changed between them you can do

```
git diff <the commit id>
```

to see changes since that commit (e.g. your last) - or 

```
git diff <first commit> <second commit>
```

to see changes between to commits.
Alternatively you can use 

```
git show <the commit id>
```

to see the commit itself. - this helps you understand what people have
done.

Cloning a repository
--------------------

Until now we've only worked on a repository alone - imagine we'd want
others to collaborate with - or we want to contribute to someone's project.
We'll need to clone the original repository.

Cloning is basically copying with the whole information attached to it -
plus git remembers where your current repository comes from and makes it
easy to update it if the original changes.

Let's clone our sample project

```
cd ..
git clone my-new-project new-project
cd new-project
```

This will create a directory called new-project, next to my-new-project
(the first parameter of clone is what to clone - in this case the directory
my-new-project - into the directory new-project) NOTE: you can clone from
various sources including the internet (using urls - you'll see that
later). 

Now we can edit the files in new-project and commit the changes... (see
above).

If we change back to the original directory we can *pull* the changes in.

```
cd ../my-new-project
git pull ../new-project master
```

This will update the original with the changes you committed in the cloned
branch. - NOTE: the second argument tells you which "branch" to clone - use
"master" unless you understand branches or told to use another one.

Of course you could do this the other way around - and pull in changes made
to the original repository (in this case, you can just type ```git pull```
since git knows where you cloned from)


