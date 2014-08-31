This is a note about learning GIT
-- Starting from 2014-8-31

1. The procedure of updating files stored should be like this: 
	<1> modify the files
	<2> add file to git (git add xxxx)
	<3> commit the change(git commit -m "String of comments")
   Notice that we cannot make the commit before adding the file to the verson controlling system. 
2. The procedure moving back to the last verson is like this. 
	git reset --hard HEAD^
   Notice: HEAD stands for present verson, where HEAD^ stands for last verson. You can go to even earlier verson by cascading more '^' characters. 

