# vim

## Musts
* Learn to touch type.

## Remaps
Your fingers will thank you:
* \ to , (or to space)
* ESC to CapsLock (or Control to CapsLock)

## Various essential tips

### Very Important Commands
* `.`     -> Repeat the last action.
* `*`     -> Search for the word under the cursor (like a variable).
* `u`     -> Undo.
* `<c-r>` -> Redo.

### Modes
* Normal -> You should spend most of your time here.
* Insert -> Only for inserting.
* Visual -> Lets you select text visually.
* Command -> Lets you run commands. Accessed with `:`.

There are more.

### Moving around
This is the most critical part. It'll become second nature after a while.

Embrace `w`, `b`, `e`, `ge`.

* `w`  -> Beginning of next word.
* `b`  -> Beginning of previous word.
* `e`  -> Next end of word.
* `ge` -> Previous end of word.

Here is some sample text; it has words.

=====

* Use `F`, `f`, `T` and `t` for line search.
  Go to the next match: `;`. Go to the previous match `,`.
* Use `/`, `?` for file search.
  Go to the next match: `n`. Go to the previous match `N`.

Rule of thumb: If on the same line, use: `f`, `F`, `t`, `T`. Else, use: `/`, `?`.

=====

* `gg` -> Go to the top of the file.
* `G`  -> Go to the end of the file.
* `H`  -> High.
* `L`  -> Low.
* `M`  -> Middle.

=====

* `(`, `)` -> Go to the start or end of a sentence.
* `{`, `}` -> Go to next or previous paragraph. Works great with code.

=====

* $    -> Go to the last character of the current line.
* ^    -> Go to the first character of the current line.
* %    -> Go to matching (, ", {, etc.
* <#>G -> Go to line <#>.

### Inserting text
* `I` -> Insert at the beginning of the line.
* `A` -> Insert at the end of the line.
* `S` -> Delete current line and insert.
* `D` -> Delete line from current cursor position.
* `C` -> Delete line from current cursor position and go into Insert mode.

* `ea`  -> Append at the end of the current word.
* `gea` -> Append at the end of the previous word.

### Dealing with (, [, {, ", '
* `ci(` -> Change inside (
* `yi(` -> Yank inside (
* `di(` -> Delete inside (

* `ya(` -> Yank around (

Replace `(` with `{`, `"`, or any text object like `w`ord, `p`aragraph, etc.

Frequently used:
* `ciw` -> Change inside word
* `daw` -> Delete around word
* `ci"` -> Change inside quotes

### Mistakes
Don't hhhhhhhhhh until you get to the error.

Use `F` to get to the error and:
* `x`     -> DDeletes the char under the cursor.
* `r`     -> Replaces the char under the cutsor with another one.
* `xp`    -> Swaps two charactesr.
* `ddp`   -> Swaps two lines.
* `<c-w>` -> Deletes the last word in Insert mode.
* `ciw`   -> Change inside word

### Visual Modes
Visual mode is like selecting text with a mouse.
* `v`     -> Character-wise visual mode.
* `V`     -> Line-wise visual mode.
* `<c-v>` -> Block-wise visual mode.

Hint: motions also work in all visual modes: `f`, `ip`, `W`, etc.

Visual mode is powerful with when combined with `r` or `c`, or with `A` or `I`.

Use block-wise visual mode when you want to edit columns quickly.

Ex.: To append semicolons at the end of multiple lines: `<c-v>jj$A;<esc>`

To reselect the last visual mode selection -> `gv`

### Arrow keys
It's your choice, but I recommend you put this in your vimrc:

`map <Left>  :echo "NO!"<cr>`

Do the same for Right, Up and Down.

### Opening projects
Vim can open directories:

`$ vim ~/code`
or
`$ vim .`

### Running shell commands inside vim
`:! <command>` -> Runs <command> in a shell without leaving vim!

The character % represents the current buffer.

`:! gcc %` -> Compiles current file. You can also use the full name of the file.

### Makefiles
You don't have to leave vim to run your makefiles. Try:

`:make`

After that, you can try:

* `:cn` -> Go to the line of the next error.
* `:cc` -> See all errors.

### Miscelaneous
* `q:`    -> Open up the command history. Careful with `:q`.
* `<c-a>` -> To +1 next number without going into Insert mode.
* `<c-x>` -> To -1 next number without going into Insert mode.
* `=`     -> Indent selected lines (with Visual mode). Useful for code.
* `==`    -> Indent current line. No Visual selection required.

If you need to do a quick task in the terminal, don't quit vim; instead, suspend.
`<c-z>` -> Puts vim in the background and returns to the terminal.
To bring vim back to the foreground, type `fg` in the terminal.

## Plugins
Golden rule: don't install anything that you don't understand.

That said, there are a few plugins that I find essential:
* [Vundle] (https://github.com/gmarik/vundle)
* [Ctrl-P] (https://github.com/kien/ctrlp.vim)
* [Commentary] (https://github.com/tpope/vim-commentary)
* [Git gutter] (https://github.com/airblade/vim-gitgutter)

## Colors
* [Base16] (https://github.com/chriskempson/base16)
* [Solarized] (http://ethanschoonover.com/solarized)

## Resources
* [Vimcasts] (http://vimcasts.org/episodes/archive)
* [Practical vim] (http://www.amazon.com/Practical-Vim-Thought-Pragmatic-Programmers/dp/1934356980/)
* [Cheatsheet] (http://www.viemu.com/vi-vim-cheat-sheet.gif)
* [The vim subreddit] (http://www.reddit.com/r/vim)
* The #vim channel on freenode
