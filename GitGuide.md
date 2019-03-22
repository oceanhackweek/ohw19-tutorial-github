Git Guide.

Prerequisites:

* Watched the lecture WaterHackWeek CyberSeminar: 
[Version Control with Git and Github Video](https://www.youtube.com/watch?v=Bc5BO9gPC9w&feature=youtu.be)

* Set up git on your laptop and have your github.com account. You have also joined the Waterhackweek Github Organization.

* Test set up



# Create a project repository

One person on your team should volunteer and create a reposotory for the project under the Waterhackweek organization.

https://github.com/waterhackweek

/Users/valentina/Desktop/Screen Shot 2019-03-22 at 11.31.35 AM.png

Follow the steps: click yes to create Readme.md

* Name Format, Default
* Invite others to the repo:
	* Settings -> Collaborators

	
Note to collaborators: you will receive an invitation to your email associated with github.com. If you cannnot find it look for the `bell` notifications on your website.

## Cloning the repository.

Each participant should clone the repository so they have their local copy. Navigate through the terminal to the folder where you want to keep Waterhackweek work. (`cd path_to_folder`)

```
git clone www.github.com/waterhackweek/whw2019_ourproject/ 
```

This will create a new folder called whw2019_ourproject. Navigate to the folder.

## Updating the Readme with your name.

Open the Readme.md file with your favorite editor and add your name to the file.

Then add this change to the git tree, commit it to the local repository, and publish it on the github.com website.

```
git add Readme.md
git commit -m "Adding Valentina's name to Readme.md"
git push origin
```

Make sure you change appears online.

! Remember to run 

``` 
   git status

```
to observe the changes made into the your repository.

Pay attention to the colors.

To see the changes in the files run:

```
git diff 

```

## Updating your local repository with the changes of your collaborators. 

```
  git pull origin master

```


! Remember `origin` is just a short name of the web address of the repository.

To see the what is hidden in origin:

```
   git remote -v 

```

To practice these steps more, make more changes to the title and the description of the problem.

Ran into a problem?

When working with several people.

* cannot push because changes have been made that have not been incorporated: need to pull

* when pulling you arrive into a merge conflict


## Resolving the merge conflict

```
git status
```


You will see the file which caused the merge conflict in green.

Open it and decide which changes you want to keep. Remove the arrows.

```
git add Readme.md
git commit -m "resolving merge conflict"
git push origin
```

You can continue working on as usual.

Picture of workflow.


! Remember to pull often and push small changes to avoid messing with complicatd merges and keep your repo up to date.

## Avoiding Problems: Forked Repo workflow.

Some merge conflicts can be avoided by working with Forks.

Forks are public copies of the main repo, from which  

* Sync your local repo with the public one
* Fork the public repo
* Go to your local repo and rename your origin to point to the fork:

```
git remote rm origin
git remote add origin www.github.com/valentina-s/ourproject
```

* Add a new remote to talk to the main repo:

```
git remote add upstream www.github.com/waterhackweek/ourproject 
```


! Make sure your origin contains your github username, and upstream contains the waterhackweek name.


## Submitting Changes via a Pull Request

Make some changes to a file and commit and publish them.

```
git add 
git commit 
git push origin
```


! Note they appear on your fork, but not on the main repo.

Submit a pull request:
Snapshot of where to click.

* Write description.
* Assign somebody for review.

* Reviewer: look through changes in the file
* Approve PR or ask for more changes.

! Pending PRs.`

From now on we encourage individual members to use forks, and submit changes to the main repo with pull requests.

## Version Control and Jupyter Notebooks

* why: git diff gives rubbish
notebooks are text files, but the information is stored in json format

* split analysis in small notebooks, individual people working on individual notebooks, put longer code into functions and keep move functions to modules (.py files which work well with version control). 

* before committing clear output notebook output
(Images are stored in very long strings of crazy characters)

* you can use jupyterlab 
```
   jupyter lab
```

* nbdime: diff notebook 


## Git and JupyterHub


You can access terminal on Jupyter Hub. From there you can commit your work periodically. (More details of the repo). 


## TroubleShooting

* Deleting files
* Resetting to an older version
* 












