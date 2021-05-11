# new-computer-setup
This repository contains information regarding what to do when setting up a new UNIX computer for development. It showcases a step by step list that details the steps required for Fredrik to become happy with his new computer.

Last updated **2021-05-11**.

## What to do:

1. Download **Google Chrome**.
    1. After **Chrome** has been downloaded, make sure it is set to the default browser. This can be set in the **General** section of the **System Settings**.
2. Go to **System Settings**.
    1. Change right click to be in the bottom right corner instead of two fingers being used.
    2. Change the screen to not enter resting mode when the charger is connected.
    3. Scale the screen so that windows aren't too large.
3. Open the **Terminal**.
    1. Change the colour scheme to something visually appealing (for instance blue on a black background). Make sure the cursor is a line and not a block.
4. Install **homebrew**. Instructions on how to do this can be found here: https://brew.sh/.
5. Install **git**. This can be done here: https://git-scm.com/downloads.
6. Add your SSH key to the `.ssh` folder.
7. Install **fish**. Instructions on how to do this can be found here: https://hackercodex.com/guide/install-fish-shell-mac-ubuntu/.
    1. Aside from what was mentioned in the guide, make sure that you change the **default shell** in the **Terminal Settings**. This is done in the **General** section, and it should be changed to `/opt/homebrew/bin/fish`.
    2. Make sure to follow the **Basic Configuration** part as well.
    3. Change the prompt of **fish** to be *Informative VCS*.
    4. Add the functions you would like implemented. If you type these directly into the **Terminal**, use `funcsave` to make sure they're permanently stored. For instance, you could add the following functions:
        1. `gitcp` - commits and pushes all modified files in a **git** repository with a given commit message.
            ```
            function gitcp
            	if test (count $argv) -gt 0
            git commit -am $argv[1]
            git push
            else
            echo "A commit message must be specified."
            end
            end
            ```
        2. `mkd` - creates a directory of the given name and enters it.
            ```
            function mkd
            	if test (count $argv) -gt 0
            mkdir $argv[1]
            cd $argv[1]
            else
            echo "A directory name must be specified."
            end
            end
            ```
8. Install **fisherman**. Instructions on how to do this can be found here: https://github.com/jorgebucaran/fisher/blob/master/README.md.
    1. Use **fisherman** (with **Terminal** command `fisher`) to install **z** (https://github.com/jethrokuan/z).
9. Download **VS Code**. This can be done here: https://code.visualstudio.com/.
10. Install **python** using **brew**.
    1. **brew** will mention that symlinks to unversioned commands of **python** will be available at a given location. This location should be added to the PATH in order to use `python3` by typing `python`.
11. Install **node**. TODO: Add instructions.

That's it! You're done for now. Good job! You should now happily be able to develop whatever you want. If you realize that something is missing, please come back and add it to this list!
