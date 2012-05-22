About This Repository
---------------------

This repository is for GNU Screen configuration files. It includes the
`.screenrc` file and any other related files that are used by the
`.screenrc` file.

Note that the name of the `.screenrc` file in the repository is
actually `screenrc` (without the dot) for convenience. You can simply
link to the file from your home directory:

     cd $HOME
     ln -s $SCREENRC_REPO_DIR/screenrc .screenrc

Requirements
------------

The current configuration assumes the following:

-   Linux

    System statistics are collected from Linux-specific pseudo-files
    in the `/proc` directory

-   Debian, or a Debian derivative

    The current scripts list the number of available updates, and use
    Debian's package manager (APT) to get that information

-   The package `gawk`

    The AWK script uses some `gawk`-only features

-   The package `apt-show-versions`

    This is also used to get the number of available updates

How to Use
----------

1.  Clone the repository to your local machine:

        cd $SCREENRC_REPO_DIR
        hg clone https://bitbucket.org/akhayyat/screenrc

2.  Set the path for the included script(s) in the `screenrc` file to
    your actual `$SCREENRC_REPO_DIR`, by editing the following line in
    the `screenrc` file:

        backtick 100 0 0 $HOME/scripts/screen/screen-stats.awk

    The default above assumes that `$SCREENRC_REPO_DIR` is `$HOME/scripts/screen/`

3.  Link the `.screenrc` file in your home directory to the `screenrc`
    file in the repository:

        ln -s $SCREENRC_REPO_DIR/screenrc $HOME/.screenrc

How it Looks
------------

![Screenshot](https://bitbucket.org/akhayyat/screenrc/raw/064acbb0294c/screenrc-screenshot.png "Screenshot")
