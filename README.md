1. [Git](#Git)
1. [Shell Hacks](#ShellHacks)
1. [Vim](#Vim)
1. [Linux Programming](#LinuxProgramming)
1. [Networking](#Networking)
1. [C programming](#CProgramming)
1. [Distributed Systems](#DistributedSystems)
1. [Regex, State Machines](#RegexStateMachines)
1. [`tmux` cheat sheet](#TmuxCheatSheet)
1. [OpenGL](#OpenGL)
1. [WebAssembly+WebGL](#WebAssemblyWebGL)


<a name="Git"></a>
# Git
1. Get clean remote branch (from [SO](https://stackoverflow.com/a/5657500))
    ```
    git checkout master
    git reset --hard origin/master
    ```
1. Squash commits (from [SO](https://stackoverflow.com/a/25357146))
    ```
    git checkout yourBranch
    git reset $(git merge-base master $(git rev-parse --abbrev-ref HEAD))
    git status
    # add stuff and commit
    ```
    Also [this](https://stackoverflow.com/questions/5189560/squash-my-last-x-commits-together-using-git) which has loads of upvotes for many of the answers. 
1. Show latest revision (from [SO](https://stackoverflow.com/questions/2231546/git-see-my-last-commit))
    ```
    git show --name-status
    git log --name-status HEAD^..HEAD
    ```
1. Show affected files in commit (from [SO](https://stackoverflow.com/a/424142))
    ```
    git diff-tree --no-commit-id --name-only -r bd61ad98
    ```
    or use `--name-status` for a bit more info. 
1. Find commit for deleted file (and restore) (from [SO](https://stackoverflow.com/a/953573))
    ```
    git log --dif-filter=D --summary
    ```
    Search for prior commit hash
    ```
    git checkout <prior-commit-hash> path/to/file.ext
    ```

<a name="ShellHacks"></a>
# Shell hacks

1. [Compile and run C programs as scripts](https://news.ycombinator.com/item?id=9144467)
1. [What's in your Bash alias file?](https://news.ycombinator.com/item?id=18898523)
1. [Learn By Example: AWK](https://github.com/learnbyexample/Command-line-text-processing/blob/master/gnu_awk.md#dealing-with-duplicates) and the HN [discussion](https://news.ycombinator.com/item?id=20037366) which refers to it
1. Deduplicate your PATH
    ```
    PATH=$(printf %s $PATH | awk -v RS=: -v ORS=: '!a[$0]++')
    ```
1. Use here-documents to work with `sqlite` in your CLI [link](https://lobste.rs/s/c1omhw/there_s_relational_database_your_unix_cli#c_u5ukrj)


<a name="Vim"></a>
# Vim

1. [Advanced Vim macros](https://sanctum.geek.nz/arabesque/advanced-vim-macros/)
1. [Advanced Vim registers](https://sanctum.geek.nz/arabesque/advanced-vim-registers/) _e.g._ `"Ayy` append line to contents of register `a`.
1. Tabular [docs](https://raw.githubusercontent.com/godlygeek/tabular/master/doc/Tabular.txt)
1. Set the `wrap` function to operate at linebreaks (from [SO](https://stackoverflow.com/a/19624717)):
    ```
    set nolist wrap linebreak breakat&vim
    ```


<a name="LinuxProgramming"></a>
# Linux Programming

1. [LD_PRELOAD: the hero we need and deserve](https://blog.jessfraz.com/post/ld_preload/) ([HN Thread](https://news.ycombinator.com/item?id=19187417))
1. [Mesh: compacting memory management for C programs](https://arxiv.org/abs/1902.04738) ([HN Thread](https://news.ycombinator.com/item?id=19182779))
1. [Wipe Linux while running & reinstall](http://unix.stackexchange.com/a/227318/189858) ([HN Thread](https://news.ycombinator.com/item?id=13622301))


<a name="Networking"></a>
# Networking

1. [TCP Puzzlers](https://www.joyent.com/blog/tcp-puzzlers) with joyent.com submissions on [HN](https://news.ycombinator.com/from?site=joyent.com)
1. When TCP sockets [refuse to die](https://idea.popcount.org/2019-09-20-when-tcp-sockets-refuse-to-die/) (from [HN](https://news.ycombinator.com/item?id=21044529))


<a name="CProgramming"></a>
# C Programming

1. Peter's blog [strchr.com](https://www.strchr.com/)
1. Common Weakness Enumerations: [Weakness in software](http://cwe.mitre.org/data/definitions/658.html) and [SEI Cert coding standards](http://cwe.mitre.org/data/definitions/1154.html) for software written in C.
1. Generic selections in C11 ([Rob's programming blog](http://www.robertgamble.net/2012/01/c11-generic-selections.html))


<a name="DistributedSystems"></a>
# Distributed Systems

1. Distributed Consensus Revised talk by Heidi Howard [YouTube](https://www.youtube.com/watch?v=Pqc6X3sj6q8&list=PLGRqfvsPiRSgAKk3H9uc5AEH6RaWnY9At&autoplay=0&auto_play=false)


<a name="RegexStateMachines"></a>
# Regex, State Machines

1. Ragel ([homepage](http://www.colm.net/files/ragel/))
    1. SO answer on how to [balance parenthesis](https://stackoverflow.com/a/12835891)

<a name="TmuxCheatSheet"></a>
# `tmux` Cheat Sheet

1. Layouts
   * `select-layout even-horizontal`: yields panes laid-out next to each other
   * `select-layout even-vertical`: yields panes stacked one on top of the other
   * `<cmd>+space`: cycle through the five preset layouts
1. Keystrokes
   * `setw synchronize-panes on`: sends commands to all panes

<a name="OpenGL"></a>
# OpenGL

1. Anton's OpenGL4 Tutorials [eBook](https://capnramses.itch.io/antons-opengl-4-tutorials)
1. [Learn OpenGL](https://learnopengl.com/)
1. Learn OpenGL YouTube [playlist](https://youtu.be/W3gAzLwfIP0)

<a name="Vulkan"></a>

<a name="WebAssemblyWebGL"></a>
