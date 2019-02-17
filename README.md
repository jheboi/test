# test
Repository to help with learning Git. 

## Cloning the repository. 
To clone this repository, go into a folder where you want to store this repository and then type in the following command into your **Git Bash** program. `git clone https://github.com/jheboi/test.git`. This will create local git repository containing all source code in the repository, as well any remote branches on the remote Git Repository. 

To see all the available branches in the repository, type in the command into **Git Bash** `git branch -a`. This will show all the local repositories in **white**, and all the remote repositories in **red**. To check out any branch, type in the command `git checkout branch-name`, and it will bring up the source code for that branch. In this case you can do this with the branches _develop_ and _master_. To check out the master branch of this repository, type in `git checkout master`. Then you can type in `git checkout develop` to see the source code for the develop branch. 


## Editing your files
I like to use Visual Studio Code which can be downloaded [here](https://code.visualstudio.com/docs/?dv=win). It is a text editor that can support a multitude of programming and scripting languages, along with downloadable tools and features. 

## About repositories
A repository contains code that is relevant to a particular project. For instance, if you are writing code for an app, that code is stored within the repository. There are other things that can be stored within a repository. You can store:

* README's (like this one)
* Configuration files (perhaps for IDEs)
* Source Code
* Any other files related to that source code

There are programs that can create repositories, such as Git and SVN, however this project and other projects pertaining to JHEBOI will be **Git** repositories. Next we will find out what Git is and how to drive it. 


## Git
Git is a version control system that tracks _changes_ to code rather than storing snapshots of code. It is a great tool to allow multiple developers to work together, and work on the same source code together, yet independantly. One team member could be making changes to part of a code, whilst another member is able to change another part of the code simulataneously with almost no interference. This can be done by the way Git works. It tracks changes to code. Once changes are made, they can be _merged_ into a, what we call, _master_ branch. All changes that are made will end up being merged into a master branch, which is the version of the software that is considered the most stable version. In order for multiple developers to work on code, they create a branch off another branches. Branches are one of the most fundamental features of Git, and we will discuss this in the next section. 

### Branches
Say you have a customer who uses your program, and wants a new feature added to your app. Normally, you would create a backup of your most stable version of the app, and then proceed to work on it. Once finished, that version you finished now is the most recent version of the app. 

Now say you were working on a feature, and then unexpectedly, a customer reports a critical bug that needs to be addressed immediately. All the work you have been working on is now, pretty much, pointless, as you will need to make changes to the code which override the code you have been working on. In order to get back to working on your feature, you will now have to work on the version that just had its bug fixed. You can see now that this is an extremely ineffective method, and is even worse if working on hundreds of features. Lets replay this scenario, but use Git branches instead. 

You want to work on a new feature for your app, so you create a branch off the most stable branch of your source code, i.e., your _master_ branch. You now work on this, and while working on it, a customer has reported a critical bug that needs to be fixed immediately. Your colleague now branches off the _master_ branch and starts working on to fix the big, while you proceed to work on your feature. Once your colleague has finished working on his bugfix, he proceeds to merge in his work into the _master_ branch and once you finish your feature, you merge into the _master_ branch too. 

As you can see, the latter situation sounds the most effective. Two developers were able to work on the same source code without affecting each other's work. All thanks to branches. 


### Branch Hierarchy 
In most situations, you are going to have **TWO** main branches. These are your, previously mentioned, _master_ branch, and a _develop_ branch. The _master_ branch is always considered your most recent and stable version of the code. The _develop_ branch is used as a testing grounds of all features and bugfixes that have been made to the _master_ branch. 

Usually, if a feature needs to be developed, or a bugfix needs to be created, you will branch off your _master_ branch. Lets call this **Branch A**. Once **Branch A** is complete, you will _merge_ it into your _develop_ branch. Then you can test your _develop_ branch and make sure that your change you made has not affected the rest of the code and works as it should. Once everyone has agreed that **Branch A** is stable, then you can merge it into your _master_ branch. 

Notice how anything that needs to be added or fixed is branched off the _master_ branch, and then is merged into _develop_ to test out the changes? This is the technique that is used most of the time:

1. Branch off _master_ branch to work on feature or bugfix
2. Once finished developing branch, merge into _develop_
3. Repeat **1** and **2** for any other features/bugfixes that need to be done
4. Test your _develop_ branch and get everyone to sign off on it. 
5. Merge back into _master_

