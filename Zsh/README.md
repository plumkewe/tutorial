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

This also works for most text input fields system wide.  Netbeans being one exception

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>A</kbd></td></tr></tbody></table>

#### Go to the end of the line you are currently typing on.

This also works for most text input fields system wide.  Netbeans being one exception

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>E</kbd></td></tr></tbody></table>

#### Clears the Screen

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>L</kbd></td></tr></tbody></table>

#### Clears the Screen

<table><tbody><tr><td><kbd>⌘</kbd> + <kbd>K</kbd></td></tr></tbody></table>

#### Cut everything backwards to beginning of line

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>U</kbd></td></tr></tbody></table>

#### Cut everything forward to end of line

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>K</kbd></td></tr></tbody></table>

#### Cut one word backwards using white space as delimiter

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>W</kbd></td></tr></tbody></table>

#### Paste whatever was cut by the last cut command

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>Y</kbd></td></tr></tbody></table>

#### Same as backspace

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>H</kbd></td></tr></tbody></table>

#### Kill whatever you are running.  Also clears everything on current line

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>C</kbd></td></tr></tbody></table>

#### Exit the current shell when no process is running, or send EOF to a the running process

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>D</kbd></td></tr></tbody></table>

#### Puts whatever you are running into a suspended background process. fg restores it

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>Z</kbd></td></tr></tbody></table>

#### Undo the last command.

(Underscore.  So it's actually Ctrl + Shift + minus)

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>_</kbd></td></tr></tbody></table>

#### Swap the last two characters before the cursor

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>T</kbd></td></tr></tbody></table>

#### Move cursor one character forward

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>F</kbd></td></tr></tbody></table>

#### Move cursor one character backward

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>B</kbd></td></tr></tbody></table>

#### Move cursor one word forward

<table><tbody><tr><td><kbd>⌥</kbd> + <kbd>→</kbd></td></tr></tbody></table>

#### Move cursor one word backward

<table><tbody><tr><td><kbd>⌥</kbd> + <kbd>←</kbd></td></tr></tbody></table>

#### Swap the last two words before the cursor

<table><tbody><tr><td><kbd>⎋</kbd> + <kbd>T</kbd></td></tr></tbody></table>

#### Cut one word backwards using none alphabetic characters as delimiters

<table><tbody><tr><td><kbd>⎋</kbd> + <kbd>⌫</kbd></td></tr></tbody></table>

#### Auto-complete files and folder names

<table><tbody><tr><td><kbd>⇥</kbd></td></tr></tbody></table>

<br>

### Core commands

<p align="right">(<a href="#indice">indice</a>)</p>


#### Change directory e.g. `cd Documents`

<table><tbody><tr><td><code>cd [folder]</code></td><td>change directory</td></tr></tbody></table>

#### Home directory

<table><tbody><tr><td><code>cd</code></td><td>change directory</td></tr></tbody></table>

#### Home directory

<table><tbody><tr><td><code>cd ~</code></td><td>change directory</td></tr></tbody></table>

#### Root of drive

<table><tbody><tr><td><code>cd /</code></td><td>change directory</td></tr></tbody></table>

#### Previous directory

<table><tbody><tr><td><code>cd -</code></td><td>change directory</td></tr></tbody></table>

#### Short listing

<table><tbody><tr><td><code>ls</code></td><td>list</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ ls
GitHub				Scripts
Other
School
Screenshots
</pre></td></tr></tbody></table>

#### Long listing

<table><tbody><tr><td><code>ls -l</code></td><td>list</td><td>list</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ ls -l
total 0
drwxr-xr-x@  33 Plumkewe  staff  1056 Aug 22 01:59 GitHub
drwxr-xr-x  199 Plumkewe  staff  6368 Aug 22 00:23 Other
drwxr-xr-x   10 Plumkewe  staff   320 Jul 30 00:12 School
drwxr-xr-x@  86 Plumkewe  staff  2752 Aug 19 13:37 Screenshots
drwxr-xr-x    8 Plumkewe  staff   256 Aug 22 02:40 Scripts
</pre></td></tr></tbody></table>

#### Listing incl. hidden files

<table><tbody><tr><td><code>ls -a</code></td><td>list</td><td>list</td><td>list</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ ls -a
.		.DS_Store	.localized	Other		Screenshots
..		.idea		GitHub		School		Scripts
</pre></td></tr></tbody></table>

#### Long listing with Human readable file sizes

<table><tbody><tr><td><code>ls -lh</code></td><td>list</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ ls -lh
total 0
drwxr-xr-x@  33 Plumkewe  staff   1.0K Aug 22 01:59 GitHub
drwxr-xr-x  199 Plumkewe  staff   6.2K Aug 22 00:23 Other
drwxr-xr-x   10 Plumkewe  staff   320B Jul 30 00:12 School
drwxr-xr-x@  86 Plumkewe  staff   2.7K Aug 19 13:37 Screenshots
drwxr-xr-x    8 Plumkewe  staff   256B Aug 22 02:40 Scripts
</pre></td></tr></tbody></table>

#### Entire content of folder recursively

<table><tbody><tr><td><code>ls -R</code></td><td>list</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ ls -R
GitHub		Other		School		Screenshots	    Scripts

./GitHub:
Kitsune-Translations
...

./GitHub/Kitsune-Translations:
Localizations	README.md
...
</pre></td></tr></tbody></table>

#### Run command with the security privileges of the superuser (Super User DO)

<table><tbody><tr><td><code>sudo [command]</code></td><td>super user do</td></tr></tbody></table>

#### Opens a file ( as if you double clicked it )

<table><tbody><tr><td><code>open [file]</code></td><td>open</td></tr></tbody></table>

#### Displays active processes. Press q to quit

<table><tbody><tr><td><code>top</code></td><td>table of processes</td><td><pre style="font-family: monospace;">
Processes: 384 total, 2 running, 382 sleeping, 1423 threads            02:52:38
Load Avg: 1.79, 1.65, 1.69  CPU usage: 0.94% user, 1.53% sys, 97.51% idle
SharedLibs: 224M resident, 45M data, 60M linkedit.
MemRegions: 126075 total, 2045M resident, 76M private, 741M shared.
PhysMem: 8162M used (2925M wired), 28M unused.
VM: 6183G vsize, 2317M framework vsize, 53980655(0) swapins, 56295739(0) swapout
Networks: packets: 12928380/15G in, 13852515/6460M out.
Disks: 16802996/431G read, 35391275/428G written.

PID    COMMAND      %CPU TIME     #TH   #WQ  #PORT MEM    PURG   CMPRS  PGRP
64950  top          1.9  00:01.42 1/1   0    26    4504K  0B     0B     64950
</pre></td></tr></tbody></table>

#### Opens the file using the nano editor

<table><tbody><tr><td><code>nano [file]</code></td><td>Nano's ANOther editor</td></tr></tbody></table>

#### Opens the file using the vim editor

<table><tbody><tr><td><code>vim [file]</code></td><td>Vi IMproved</td></tr></tbody></table>

#### Clears the screen

<table><tbody><tr><td><code>clear</code></td><td>clear</td></tr></tbody></table>

#### Resets the terminal display

<table><tbody><tr><td><code>reset</code></td><td>reset</td></tr></tbody></table>

<br>

### Chaining commands

<p align="right">(<a href="#indice">indice</a>)</p>


#### Run command A and then B, regardless of success of A

<table><tbody><tr><td><code>[command-a]; [command-b]</code></td></tr></tbody></table>

#### Run command B if A succeeded

<table><tbody><tr><td><code>[command-a] && [command-b]</code></td></tr></tbody></table>

#### \ | [command-b] | Run command B if A failed

<table><tbody><tr><td><code>[command-a] || [command-b]</code></td></tr></tbody></table>

#### Run command A in background

<table><tbody><tr><td><code>[command-a] &</code></td></tr></tbody></table>

<br>

### Piping commands

<p align="right">(<a href="#indice">indice</a>)</p>


#### [command-b] | Run command A and then pass the result to command B e.g ps auxwww \ | grep google

<table><tbody><tr><td><code>[command-a] | [command-b]</code></td></tr></tbody></table>

<br>

### Command history

<p align="right">(<a href="#indice">indice</a>)</p>


#### Shows the stuff typed – add a number to limit the last n items

<table><tbody><tr><td><code>history n</code></td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ history 4
519  ls -R
520  top
521  nano readme.md
522  history 4
</pre></td></tr></tbody></table>

#### Interactively search through previously typed commands

<table><tbody><tr><td><kbd>⌃</kbd> + <kbd>r</kbd></td></tr></tbody></table>

#### Execute the last command typed that starts with ‘value’

<table><tbody><tr><td><code>![value]</code></td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ !to
touch readme.md
</pre></td></tr></tbody></table>

#### Print to the console the last command typed that starts with ‘value’

<table><tbody><tr><td><code>![value]:p</code></td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ !t:p
touch readme.md	
</pre></td></tr></tbody></table>

#### Execute the last command typed

<table><tbody><tr><td><code>!!</code></td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ !!
touch readme.md	
</pre></td></tr></tbody></table>

#### Print to the console the last command typed

<table><tbody><tr><td><code>!!:p</code></td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ !!
touch readme.md	
</pre></td></tr></tbody></table>

<br>

### File management

<p align="right">(<a href="#indice">indice</a>)</p>


#### Create a new file

<table><tbody><tr><td><code>touch [file]</code></td></tr></tbody></table>

#### Full path to working directory

<table><tbody><tr><td><code>pwd</code></td><td>print working directory</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ pwd
/Users/Plumkewe/desktop
</pre></td></tr></tbody></table>

#### Current folder, e.g. `ls .`

<table><tbody><tr><td><code>.</code></td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ ls .
GitHub		School		Scripts
Other		Screenshots	readme.md
</pre></td></tr></tbody></table>

#### Parent/enclosing directory, e.g. `ls ..`

<table><tbody><tr><td><code>..</code></td></tr></tbody></table>

#### Long listing of parent directory

<table><tbody><tr><td><code>ls -l ..</code></td><td>list</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ ls ..
Applications					Public
Bootstrap Studio Backups		README.md
CLionProjects					WebstormProjects
</pre></td></tr></tbody></table>

#### Move 2 levels up

<table><tbody><tr><td><code>cd ../../</code></td><td>change directory</td></tr></tbody></table>

#### Concatenate to screen

<table><tbody><tr><td><code>cat</code></td><td>concatenate</td></tr></tbody></table>

#### Remove a file, e.g. `rm data.tmp`

<table><tbody><tr><td><code>rm [file]</code></td><td>remove</td></tr></tbody></table>

#### Remove with confirmation

<table><tbody><tr><td><code>rm -i [file]</code></td><td>remove</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ rm -i readme.md
remove readme.md? n/y
</pre></td></tr></tbody></table>

#### Remove a directory and contents

<table><tbody><tr><td><code>rm -r [dir]</code></td><td>remove</td></tr></tbody></table>

#### Force removal without confirmation

<table><tbody><tr><td><code>rm -f [file]</code></td><td>remove</td></tr></tbody></table>

#### Copy file to file

<table><tbody><tr><td><code>cp [file] [newfile]</code></td><td>copy</td></tr></tbody></table>

#### Copy file to directory

<table><tbody><tr><td><code>cp [file] [dir]</code></td><td>copy</td></tr></tbody></table>

#### Move/Rename, e.g. `mv file1.ad /tmp`

<table><tbody><tr><td><code>mv [file] [new filename]</code></td><td>move</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ mv CIA.txt novabb.txt
</pre></td></tr></tbody></table>

#### Copies file contents to clipboard

<table><tbody><tr><td><code>pbcopy < [file]</code></td><td>pasteboard copy</td></tr></tbody></table>

#### Paste clipboard contents

<table><tbody><tr><td><code>pbpaste</code></td><td>pasteboard paste</td></tr></tbody></table>

#### Paste clipboard contents into file, `pbpaste > paste-test.txt`

<table><tbody><tr><td><code>pbpaste > [file]</code></td><td>pasteboard paste</td></tr></tbody></table>

<br>

### Directory management

<p align="right">(<a href="#indice">indice</a>)</p>


#### Create new directory

<table><tbody><tr><td><code>mkdir [dir]</code></td><td>make directory</td></tr></tbody></table>

#### Create nested directories

<table><tbody><tr><td><code>mkdir -p [dir]/[dir]</code></td><td>make directory</td></tr></tbody></table>

#### Remove directory ( only operates on empty directories )

<table><tbody><tr><td><code>rmdir [dir]</code></td><td>remove directory</td></tr></tbody></table>

#### Remove directory and contents

<table><tbody><tr><td><code>rm -R [dir]</code></td><td>remove</td></tr></tbody></table>

#### Output file content delivered in screensize chunks

<table><tbody><tr><td><code>less [file]</code></td></tr></tbody></table>

#### Push output to file, keep in mind it will get overwritten

<table><tbody><tr><td><code>[command] > [file]</code></td></tr></tbody></table>

#### Append output to existing file

<table><tbody><tr><td><code>[command] >> [file]</code></td></tr></tbody></table>

#### Tell command to read content from a file

<table><tbody><tr><td><code>[command] < [file]</code></td></tr></tbody></table>

<br>

### Search

<p align="right">(<a href="#indice">indice</a>)</p>


#### Search for files, e.g. `find /Users -name "file.txt"`

<table><tbody><tr><td><code>find [dir] -name [search_pattern]</code></td><td>find</td></tr></tbody></table>

#### Search for all lines that contain the pattern, e.g. `grep "Tom" file.txt`

<table><tbody><tr><td><code>grep [search_pattern] [file]</code></td><td>globally search a regular expression and print</td></tr></tbody></table>

#### Recursively search in all files in specified directory for all lines that contain the pattern

<table><tbody><tr><td><code>grep -r [search_pattern] [dir]</code></td><td>globally search a regular expression and print</td></tr></tbody></table>

#### Search for all lines that do NOT contain the pattern

<table><tbody><tr><td><code>grep -v [search_pattern] [file]</code></td><td>globally search a regular expression and print</td></tr></tbody></table>

#### Search for all lines that contain the case-insensitive pattern

<table><tbody><tr><td><code>grep -i [search_pattern] [file]</code></td><td>globally search a regular expression and print</td></tr></tbody></table>

#### Spotlight search for files (names, content, other metadata), e.g. `mdfind skateboard`

<table><tbody><tr><td><code>mdfind [search_pattern]</code></td><td>metadata find</td></tr></tbody></table>

#### Spotlight search for files named like pattern in the given directory

<table><tbody><tr><td><code>mdfind -onlyin [dir] -name [pattern]</code></td><td>metadata find</td></tr></tbody></table>

<br>

### Help

<p align="right">(<a href="#indice">indice</a>)</p>


#### Offers help

<table><tbody><tr><td><code>[command] -h</code></td><td>help</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ cd --help
-bash: cd: --: invalid option
cd: usage: cd [-L|-P] [dir]
</pre></td></tr></tbody></table>

#### Offers help

<table><tbody><tr><td><code>[command] --help</code></td><td>help</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ cd --help
-bash: cd: --: invalid option
cd: usage: cd [-L|-P] [dir]
</pre></td></tr></tbody></table>

#### Offers help

<table><tbody><tr><td><code>info [command]</code></td><td>information</td></tr></tbody></table>

#### Show the help manual for [command]

<table><tbody><tr><td><code>man [command]</code></td><td>manual</td></tr></tbody></table>

#### Gives a one-line description of [command]

<table><tbody><tr><td><code>whatis [command]</code></td><td>what is</td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ whatis grep
grep(1), egrep(1), fgrep(1), zgrep(1), zegrep(1), zfgrep(1) - file pattern searcher
grep(1), egrep(1), fgrep(1), rgrep(1), bzgrep(1), bzegrep(1), bzfgrep(1), zgrep(1), zegrep(1), zfgrep(1) - file pattern searcher
git-grep(1)              - Print lines matching a pattern
</pre></td></tr></tbody></table>

#### Searches for command with keywords in description

<table><tbody><tr><td><code>apropos [search-pattern]</code></td><td><pre style="font-family: monospace;">
[Plumkewe-MacBook:desktop Plumkewe$ apropos write
BIO_get_buffer_num_lines(3ssl), BIO_set_read_buffer_size(3ssl), BIO_set_write_buffer_size(3ssl), BIO_set_buffer_size(3ssl), ...
</pre></td></tr></tbody></table>