# Master to main

The default branch name for new Github repositories is now main. Github says, that later this year, we'll be able to rename the default branch for existing repositories. But while this is not possible, you can follow these steps:

1. Create main branch locally:
```
git branch -m master main
```

2. Push the local main branch to the remote repository:
```
git push -u origin main
```

3. Switch the current HEAD to the main branch:
```
git symbolic-ref refs/remotes/origin/HEAD refs/remotes/origin/main
```

4. [Change the default branch on Github to main](https://docs.github.com/en/github/administering-a-repository/setting-the-default-branch).


5. Delete the master branch on the remote:
```
git push origin --delete master
```

6. Perfect.