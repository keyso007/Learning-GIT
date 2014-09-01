This is a note about learning GIT
-- Starting from 2014-8-31

# 2014-8-31
1. The procedure of updating files stored should be like this: 
	<1> modify the files
	<2> add file to git (git add xxxx)
	<3> commit the change(git commit -m "String of comments")
   Notice that we cannot make the commit before adding the file to the version controlling system. 

2. The procedure moving back to the last version is like this. 
	git reset --hard HEAD^
   Notice: HEAD stands for present version, where HEAD^ stands for last version. You can go to even earlier version by cascading more '^' characters.` 

3. User 'git reflog' to find your previous operations on the version control, and get version numbers for each of the previous modified versions. 

# 2014-9-1
1. Use 'git checkout -- filename' to clear changes that not added to git. (Using 'git add filename')
2. Creating new branches. 
	<1> git branch branchName   -> Creating a new branch
	<2> git checkout branchName -> Switching to the newly created branch

