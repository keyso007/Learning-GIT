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
   Notice: HEAD stands for present version, where HEAD^ stands for last version. You can go to even earlier version by cascading more '^' characters. 

3. User 'git reflog' to find your previous operations on the version control, and get version numbers for each of the previous modified versions. 

# 2014-9-1
1. Use 'git checkout -- filename' to clear changes that not added to git. (Using 'git add filename')
2. Creating new branches. 
	<1> git branch branchName   -> Creating a new branch
	<2> git checkout branchName -> Switching to the newly created branch
	<3> git branch              -> Check currently existing branches, the branch with '*' is current location
	----------------------------   There is an alnative approach
	<1> git checkout -b branchName -> Creat and switch to a newly created branch

3. Merge branches
	<1> git checkout branchName -> Switch to the branch you want to merge (Usually the master branch)
	<2> git merge branchName2   -> Merge the changes in branchName2 to branchName
	<3> git branch -d branchName -> Delete the previous branch
   Notice: After merging, branchName2 still exist. You have to manually delete the branch if you will not use it anymore. It is not likely to recover the deleted branch unless you have a copy of it online. 

4. # Your branch is ahead of 'origin/master' by n commits.
	<1> When this line is displayed, it means your local files are not synchronous with that on github. 
	<2> git push origin master  -> Push local master branch to origin branch on github
   Notice: 
   	<1> git push origin branchName, the branchName is not necessarilly 'master'. In many scenarios, for example you want to push a new branch to github sever, namely 'make', then it's nonsense' to excute 'git push origin master' since all your modification is not on 'master' branch. Instead, you should execute 'git push origin make', then you can see a new branch on github. 
	<2> The 'push' operation is done in unit of branch. The incluence will be confined to only one branch on github sever. 

5. Observe the topology of the workspace
	<1> --graph          -> Topology display
	<2> --abbrev-commit  -> Short version of Hash
	<3> --pretty=oneline -> Single line for each commit
   Example: git log --graph --pretty=oneline --abbrev-commit

6. Download a branch from github
	<1> git checkout -b localBranch origin/branchName -> fetch the branch from sever

