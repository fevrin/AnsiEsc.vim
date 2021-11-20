# AnsiEsc.vim

This is a copy of [Charles Campbell's][author] [`AnsiEsc` vim add-on][original add-on]. I just added it here so [vim-plug][] can install it.

The add-on removes ANSI escape color codes and paints the associated text with the appropriate colors (much more pleasant on the eyes :smile:).

## Installation

As with the typical `vim-plug` installation, you can create a block (or add to an existing one) in your `~/.vimrc` that looks like this:
```vim
call plug#begin('~/.vim/plugged')
   Plug 'https://github.com/fevrin/AnsiEsc.vim', { 'branch': 'main' }
call plug#end()
```

Then open `vim` and execute `:PlugInstall`.

If you want this to run automatically upon loading files that end in `.log`, you can also add this line to your
`~/.vimrc`:
```vim
autocmd BufReadPost,FileReadPost *.log AnsiEsc
```

Otherwise, you can manually enable the plugin while viewing a file that has ANSI color codes by executing `:AnsiEsc`.

[author]: https://www.vim.org/account/profile.php?user_id=96
[original add-on]: https://www.vim.org/scripts/script.php?script_id=302
[vim-plug]: https://github.com/junegunn/vim-plug
