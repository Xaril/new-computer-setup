# new-computer-setup
This repository contains information regarding what to do when setting up a new UNIX computer for development. It showcases a step by step list that details the steps required for Fredrik to become happy with his new computer.

Last updated **2018-09-13**.

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
    1. Make sure you do not forget the step of adding a `config` file in the `.ssh` folder, containing information regarding adding the **SSH key** to your **keychain**. Also, make sure that you specify the `config` file correctly if several **SSH keys** are generated.
7. Download **ATOM**. This can be done here: https://atom.io/.
    1. In the header menu, press *Atom* and then *Install Shell Commands*. This will make it possible to open **ATOM** files via the **Terminal** using `atom`.
    2. Change the **Settings** to use spaces (*Soft tabs*) instead of tabs (*Hard tabs*). Also change the *tab length* to `4`.
8. Install **homebrew**. Instructions on how to do this can be found here: https://brew.sh/.
9. Install **fish**. Instructions on how to do this can be found here: https://hackercodex.com/guide/install-fish-shell-mac-ubuntu/.
    1. Aside from what was mentioned in the guide, make sure that you change the **default shell** in the **Terminal Settings**. This is done in the **General** section, and it should be changed to `/usr/local/bin/fish`.
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
10. Install **fisherman**. Instructions on how to do this can be found here: https://github.com/jorgebucaran/fisher/blob/master/README.md.
    1. Use **fisherman** (with **Terminal** command `fisher`) to install **z**.
11. Install **python**. Instructions on how to do this can be found here: https://docs.python-guide.org/starting/install3/osx/.
    1. In case **python** isn't pointing to `/usr/local/bin` but instead to **python2** in `/usr/bin`, do the following:
        1. Add the following line to your `config.fish` file in `~/.config/fish/`: `set -gx PATH /usr/local/opt/python/libexec/bin $PATH`.
        2. Make sure your `/etc/paths` file looks like this:
            ```
            /usr/local/bin
            /usr/local/sbin
            /usr/bin
            /bin
            /usr/sbin
            /sbin
            ```
12. Install the **java JDK**. Instructions on how to do this can be found here: https://www.lonecpluspluscoder.com/2017/04/27/installing-java-8-jdk-os-x-using-homebrew/.
13. Install **IntelliJ**. Instructions on how to do this can be found here: https://www.jetbrains.com/idea/.

That's it! You're done. Good job! You should now happily be able to develop whatever you want. If you realize that something is missing, please come back and add it to this list!
