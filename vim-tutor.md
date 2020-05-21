# VimTutor notes

### Chapter 6
### Chapter 1
* press i to get into Insert mode
* press I to get into Insert mode and place cursor in the front of the line
* a appends to current location, A appends to current line's order
* hjkl to move aswd
* Ctrl + `[` to enter command mode
* Save & Exit Vi with ZZ  
* :w to save
* x to delete current character
* dd to delete current line
* d#d where # is any number will delete that many lines from the current line. Eg: d4d deletes the current line and 3 other lines below it.
* Type 0 to reach the start of the line
* w to move forward , b to move backward one work with punctuations,
* W and B without punct.
* Recommended way of saving by normal inefficient people is :wq

## Always remember to enter command mode by pressing ^+`[`!


### Be careful with small or caps of a character which may result in different behaviour.


#### Fact:


> You start recording by q<letter> and you can end it by typing q again.

>Recording is a really useful feature of Vim.

>It records everything you type. You can then replay it simply by typing @<letter>. Record search, movement, replacement...

* u does undo
* Capital A to Append to a line.
* gg to reach the top of a file
* G to reach END OF FILE.


### Chapter 2
** ALL d commands acts a delete/ cut.**
* dw to delete word / Also cut into your buffer!
* p to paste them
* d$ or D deletes from current cursor to end of line. also cuts.


>
    d      - is the delete operator.
    motion - is what the operator will operate on (listed below).
    A short list of motions:
    w - until the start of the next word, EXCLUDING its first character.
    e - to the end of the current word, INCLUDING the last character.
    $ - to the end of the line, INCLUDING the last character.
 

#### Fact: 
> Visual Mode is available with V command for easier selection to copy a group of lines

* we learn w to move forward a word... 2w makes us move 2 letters forward
* e to move a word forward but cursor lies before the last letter.
* d#w same as d#d where d is # number here it cuts # number of words.
* d#d and #dd works as same as intended. [Refer](https://stackoverflow.com/questions/32010466/what-is-the-difference-between-number-command-motion-and-command-number-motion)
* u to undo, U to fix a WHOLE line
* x to delete an unwanted character
* ^R Redo , ^ stands for Ctrl fyi.

### Chapter 3

* p stands for put and behaves as paster command as we know
* use dd to cut a line 
* use yy to copy a line then paste! with p
* r' ' where any single character typed will be replaced on the editor
* c is change command
* ce changes from current cursor to end of word.
* ce cuts your word into the buffer but! it actually puts u in insert mode after using ce command!
* c is used with same motions *the commands that follow * as delete
* cw, c$ also puts you in insert mode after changing. *thats something to remember*

### Chapter 4

* CtrlG to show file status if its saved or modified/ expanded line/character location of the file *If u see [Modified] it is recommended to save the file with :w and means it is not saved*
* G to reach EOF
* gg to reach file start
* #gg takes you to #th number line where # is a line.
* use / and followed by text to start searching a file.
* type n to go to next searched word, N to go search upwards

* I recommend sticking to either / or ? . Preferably /
* Percentage Sign or the modulo or % can be used to Match Brackets.
* Place Cursor and % to find matching paran... Useful forr Debugging.

*Note: Vim Has Plugins which can be installed for easier use of this bracket Matching and possibly anything you can think of, if u cant find it, time to make a plugin ;)*

* :s is the substitute command
* it is like find and replace
* Syntax- :s/oldtext/newtext/g where g stands for global changing every instance of that word.

##### Variations are :
>type   :#,#s/old/new/g    where #,# are the line numbers of the range
                               of lines where the substitution is to be done.
     Type   :%s/old/new/g      to change every occurrence in the whole file.
     Type   :%s/old/new/gc     to find every occurrence in the whole file,
                               with a prompt whether to substitute or not.

### Chapter 5

* :! is used to directly execute a command from you terminal and get that right here in vim without leaving it.
* follow it by a bash command to look at what it executes.
* to save file which doesnt have a file name you can use :w filename to name it
* if file already exits, it creates a new copy of that file.
* V is Visual Mode, useful for copying, saving in our case :w file with some selected will make those into a text file.
* r is useful is useful for importing a file directly into file
* type v to enter Visual mode, then press :w enter new file.
* to overwrite v to enter visual mode then :w!
* o to open a line below the current line on a new line, and puts u in insert mode.
* O to open a line above the current line on a new line. and puts u insert mode
* S to deletes current line and puts you in insert mode.

### Fun Fact 
 > . Command to repeat the last command you have used!


*  Explore Registers and master put command
* :r !ls outputs the ls command executed your shell and prints here


* e to get to the last before letter of a word.
* R to replace more than one character...
* C does the same thing but puts you in insert mode and better.

* Use / to search and n to move but if u had replaced first time you want to repeat it, then type n, n , n  to move and choose which to replace with .
* cmd} applies the command to a snippet of code until a blank line is seen.

#### Fact

>   6. Typing ":set xxx" sets the option "xxx".  Some options are:
        'ic' 'ignorecase'       ignore upper/lower case when searching
        'is' 'incsearch'        show partial matches for a search phrase
        'hls' 'hlsearch'        highlight all matching phrases
     You can either use the long or the short option name.
	Prepend "no" to switch an option off:   :set noic

### Chapter 7
* :help to enter help menu
* :help cmd where cmd is a command will show a mini man
* :e ~/.vimrc for unix, :e `$VIM/_vimrc` in windows
* Tab completion Tab or CTRL+D
