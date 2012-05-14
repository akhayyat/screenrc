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
