# Terminal

Avevo deciso di imparare qualche comando per il terminale, data la frustrazione continua di dover fare click infiniti per eseguire azioni basilari, come creare un file .txt tramite la GUI.
Per la base ho scelto di utilizzare una delle tante [cheat sheet](https://github.com/0nn0/terminal-mac-cheatsheet) disponibili sul web, ma l'ho modificata un po' per soddisfare le mie esigenze.


## Indice

* [Shortcuts](#shortcuts)
* [Core commands](#core-commands)
* [Chaining commands](#chaining-commands)
* [Piping commands](#piping-commands)
* [Command history](#command-history)
* [File management](#file-management)
* [Directory management](#directory-management)
* [Search](#search)
* [Help](#help)

<br>

### Shortcuts

<p align="right">(<a href="#indice">indice</a>)</p>


#### Go to the beginning of the line you are currently typing on.  

This also works for most text input fields system wide.  Netbeans being one exception

<table><tbody><tr><td><kbd>⌃ + A</kbd></td></tr></tbody></table>

#### Go to the end of the line you are currently typing on.

This also works for most text input fields system wide.  Netbeans being one exception

<table><tbody><tr><td><kbd>⌃ + E</kbd></td></tr></tbody></table>

#### Clears the Screen

<table><tbody><tr><td><kbd>⌃ + L</kbd></td></tr></tbody></table>

#### Clears the Screen

<table><tbody><tr><td><kbd>⌘ + K</kbd></td></tr></tbody></table>

#### Cut everything backwards to beginning of line

<table><tbody><tr><td><kbd>⌃ + U</kbd></td></tr></tbody></table>

#### Cut everything forward to end of line

<table><tbody><tr><td><kbd>⌃ + K</kbd></td></tr></tbody></table>

#### Cut one word backwards using white space as delimiter

<table><tbody><tr><td><kbd>⌃ + W</kbd></td></tr></tbody></table>

#### Paste whatever was cut by the last cut command

<table><tbody><tr><td><kbd>⌃ + Y</kbd></td></tr></tbody></table>

#### Same as backspace

<table><tbody><tr><td><kbd>⌃ + H</kbd></td></tr></tbody></table>

#### Kill whatever you are running.  Also clears everything on current line

<table><tbody><tr><td><kbd>⌃ + C</kbd></td></tr></tbody></table>

#### Exit the current shell when no process is running, or send EOF to a the running process

<table><tbody><tr><td><kbd>⌃ + D</kbd></td></tr></tbody></table>

#### Puts whatever you are running into a suspended background process. fg restores it

<table><tbody><tr><td><kbd>⌃ + Z</kbd></td></tr></tbody></table>

#### Undo the last command.

(Underscore.  So it's actually Ctrl + Shift + minus)

<table><tbody><tr><td><kbd>⌃ + _</kbd></td></tr></tbody></table>

#### Swap the last two characters before the cursor

<table><tbody><tr><td><kbd>⌃ + T</kbd></td></tr></tbody></table>

#### Move cursor one character forward

<table><tbody><tr><td><kbd>⌃ + F</kbd></td></tr></tbody></table>

#### Move cursor one character backward

<table><tbody><tr><td><kbd>⌃ + B</kbd></td></tr></tbody></table>

#### Move cursor one word forward

<table><tbody><tr><td><kbd>⌥ + →</kbd></td></tr></tbody></table>

#### Move cursor one word backward

<table><tbody><tr><td><kbd>⌥ + ←</kbd></td></tr></tbody></table>

#### Swap the last two words before the cursor

<table><tbody><tr><td><kbd>⎋ + T</kbd></td></tr></tbody></table>

#### Cut one word backwards using none alphabetic characters as delimiters

<table><tbody><tr><td><kbd>⎋ + ⌫</kbd></td></tr></tbody></table>

#### Auto-complete files and folder names

<table><tbody><tr><td><kbd>⇥</kbd></td></tr></tbody></table>

<br>

### Core commands

<p align="right">(<a href="#indice">indice</a>)</p>


#### Change directory e.g. `cd Documents`

<table><tbody><tr><td><kbd>cd [folder]</kbd></td></tr></tbody></table>

#### Home directory

<table><tbody><tr><td><kbd>cd</kbd></td></tr></tbody></table>

#### Home directory

<table><tbody><tr><td><kbd>cd ~</kbd></td></tr></tbody></table>

#### Root of drive

<table><tbody><tr><td><kbd>cd /</kbd></td></tr></tbody></table>

#### Previous directory

<table><tbody><tr><td><kbd>cd -</kbd></td></tr></tbody></table>

#### Short listing

<table><tbody><tr><td><kbd>ls</kbd></td></tr></tbody></table>

#### Long listing

<table><tbody><tr><td><kbd>ls -l</kbd></td></tr></tbody></table>

#### Listing incl. hidden files

<table><tbody><tr><td><kbd>ls -a</kbd></td></tr></tbody></table>

#### Long listing with Human readable file sizes

<table><tbody><tr><td><kbd>ls -lh</kbd></td></tr></tbody></table>

#### Entire content of folder recursively

<table><tbody><tr><td><kbd>ls -R</kbd></td></tr></tbody></table>

#### Run command with the security privileges of the superuser (Super User DO)

<table><tbody><tr><td><kbd>sudo [⌘]</kbd></td></tr></tbody></table>

#### Opens a file ( as if you double clicked it )

<table><tbody><tr><td><kbd>open [file]</kbd></td></tr></tbody></table>

#### Displays active processes. Press q to quit

<table><tbody><tr><td><kbd>top</kbd></td></tr></tbody></table>

#### Opens the file using the nano editor

<table><tbody><tr><td><kbd>nano [file]</kbd></td></tr></tbody></table>

#### Opens the file using the vim editor

<table><tbody><tr><td><kbd>vim [file]</kbd></td></tr></tbody></table>

#### Clears the screen

<table><tbody><tr><td><kbd>clear</kbd></td></tr></tbody></table>

#### Resets the terminal display

<table><tbody><tr><td><kbd>reset</kbd></td></tr></tbody></table>

<br>

### Chaining commands

<p align="right">(<a href="#indice">indice</a>)</p>


#### Run command A and then B, regardless of success of A

<table><tbody><tr><td><kbd>[⌘-a]; [⌘-b]</kbd></td></tr></tbody></table>

#### Run command B if A succeeded

<table><tbody><tr><td><kbd>[⌘-a] && [⌘-b]</kbd></td></tr></tbody></table>

#### \ | [command-b] | Run command B if A failed

<table><tbody><tr><td><kbd>[⌘-a] \</kbd></td></tr></tbody></table>

#### Run command A in background

<table><tbody><tr><td><kbd>[⌘-a] &</kbd></td></tr></tbody></table>

<br>

### Piping commands

<p align="right">(<a href="#indice">indice</a>)</p>


#### [command-b] | Run command A and then pass the result to command B e.g ps auxwww \ | grep google

<table><tbody><tr><td><kbd>[⌘-a] \</kbd></td></tr></tbody></table>

<br>

### Command history

<p align="right">(<a href="#indice">indice</a>)</p>


#### Shows the stuff typed – add a number to limit the last n items

<table><tbody><tr><td><kbd>history n</kbd></td></tr></tbody></table>

#### Interactively search through previously typed commands

<table><tbody><tr><td><kbd>⌃ + r</kbd></td></tr></tbody></table>

#### Execute the last command typed that starts with ‘value’

<table><tbody><tr><td><kbd>![value]</kbd></td></tr></tbody></table>

#### Print to the console the last command typed that starts with ‘value’

<table><tbody><tr><td><kbd>![value]:p</kbd></td></tr></tbody></table>

#### Execute the last command typed

<table><tbody><tr><td><kbd>!!</kbd></td></tr></tbody></table>

#### Print to the console the last command typed

<table><tbody><tr><td><kbd>!!:p</kbd></td></tr></tbody></table>

<br>

### File management

<p align="right">(<a href="#indice">indice</a>)</p>


#### Create a new file

<table><tbody><tr><td><kbd>touch [file]</kbd></td></tr></tbody></table>

#### Full path to working directory

<table><tbody><tr><td><kbd>pwd</kbd></td></tr></tbody></table>

#### Current folder, e.g. `ls .`

<table><tbody><tr><td><kbd>.</kbd></td></tr></tbody></table>

#### Parent/enclosing directory, e.g. `ls ..`

<table><tbody><tr><td><kbd>..</kbd></td></tr></tbody></table>

#### Long listing of parent directory

<table><tbody><tr><td><kbd>ls -l ..</kbd></td></tr></tbody></table>

#### Move 2 levels up

<table><tbody><tr><td><kbd>cd ../../</kbd></td></tr></tbody></table>

#### Concatenate to screen

<table><tbody><tr><td><kbd>cat</kbd></td></tr></tbody></table>

#### Remove a file, e.g. `rm data.tmp`

<table><tbody><tr><td><kbd>rm [file]</kbd></td></tr></tbody></table>

#### Remove with confirmation

<table><tbody><tr><td><kbd>rm -i [file]</kbd></td></tr></tbody></table>

#### Remove a directory and contents

<table><tbody><tr><td><kbd>rm -r [dir]</kbd></td></tr></tbody></table>

#### Force removal without confirmation

<table><tbody><tr><td><kbd>rm -f [file]</kbd></td></tr></tbody></table>

#### Copy file to file

<table><tbody><tr><td><kbd>cp [file] [newfile]</kbd></td></tr></tbody></table>

#### Copy file to directory

<table><tbody><tr><td><kbd>cp [file] [dir]</kbd></td></tr></tbody></table>

#### Move/Rename, e.g. `mv file1.ad /tmp`

<table><tbody><tr><td><kbd>mv [file] [new filename]</kbd></td></tr></tbody></table>

#### Copies file contents to clipboard

<table><tbody><tr><td><kbd>pbcopy < [file]</kbd></td></tr></tbody></table>

#### Paste clipboard contents

<table><tbody><tr><td><kbd>pbpaste</kbd></td></tr></tbody></table>

#### Paste clipboard contents into file, `pbpaste > paste-test.txt`

<table><tbody><tr><td><kbd>pbpaste > [file]</kbd></td></tr></tbody></table>

<br>

### Directory management

<p align="right">(<a href="#indice">indice</a>)</p>


#### Create new directory

<table><tbody><tr><td><kbd>mkdir [dir]</kbd></td></tr></tbody></table>

#### Create nested directories

<table><tbody><tr><td><kbd>mkdir -p [dir]/[dir]</kbd></td></tr></tbody></table>

#### Remove directory ( only operates on empty directories )

<table><tbody><tr><td><kbd>rmdir [dir]</kbd></td></tr></tbody></table>

#### Remove directory and contents

<table><tbody><tr><td><kbd>rm -R [dir]</kbd></td></tr></tbody></table>

#### Output file content delivered in screensize chunks

<table><tbody><tr><td><kbd>less [file]</kbd></td></tr></tbody></table>

#### Push output to file, keep in mind it will get overwritten

<table><tbody><tr><td><kbd>[⌘] > [file]</kbd></td></tr></tbody></table>

#### Append output to existing file

<table><tbody><tr><td><kbd>[⌘] >> [file]</kbd></td></tr></tbody></table>

#### Tell command to read content from a file

<table><tbody><tr><td><kbd>[⌘] < [file]</kbd></td></tr></tbody></table>

<br>

### Search

<p align="right">(<a href="#indice">indice</a>)</p>


#### Search for files, e.g. `find /Users -name "file.txt"`

<table><tbody><tr><td><kbd>find [dir] -name [search_pattern]</kbd></td></tr></tbody></table>

#### Search for all lines that contain the pattern, e.g. `grep "Tom" file.txt`

<table><tbody><tr><td><kbd>grep [search_pattern] [file]</kbd></td></tr></tbody></table>

#### Recursively search in all files in specified directory for all lines that contain the pattern

<table><tbody><tr><td><kbd>grep -r [search_pattern] [dir]</kbd></td></tr></tbody></table>

#### Search for all lines that do NOT contain the pattern

<table><tbody><tr><td><kbd>grep -v [search_pattern] [file]</kbd></td></tr></tbody></table>

#### Search for all lines that contain the case-insensitive pattern

<table><tbody><tr><td><kbd>grep -i [search_pattern] [file]</kbd></td></tr></tbody></table>

#### Spotlight search for files (names, content, other metadata), e.g. `mdfind skateboard`

<table><tbody><tr><td><kbd>mdfind [search_pattern]</kbd></td></tr></tbody></table>

#### Spotlight search for files named like pattern in the given directory

<table><tbody><tr><td><kbd>mdfind -onlyin [dir] -name [pattern]</kbd></td></tr></tbody></table>

<br>

### Help

<p align="right">(<a href="#indice">indice</a>)</p>


#### Offers help

<table><tbody><tr><td><kbd>[⌘] -h</kbd></td></tr></tbody></table>

#### Offers help

<table><tbody><tr><td><kbd>[⌘] --help</kbd></td></tr></tbody></table>

#### Offers help

<table><tbody><tr><td><kbd>info [⌘]</kbd></td></tr></tbody></table>

#### Show the help manual for [command]

<table><tbody><tr><td><kbd>man [⌘]</kbd></td></tr></tbody></table>

#### Gives a one-line description of [command]

<table><tbody><tr><td><kbd>whatis [⌘]</kbd></td></tr></tbody></table>

#### Searches for command with keywords in description

<table><tbody><tr><td><kbd>apropos [search-pattern]</kbd></td></tr></tbody></table>