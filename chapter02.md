# Chapter02_Concepts_Commands

> You can use the branch command to create a new branch, list all the branches in your repository, and even delete branches.

```
git branch my-first-branch
```
> Git does not report success or failure, but you can list all your branches by using the same branch command, except with no arguments.

```
git branch 

```

> creating a new branch does not mean you can start using it. To switch to another branch, you will use yet another Git command, aptly named switch, which takes one argument, namely the name of the branch you wish to switch to

```
git switch my-first-branch

```

> can invoke the git switch command with the -c (or --create) flag, giving it the name of the branch you wish to create, like so:

```
git switch -c my-first-branch

```

> Bringing the work that was done in separate branches together is called merging, and Git has a command specifically built in to do just that: merge. The git merge command allows you to combine the work done in different branches.

```
git switch master
git merge add-fall-menu 
```

> So far it’s just been you creating commits, and every time you did so, you supplied a commit message using the -m flag supplied to the commit command. However, if Git ever needs to create a commit, Git will present you with a text editor to type your commit message in. The question is—what editor should it use?
using Visual Studio Code, then fire up your terminal and run this little nugget of code.

```
git config  --global core.editor "code -w"
```

> To delete a branch, we supply the -d (or --delete) flag to git branch along with the name of the branch we wish to delete, like so:

```
git branch -d feat-home-screen
```

> Now there is a chance that you created a branch just to try out an idea or approach a problem using a different tack, and you don’t care for it anymore. You can supply the branch command with the -D (yep, uppercase D) flag to force its deletion.

```
git branch -D feat-home-screen
```