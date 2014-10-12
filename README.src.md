[:var_set('', """
#/ Compile command
aoikdyndocdsl -s README.src.md -n aoikdyndocdsl.ext.all::nto -g README.md
""")]\
[:HDLR('heading', 'heading')]\
# AoikWinWhich
Windows version of Linux's **which** program, written in a variety of languages:
- [AoikWinWhich-Bash](https://github.com/AoiKuiyuyou/AoikWinWhich-Bash)
- [AoikWinWhich-Batch](https://github.com/AoiKuiyuyou/AoikWinWhich-Batch)
- [AoikWinWhich-Ceylon](https://github.com/AoiKuiyuyou/AoikWinWhich-Ceylon)
- [AoikWinWhich-Clojure](https://github.com/AoiKuiyuyou/AoikWinWhich-Clojure)
- [AoikWinWhich-CoffeeScript](https://github.com/AoiKuiyuyou/AoikWinWhich-CoffeeScript)
- [AoikWinWhich-C](https://github.com/AoiKuiyuyou/AoikWinWhich-C)
- [AoikWinWhich-Cpp](https://github.com/AoiKuiyuyou/AoikWinWhich-Cpp)
- [AoikWinWhich-Cpp-CLI](https://github.com/AoiKuiyuyou/AoikWinWhich-Cpp-CLI)
- [AoikWinWhich-CSharp](https://github.com/AoiKuiyuyou/AoikWinWhich-CSharp)
- [AoikWinWhich-D](https://github.com/AoiKuiyuyou/AoikWinWhich-D)
- [AoikWinWhich-Dart](https://github.com/AoiKuiyuyou/AoikWinWhich-Dart)
- [AoikWinWhich-Eiffel](https://github.com/AoiKuiyuyou/AoikWinWhich-Eiffel)
- [AoikWinWhich-Erlang](https://github.com/AoiKuiyuyou/AoikWinWhich-Erlang)
- [AoikWinWhich-FSharp](https://github.com/AoiKuiyuyou/AoikWinWhich-FSharp)
- [AoikWinWhich-Go](https://github.com/AoiKuiyuyou/AoikWinWhich-Go)
- [AoikWinWhich-Groovy](https://github.com/AoiKuiyuyou/AoikWinWhich-Groovy)
- [AoikWinWhich-Haskell](https://github.com/AoiKuiyuyou/AoikWinWhich-Haskell)
- [AoikWinWhich-Hy](https://github.com/AoiKuiyuyou/AoikWinWhich-Hy)
- [AoikWinWhich-Java](https://github.com/AoiKuiyuyou/AoikWinWhich-Java)
- [AoikWinWhich-JavaScript](https://github.com/AoiKuiyuyou/AoikWinWhich-JavaScript)
- [AoikWinWhich-Julia](https://github.com/AoiKuiyuyou/AoikWinWhich-Julia)
- [AoikWinWhich-Kotlin](https://github.com/AoiKuiyuyou/AoikWinWhich-Kotlin)
- [AoikWinWhich-Lua](https://github.com/AoiKuiyuyou/AoikWinWhich-Lua)
- [AoikWinWhich-OCaml](https://github.com/AoiKuiyuyou/AoikWinWhich-OCaml)
- [AoikWinWhich-Pascal](https://github.com/AoiKuiyuyou/AoikWinWhich-Pascal)
- [AoikWinWhich-Perl](https://github.com/AoiKuiyuyou/AoikWinWhich-Perl)
- [AoikWinWhich-PHP](https://github.com/AoiKuiyuyou/AoikWinWhich-PHP)
- [AoikWinWhich-Python](https://github.com/AoiKuiyuyou/AoikWinWhich-Python)
- [AoikWinWhich-Ruby](https://github.com/AoiKuiyuyou/AoikWinWhich-Ruby)
- [AoikWinWhich-Rust](https://github.com/AoiKuiyuyou/AoikWinWhich-Rust)
- [AoikWinWhich-Scala](https://github.com/AoiKuiyuyou/AoikWinWhich-Scala)
- [AoikWinWhich-Scheme](https://github.com/AoiKuiyuyou/AoikWinWhich-Scheme)
- [AoikWinWhich-Tcl](https://github.com/AoiKuiyuyou/AoikWinWhich-Tcl)
- [AoikWinWhich-VB.NET](https://github.com/AoiKuiyuyou/AoikWinWhich-VB.NET)
- [AoikWinWhich-Xtend](https://github.com/AoiKuiyuyou/AoikWinWhich-Xtend)

## Table of Contents
[:toc(beg='next', indent=-1)]

## How to use
Assume the program is accessible in your command console via short name
**aoikwinwhich**.

To get you started, find where **aoikwinwhich** itself is located:
```
aoikwinwhich aoikwinwhich
```

Run without argument to show usage:
```
aoikwinwhich
```
```
Usage: aoikwinwhich PROG

#/ PROG can be either name or path
aoikwinwhich notepad.exe
aoikwinwhich C:\Windows\notepad.exe

#/ PROG can be either absolute or relative
aoikwinwhich C:\Windows\notepad.exe
aoikwinwhich Windows\notepad.exe

#/ PROG can be either with or without extension
aoikwinwhich notepad.exe
aoikwinwhich notepad
aoikwinwhich C:\Windows\notepad.exe
aoikwinwhich C:\Windows\notepad
```

## What are executable on Windows console
Unlike on Linux console where executable bit determines whether a file is
executable, on Windows console a file is executable if only its file extension
(e.g. *.exe*) is listed in Windows environment variable **PATHEXT**.

### Save your typing
When run an executable on Windows console, one does not have to always type its
full path. Several parts in the path can be omitted:

- Dir path can be omitted, e.g.:
  ```
notepad.exe
  ```
  can be resolved to
  ```
C:\Windows\notepad.exe
  ```
  This is because dir paths listed in environment variable **PATH** are implied.

- File extension can be omitted, e.g.:
  ```
notepad
  ```
  can be resolved to
  ```
notepad.exe
  ```
  This is because extensions listed in environment variable **PATHEXT** are
  implied.

## How to read the funny source code
For developers interested in reading the source code,
Here is a flowchart ([.png](/doc/dev/main.png?raw=true),
[.svg](/doc/dev/main.svg?raw=true), or
[.graphml](/doc/dev/main.graphml?raw=true)) that has shown key steps of the
program.
![Image](/doc/dev/main.png?raw=true)

The flowchart is produced using free graph editor
[yEd](http://www.yworks.com/en/products_yed_download.html).

If you want to copy the text in the graph, it's recommended to download the
[.svg](/doc/dev/main.svg?raw=true) file and open it locally in your browser.
(For security reason, Github has disabled rendering of SVG images on the page.)

The meaning of the shapes in the flowchart should be straightforward. One thing
worth mentioning is a filled arrow means next step whereas an unfilled arrow
means sub-step.

The most useful feature of the flowchart is, for each step in it, there is a
7-character ID. This ID can be used to locate (by text searching) the code that
implements a step. This mechanism has two merits:

1. It has provided **precise** (locating precision is line-level)
  and **fast** (text searching is fast) mapping from doc to code, which is
  very handy for non-trivial project.

  Without it you have to rely on developers' memory to recall the code
  locations (*Will you recall them after several months, precise and fast?*).

2. It has provided **precise** (unique ID) and **concise** (7-character long)
  names for each steps of a program, which is very handy for communicating
  between members of a development team.

  Without it describing some steps of a program between team members tends to be
  unclear.
