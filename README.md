# General
<b>
What is vi </br>
Who is Bill Joy </br>
How to start and exit vi </br>
What are the command and insert modes, and how to switch from one to the other </br>
How to edit text </br>
How to cut and paste lines </br>
How to search forward and backward </br>
How to undo </br>
How to quit vi </br>
</b>


 ## To Start vi

```diff 
vi filename	    : edit filename starting at line 1
vi -r filename	    : recover filename that was being edited when system crashe
```


## Moving the Cursor

#####  press _Echap_ one time and press any letter below
```diff 
+ j     :_         _move_ cursor down one line
+ k     :_         move cursor up one line

+ h or <Backspace>  :_  move cursor left one character
+ l or <Space>      :_  move cursor right one character

+ 0 (zero):_       move cursor to start of current line (the one with the cursor)
+ $     :_         move cursor to end of current line
+ w     :_         move cursor to beginning of next word
+ b     :_         move cursor back to beginning of preceding word

+ 1G    :_         move cursor to first line in file
+ nG    :_         move cursor to line n
+ G     :_         move cursor to last line in file

```
```diff 
- u  : UNDO WHATEVER YOU JUST DID; a simple toggle 
```

## Inserting or Adding Text

```diff 
+ i     :_         	insert text before cursor, until <Esc> hit
+ I     :_         	insert text at beginning of current line, until <Esc> hit
+ a     :_         	append text after cursor, until <Esc> hit
+ A     :_         	append text to end of current line, until <Esc> hit
+ o     :_         	open and put text in a new line below current line, until <Esc> hit
+ O     :_         	open and put text in a new line above current line, until <Esc> hit
```


## Changing Text

```diff 
+ r     :_         	replace single character under cursor (no <Esc> needed) 
+ R     :_         	replace characters, starting with current cursor position, until <Esc> hit
+ cw    :_         	change the current word with new text, starting with the character under cursor, until <Esc> hit
+ cNw   :_           change N words beginning with character under cursor, until <Esc> hit; e.g., c5w changes 5 words
+ C     :_         	change (replace) the characters in the current line, until <Esc> hit
+ cc    :_         	change (replace) the entire current line, stopping when <Esc> is hit
+ Ncc or cNc  :_     change (replace) the next N lines, starting with the current line, stopping when <Esc> is hit
```

## Deleting Text

```diff 
+ x    :_         	delete single character under cursor
+ Nx   :_         	delete N characters, starting with character under cursor
+ dw   :_         	delete the single word beginning with character under cursor
+ dNw  :_         	delete N words beginning with character under cursor;e.g., d5w deletes 5 words
+ D    :_         	delete the remainder of the line, starting with current cursor position
+ dd   :_         	delete entire current line
+ Ndd or dNd :_  delete N lines, beginning with the current line;e.g., 5dd deletes 5 lines
+ d$   :_         	Delete (cut) everything from the cursor to the end of the line.
 ```
 
## Cutting and Pasting Text

```diff 
+ yy   :_         	copy (yank, cut) the current line into the buffer
+ Nyy or yNy   :_    copy (yank, cut) the next N lines, including the current line, into the buffer
+ p   :_         	put (paste) the line(s) in the buffer into the text after the current line
```


## Searching Text

```diff 
+   /string   :_         	search forward for occurrence of string in text
+   ?string   :_         	search backward for occurrence of string in text
+ n   :_         	move to next occurrence of search string
+ N   :_         	move to next occurrence of search string in opposite direction
```

## Saving and Reading Files

```diff 
+ :r   :_         	filename<Return>	read file named filename and insert after current line(the line with cursor)
+ :w   :_            write current contents to file named in original vi call

+ :w newfile :_                      write current contents to a new file named newfile
+ :12,35w smallfile   :_         	write the contents of the lines numbered 12 through 35 to a new file named smallfile
+ :w! prevfile   :_         	        write current contents over a pre-existing file named prevfile
```

## To Exit vi

```diff 
+ :x<ENTRER>   :_         	quit vi, writing out modified file to file named in original invocation
+ :wq<ENTRER>  :_         	quit vi, writing out modified file to file named in original invocation
+ :q<ENTRER>   :_         	quit (or exit) vi
+ :q!<ENTRER>  :_         	quit vi even though latest changes have not been saved for this vi call

```

***
 <b> learning all these was pretty interesting!! </b>


## Author 
+ [YOUSRA -:octocat:- BDFT](https://linktr.ee/bdftyousra) 

---

## Resources
+ [Basic-vi-Commands](https://www.cs.colostate.edu/helpdocs/vi.html)

## WARNING!!
```diff
- This repo is done as a school assignment. Beware of copying my responses.
- I recommend you  to read resources and come up with your own solutions instead. Feel free to reach out for help!
- This repo may contain some errors. If you notice any, please add a pull request.
```
