# When push or pull to main, use following commmands:
- git remote add nlfrom2008 https://github.com/nlfrom2008/jtnotes.git (Once ran on a machine, No need do again) 
- git push/pull nlfrom2008 main (for jtnotes)
- git push/pull origin master (for react01)

# How to push local dir/files to github:
1. create a new repository on the Github (react01)
2. run: git remote add origin https://github.com/nlfrom2008/react02.git
  - echo:  error: remote origin already exists.
  - if echo above message, run: git remote rm origin
3. re-run: git remote add origin https://github.com/nlfrom2008/react02.git
4. run: git push origin master
5. confirm all the directories and files have benn pushed to Github.