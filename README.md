# new-computer-setup
This repository contains information regarding what to do when setting up a new UNIX computer for development. It showcases a step by step list that details the steps required for Fredrik to become happy with his new computer.

## What to do:

1. Go to **System Settings**.
    1. Change right click to be in the bottom right corner instead of two fingers being used.
    2. Change the screen to not enter resting mode when the charger is connected.
    3. Scale the screen so that windows aren't too large.
2. Open the **Terminal**.
    1. Change the colour scheme to something visually appealing (for instance blue on a black background). Make sure the cursor is a line and not a block.
3. Download **Google Chrome**.
    1. After **Chrome** has been downloaded, make sure it is set to the default browser. This can be set in the **General** section of the **System Settings**.
4. In the **Terminal**, write `git --version`. This will prompt the computer to download the **Xcode Command Line Tools**. Install these.
5. Install **git**. This can be done here: https://git-scm.com/downloads.
6. Follow the **GitHub** guide to generate an **SSH key** for **GitHub** and all other **git** distributions you are using. The guide can be found here: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/.
    1. Make sure you do not forget the step of adding a `config` file in the `.ssh` folder, containing information regarding adding the **SSH key** to your **keychain**.
7. Download **ATOM**. This can be done here: https://atom.io/.
    1. In the header menu, press *Atom* and then *Install Shell Commands*. This will make it possible to open **ATOM** files via the **Terminal** using `atom`.
    2. Change the **Settings** to use spaces (*Soft tabs*) instead of tabs (*Hard tabs*). Also change the *tab length* to `4`.
8. Install **homebrew**. Instructions on how to do this can be found here: https://brew.sh/.
9. Install **fish**. Instructions on how to do this can be found here: https://hackercodex.com/guide/install-fish-shell-mac-ubuntu/.
    1. Aside from what was mentioned in the guide, make sure that you change the **default shell** in the **Terminal Settings**. This is done in the **General** section, and it should be changed to `/usr/local/bin/fish`.
    2. Make sure to follow the **Basic Configuration** part as well.
    3. Change the prompt of **fish** to be *Informative VCS*.
