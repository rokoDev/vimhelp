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

## find and replace(at first you should switch to COMMAND mode: `Esc`)
General form:`[range]s/{pattern}/{string}/[flags] [count]`
  The command searches each line in `[range]` for a `{pattern}`, and replaces it with a `{string}`. `[count]` is a positive integer that multiplies the command.
  If no `[range]` and `[count]` are given, only the pattern found in the current line is replaced. The current line is the line where the cursor is placed.
  By default search is case sensitive. To ignore case, use `i` flag.

Examples:
- replace first occurrence of `foo` in the current line with `bar`: `s/foo/bar/`
- replace all occurrences of `foo` in the current line with `bar`: `s/foo/bar/g`
- replace all occurrences of `foo` in the entire file with `bar`: `%s/foo/bar/g`
- replace all occurrences of `foo`, `Foo`, `fOO`, etc. in the entire file with `bar`: `%s/foo/bar/gi`

If we need to search for or replace with a string that contains special character(e.g. `/`) then we should use back slash as escape character(`\`).
Example:
- replace all occurrences of `path/to/foo` in the entire file with `fixed/path/to/foo`: `%s/path\/to\/foo/fixed\/path\/to\/foo/g`

The same as above can be achieved by using any other non-alphanumeric single-byte character except as a delimiter instead of slash `/`:
- replace all occurrences of `path/to/foo` in the entire file with `fixed/path/to/foo`: `%s|path/to/foo|fixed/path/to/foo|g`

## quit(at first you should switch to COMMAND mode: `Esc`)
- to quit (short for `:quit`): -------------------------------------------------------------- `:q`
- to quit without saving (short for `:quit!`): .............................................. `:q!`
- to write and quit: ------------------------------------------------------------------------ `:wq`
- to write and quit, attempting to force the write if the file lacks write permission: ...... `:wq!`
- to write and quit; like `:wq` but writes only if modified (short for `:exit`): ------------ `:x`
- to quit all (short for `:quitall`): ....................................................... `:qa`
- to quit, without saving, with a nonzero exit code to indicate failure (short for `:cquit`): `:cq`
