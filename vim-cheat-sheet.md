## Vim Cheat Sheet

### Navigation

- End of the file: shift + g
- Next line: j
- Go down a defined number of lines: number + j
- Skip to next word: w
- Skip back a word: b
- Skip to next section: W
- Skip back to previous section: B
- Go to end of the line: $
- Go to beginning of the line: 0
- Go to top of the screen: shift + h
- Go to bottom of the screen: shift + l
- Forward multiple words: 5w
- Forward multiple letters: 5l
- Back multiple letters: 5h
- Forward to the next 'y': fy (case sensitive)


### Editing 

- Undo: u
- Redo: ctrl + r
- Inserting text where the cursor is: i
- Inserting text at the start of the line: I
- Insert at the end of the line: shift + a
- Copy entire line: yy or Y
- Paste copied line: p
- Change multiple words: 5cw
- Insert at the end of the line: A


### Deleting

- d<leftArrow> will delete current and left character
- d$ will delete from current position to end of line
- d^ will delete from current backward to first non-white-space character
- d0 will delete from current backward to beginning of line
- dw deletes current to end of current word (including trailing space)
- db deletes current to beginning of current word
- Delete current line: dd
- Delete the line below: shift + j
- Delete entire word: cw
- Delet to the end of the line: shift + C
- Delete multiple lines: d + number of lines + enter
- Delete from current position to a specific line number: d<line number>G
- Deleting all items in a file that start with a pattern: :g/< search term>/d
- Deleting all lines that are empty or that contain only whitespace: :g/^\s*$/d


### Selecting

- Select the entire line: V
- Select a range of text: v
- Select a column: control + v
- Reselect a block: gv
- Select all: ggVG


### Find and Replace

- %s/pattern/text to replace


### Saving

- Save the file: :w
- Save the file and quit: :wq
- Quit without saving: :q!


### Views

- Use horizontal split: :sp filename
- Use vertical split: :vsp filename
- Switch from top to bottom: control + w + j
- Switch from left to right: control + w + l
- Switch from bottom to top: control + w + j
- Switch from right to left: control + w + h


### Search

- While on current line: f + <queried item>
- Search for word in file: /word + enter
- Find next search result: n
- Search backwards: N
- Go to first result: ggn
- Go to last result: GN
- To remove search highlighting: :noh


### Modes

- Normal
- Insert
- Visual
- Replace
- Command Line 


### Multiple Files

- :e filename - Edit a file in a new buffer
- :bnext (or :bn) - go to next buffer
- :bprev (of :bp) - go to previous buffer
- :bd - delete a buffer (close a file)
- :sp filename - Open a file in a new buffer and split window
- ctrl + ws - Split windows
- ctrl + ww - switch between windows
- ctrl + wq - Quit a window
- ctrl + wv - Split windows vertically


### Indenting

- Fix indenting when pasting: set paste in .vimrc file 
- Indenting: visual mode + > or <
- Repeat indenting: .


## Commenting/Uncommenting

- Comment: visual block select with CTRL-V then I# (insert # in the begining)
- Uncomment: visual block select with CTRL-V then X (delete the first symbol on the line)


### Visual Mode

- Changing multiple lines of text: control + v + shift + i + action + esc
- Select elements in paragraph: v + / + content


### Display settings

- Turning on line numbers: :set nu
- Turning on syntax highlighting: :syntax on


### Reseting Vim Settings

```
cd
mv .vimrc .vimrc-old
mv .vim .vim-old
touch .vimrc; mkdir .vim
```

### Help

- To get help: :h <topic>
- To exit help: :bd


### Removing blocks of text in code files

- `c + i + t` will remove the code between HTML tags, such as: `<div>Some content</div>`
- `c + i + }` will remove the code inside of a JavaScript function
