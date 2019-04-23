markdown file
* i insert mode
* x delete a char
* dd delete a line
* p paste

***insert mode***
* a-i insert after/infront
* o-O insert a new line below/above
* cw replace the word from cursor

***move cursor***
* 0 to the home(real head)
* ^ to the head
* % to the end(real end)
* /pattern search pattern
* g_ to the end

***copy and paste***
* p/P paste after/infront the cursor
* yy copy current line

***Undo/Redo***
* u undo
* ctrl+r redo

***open/save/quit/change file***
* :e <path/to/file> open file
* :w save
* :q quit
* :saveas <path/to/file> 
* :x/ZZ/:wq save and quit
* :bn/:bq shift the file

***tips***
* . do the last operation
* N<command> repeat command N times

***move the cursor***
* NG move to Nth line
* :N move to Nth line
* gg move to 1st line = 1G/:1
* G  move to last line
* w/e move the infront/end of next word
* % move the next match bracket
* */# move the last/next same word