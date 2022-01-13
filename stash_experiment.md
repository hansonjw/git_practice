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