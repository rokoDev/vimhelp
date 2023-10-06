# Vim help:

## switching modes
- to enter INSERT mode: `i`
- to enter COMMAND mode: `Esc`

## moving cursor
- move cursor to the last line: `G`
- move cursor to the first line: `1G`
- move cursor to the n-th line: `nG`
- move cursor to the end of a current line: `$`
- move cursor to the beginning of a current line: `0`
- move cursor one page down: `ctrl+f`
- move cursor one page up: `ctrl+b`
- move cursor to the beginning of the next word: `w`
- move cursor to the beginning of the previous word: `b`
- move cursor to the end of a line and enter INSERT mode: `A`

## putting new line
- put new line ABOVE current line and enter INSERT mode: `O`
- put new line BELOW current line and enter INSERT mode: `o`

## cutting/deleting
- to cut or delete character at current cursor location: `x`
- to cut or delete n characters from the current cursor location: `nx`
- to cut or delete current line: `dd`
- to cut or delete n lines including current: `ndd`
- to cut or delete from the current position to the end of the line: `d$`
- to cut or delete from the current position to the beginning of the line: `d0`
- to cut or delete from the current line to the end of the file: `dG`
- to cut or delete from the current line to the n-th line of the file: `dnG`

## copying
- to copy current line: `yy`
- to copy n lines including current: `nyy`
- to copy from current location to the end of the line: `y$`
- to copy from current location to the beginning of the line: `y0`
- to copy from the current line to the end of the file: `yG`
- to copy from the current line to the n-th line: `ynG`

## pasting
- to past after the cursor position: `p`
- to past before the cursor position: `P`

## quit(at first you should switch to COMMAND mode: `Esc`)
- to quit (short for `:quit`): -------------------------------------------------------------- `:q`
- to quit without saving (short for `:quit!`): .............................................. `:q!`
- to write and quit: ------------------------------------------------------------------------ `:wq`
- to write and quit, attempting to force the write if the file lacks write permission: ...... `:wq!`
- to write and quit; like `:wq` but writes only if modified (short for `:exit`): ------------ `:x`
- to quit all (short for `:quitall`): ....................................................... `:qa`
- to quit, without saving, with a nonzero exit code to indicate failure (short for `:cquit`): `:cq`
