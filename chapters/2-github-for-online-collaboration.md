Github for online collaboration
===============================

Since git is great to allow collaboration - you can make changes and ask
other people to get them from you - plattforms have sprung up to facilitate
this procedures. The most popular one right now is github. 

What github does is host git repositories for you and other users and
facilitate the cloning and pulling process.

Take for example the git repository having this tutorial - it lives on
github and anyone on the internet can simply clone it - to have a local
copy to work with. 

Publishing/Creating a repository on Github
------------------------------------------
If you want to create a new repository or publish one of your projects
that is already a git repository. There is a small "create a new repo"
![create-new-repo](img/create-new-repo.png) button. Click this and github
will walk you through the commands of doing so.

Contributing to a team project
------------------------------
In many cases you will want to contribute to a project. In some cases you
might have direct access to the repository (e.g. it's an OKFN project and
you are in the OKFN group) - then you can simply clone, edit, commit your
changes and then push your changes.

e.g.

```
git clone <URL>
... EDIT some file ...
git add <file>
git commit -m "describe your edits"
git push
```

This will push your changes.

Pull Requests - Contributing to a project where you're not a team member
------------------------------------------------------------------------

If you're not part of the team - that means you can not push to the
repository you want to contribute you'll need to go the following route
(this is by some considered a better method of changing things...)

* you'll need to fork the project on github (click on the "fork" button) ![fork](img/fork.png)
* clone your own repository, commit and push as above (all to your own
  clone on github)
* issue a pull request by: clicking on the "compare-and-review button" 
* in the comparison view click on "Click to create pull request" on the top ![pull-request](img/pull-request.png)
* this will issue a pull request that let's the original contributors see
  your changes and allow them to accept the changes (or just ignore them)

Issues
-------

Another nice feature on Github are issues: a simple way to track bugs,
feature requests etc. You'll find them in the original repository with the
"issues" tab on the side. If you discover a bug, request a feature etc. Do
so with issues. Simply put in a new issue (the green button on the top
right) for something you want to have.

If you decide to address an issue, you can mention you do so in the commit
message. Simply putting a #[number] in there will link your commit to an
issue. Writing "fixes #[number]" in the commit message will close the issue
automatically. Don't worry, if you work a while with github, you'll get the
hang of it.

Now, let's try that out:
*Add a file describing yourself to the participants directory in this
repository.*


