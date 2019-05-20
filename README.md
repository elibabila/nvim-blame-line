# nvim-blame-line
A small plugin that uses neovims virtual text to print git blame info at the end of the current line.

Also supports showing blame below the current window, for normal vim users.

nvim-blame-line prints author, date and summary of the commit belonging to the line underneath the cursor.
Just like a real IDE!

### Installation:
Use a plugin manager like [vim-plug](https://github.com/junegunn/vim-plug)

```
Plug 'tveskag/nvim-blame-line'
```

### Usage:

![example gif](https://github.com/tveskag/nvim-blame-line/blob/master/img/example.gif "Example gif")

#### Functions
the plugin is exposed through the functions:

EnableBlameLine, 
DisableBlameLine, 
ToggleBlameLine

example:

```
nmap <silent> <leader>b :ToggleBlameLine<CR>
```

#### Options
 
To show blame info below the current window instead, put this in your vimrc:

```
let g:blameLineUseVirtualText = 0
```

Set the timer to query git blame via (default = 70, instant)
```
let g:blameLineDisplayTimer = 2500

