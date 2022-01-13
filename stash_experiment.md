# Stash Experiment
I am conducting a test to see if I truly understanding branches, and more specifically how to use `stash` when multiple users are involved

## Procedure
1. Clone this repository to two different locations, `git_user_1` and `git_user_2`
2. From here I will make changes in `git_user_1` and check those changes in
3. Next I'll make changes in `git_user_2` and attempt to check those changes in as well.
    - I expect I will not be able to check the changes in.
4. I will attempt to stash the changes in `git_user_2`...
5. Then I will pull the code from the remote repo
6. Then I will pop the `git_user_2` changes
7. I believe I need to `merge` back in the changes

This should simulate something like the following diagrams:

          0---0                 User 1
         /     \
    0---0---0---0---0---0---0   Main Branch
         \       \     /
          0---0---R---0         User 2

This file was created by `git_user_1`

## Summary and Results (user2)
This comment is by user 2.  I will attempt to stash and merge some of the code now.

## Results and Summary
I was unsuccessful in use of the `stash` command.  However, the end results illustrated above were achieved.  The lesson learned here is that stash is only really for changes that haven't been added and/or committed, nevermind merged into the remote.  As user2 I was able to commit changes, however, I was unable to push code to the remote.  The fix was rather easy in that I had to pull the code again then work through the conflicts, then commit and push code.  It really isn't as complicated as it sounds.  It would be messy and challenging if one was in a position where the changes were big and dramatic.

Next step.  I am going to push this update to the remote.  Then I will make some changes as user 2, not not commit, then utilize stash to hopefull resolve everything.

User2 comment for one last attempt at `stash`

Alas, `stash` worked...