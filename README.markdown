# Outline #

“GoToFile” imitates TextMate’s “Go to File…” ⌘T functionality [see here](http://manual.macromates.com/en/working_with_multiple_files#moving_between_files_with_grace). In addition it is possible to narrow down the list of files by considering (parts of) the file path. 

Furthermore it is not only possible to open the selected file in TextMate but also to:

* open the selected file in the default application (by using “open”)
* activate QuickLook
* insert the relative path from the current file to the selected one
* insert the absolute path.

The list of found files is sorted by the score which is calculated inside of Jamis Buck's “Fuzzy File Finder” routine. The maximum number of outputted files is set to 100 (can be changed in “FileFinder.rb” line 4).

To ignore certain files add a TM variable called "TM_FUZZYFINDER_IGNORE", in it put the file regexp separated by commas. For example: '\*.pyc,\*.zip,\*.gz,\*.bz,\*.tar,\*.jpg,\*.png,\*.gif,\*.avi,\*.wmv,\*.ogg,\*.mp3,\*.mov'.

“GoToFile” makes usage of Jamis Buck's [“Fuzzy File Finder”](http://github.com/jamis/fuzzy_file_finder) and was inspired by Amiel Martin's [“FuzzyFileFinder”](http://github.com/amiel/gotofile.tmbundle/tree/amiels_original) bundle which a few code fragments are taken from.

# Official Git Repos #

can be found here: http://github.com/amiel/gotofile.tmbundle


# Usage #

<button>⇧⌘K</button> invokes “GoToFile”. The root directory will be taken from `$TM_PROJECT_DIRECTORY` || `$TM_DIRECTORY` || current directory. “GoToFile” won't work on unsaved documents. There is a mouse-over event to display the entire file path.


## Input Field ##

Type characters in order to narrow down the list of files. The dialogue will be updated while typing. To search only in certain folders type for instance: `s/rb` or `s/li/mm` etc.

Normally spaces are ignored. If one wants to look for a space one has to escape the space: `\␣`

## Shortcuts ##

* <button>CLICK</button> or <button>&#x21A9;</button>opens the file in TextMate
* <button>⌥ CLICK</button> or <button>⌥&#x21A9;</button>opens the file with the default application
* <button>⇧ CLICK</button> or <button>⇧&#x21A9;</button>inserts the relative file path
* <button>⇧⌥ CLICK</button> or <button>⇧⌥&#x21A9;</button>inserts the absolute file path
* <button>SPACE</button> opens the selected file (via ⇥ or ⇧⇥) in QuickLook (Leopard only)
* <button>⇥</button> sets the focus to next element
* <button>⇧⇥</button> sets the focus to previous element
* <button>^F</button> sets the focus to the input field
* <button>⎋</button> or <button>⌘W</button> closes the “GoToFile” window

# ToDo #

* up to now it's only possible to close the QuickLook window via mouse
* improve UI

# Contributions #

***Date: Feb 23 2009***

<pre>
-  Amiel Martin&nbsp;&nbsp;<a href="mailto:amiel.martin@gmail.com">amiel.martin@gmail.com</a>
-  Hans-Jörg Bibiko&nbsp;&nbsp;<a href="mailto:bibiko@eva.mpg.de">bibiko@eva.mpg.de</a>
-  Eric Doughty-Papassideris&nbsp;&nbsp;github:ddlsmurf
-  Travis Jeffery&nbsp;&nbsp;<a href="mailto:t.jeffery@utoronto.ca">t.jeffery@utoronto.ca</a>
-  Eric O'Connell &nbsp;&nbsp;github:drd
-  Nathan Carnes&nbsp;&nbsp;github:nathancarnes
</pre>