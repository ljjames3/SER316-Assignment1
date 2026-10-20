BRANCH SUMMARY
----------------------
Brances: main, feature1, feature2, feature3, dev, hotfix, documentation
Structure:
main branches to feature1, feature3, dev, hotfix and documentation
dev branches to feature2

Branch: main
Description: Created intial number guessing game

Branch: feature1
Description: Added the ability to quit the game with a negative number input and the play-again loop at the end of the game.
Improved user feedback messages for guesses and add verison comment documenting quit feature

Branch: dev
Description: adds an encouraging message for players

Branch: feature2
Description: branched off of dev, added maxAttempts constant and game over state as well as implements max attempts logic and game over condition

Branch: feature3
Description: unclear what was done but commit messages are started hint, got it done, had to fix, and done. 

Branch: hotfix
Description: Fix randomInt to properly include max value in range

Branch: documentation
Description: create README.md and add branch summary


LEARNING SUMMARY
-------------------
- Merge combines two branches like we did with feature 1 into dev. We deleted feature1 branch so now its commit messages are under the dev branch. Merge maintains original commits so whenever maintaining the history of the commits is necessary, this would be helpful.
- Rebase takes commits one at a time and merges them onto the branch you rebased on. In our case we rebased feature 2 onto dev. We resolved conflicts one at a time for each commit and then added them to the rebase, and continued. This makes sure the commits stay linear and you manage one commit at a time on branch rather than all commits and changes at once. Rebase updates commits so I would want to use this if I was cleaning up my commit history for some changes and to keep the commits linear so that its more clear when others read it. 
- Squash takes commits in one branch and combines them into one commit, then that commit can be merged once rather than showing many commit messages. This is nice in the case of feature3 where the commit messages didn't provide value. We squashed them into one commit and updated the message to be more helpful. If I ever need to combine some commits, or merge smaller commits with a larger one under one message for clarity and simplicity, I can use squash to combine into one to make the commit message and history clearer.
- Cherry-Pick allows you to select a single commit by its hash value and commit it to another branch without having to bring anything else from that branch. If I ever need to commit something to another branch but don't want to bring the whole branch, I can use this. Maybe I make a commit on the wrong branch, I can use this to move it too.

Feature git history observations:
feature1's merge just added everything at once, and conflicts had to be resolved and then it could be merged into dev. I could imagine in a very large git repo with many commits, this could be troublesome. feature1 maintained its original commit hash values. feature2 was branched off dev originally and we rebased it onto dev, it was given new commit hash values after resolving conflicts one by one. feature3 had unclear commit messages for its history, we combined these into one commit using squash and rebased and merged these onto dev so after resolving conflicts there was a new commit hash value and a more descriptive commit message.
