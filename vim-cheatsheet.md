# Vim Cheatsheet

# Moving Around
- *h* - Move one character to the left
- *j* - Move down one line
- *k* - Move up one line
- *l* - Move one character to the right
- *0* - Move cursor to the beginning on the line
- *$* - Move cursor to the end of the line
- *w* - Moves forward one word
- *b* - Moves backward one word
- *G* - Moves to the end of the file
- *gg* - Moves to the beginning of the file
- *`.* - Moves to the last edit of the file

# Editing
- *d* - Starts the delete operation
- *dw* - Deletes a word
- *d0* - Deletes the beginning of a line
- *d$* - Deletes the end of a line
- *dgg* - Deletes the beginning of a file
- *dG* - Deletes the end of a file
- *u* - Will under last operation
- *CTRL r* - will redo the last undo

# Searching & Replacing
- /<text> - Search for <text> in document, moving forwards
- n - Move to next instance of searched text
- N - Move to previous instance of searched text
- ?<text> - Search for <text> in document, going backwards
- :%/s/<text>/<replacementtext> - Search and replace text
- :%/s/<text>/<replacementtext>/gc - Search and replace text, with confirmation for replacing

# Copying and Pasting
- v - Highlight one character at a time
- V - Highlight one line at a time
- CTRL V - Highlight by columns
- p - Paste text after current line
- P - Paste text on the current line
- y - Yank text into copy buffer

# Word Completion
- CTRL p - Searches and auto-completes previously used words
- CTRL n - Searches and auto-completes next words

# Abbreviations
- :ab <abbreviation> <abbreviated word> - Set abbreviation
- :una <abbreviation> - Clears abbreviation

# View Ports
- :split or CTRL ws - Will split into two viewports, horizontally
- :vsplit or CTRL wv - Will split into two viewports, vertically
- :split <filename> - Will split the vim view into two viewports horizontally and open filename in new viewport
- :vsplit <filename> - Will split the vim view into two viewports vertically and open filename in new viewport
- CTRL wj - Move down to viewport
- CTRL wk - Move up to viewport
- CTRL wr - Moves viewports clockwise
- CTRL WR - Moves viewports counter-clockwise
- CTRL wq - Close viewport

# VIM and Tabs
- vim -p filename1 filename2 - Open multiple files in tabs
- :tabnew - Open a new tab
- gt - to switch to the next tab
- gT - to switch to the previous tab
- :tabc - to close a tab

# Folding
- zf<n>j - creates a fold from the cursor down <n> lines
- zo - opens a fold on the cursor
- zj - moves the cursor to the next fold
- zk - moves the cursor to the previous fold
- zd - deletes the fold at the cursor
- zE - deletes all folds in the document
- zM - closes all open folds
- zR - opens all folds

# Shell
- :sh - Open shell from inside Vim
- exit - Close shell when done and return to Vim

# Sorting
- :! sort - Sort alphanetically after selecting text (using Ctrl + V)

