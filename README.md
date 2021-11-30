# init.vim

My nvim config, from Uruguay to the world xD

I wanted to keep it as minimal as possible. The goal is to work with react+node while being able to find my files using fzf, finding text within them using `Ag` and having keybindings be as similar to `vscode`'s as possible.

You may love vscode's way of solving conflicts, I know I do. If that's the case, the tool I chose to deal with git conflicts which I found to be the simplest and closest to vscode's offering is [conflict-marker.vim](https://github.com/rhysd/conflict-marker.vim), it's just so simple.

## Installation steps

1. Install nvim

```zsh
brew install nvim
```

2. Clone this repo to `~/.config/nvim`

3. Install [vim-plug](https://github.com/junegunn/vim-plug) if it's not already installed on your system

```zsh
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

4. Install [Ag](https://github.com/ggreer/the_silver_searcher) if you don't have it already.

```zsh
brew install the_silver_searcher
```

5. Open nvim and run `:PlugInstall`

## Useful tips

### Searching within a file

1. Press `/`.
2. Type the search pattern.
3. Press `Enter` to perform the search.
4. Press `n` to find the next occurrence or `N` to find the previous occurrence.

### Searching in all files

Tap `Ctrl+F` to use `Ag` to look for any given text in all your files known by git

### Look for a file by name

Tap `Ctrl+P` to bring up `fzf` and start typing your filename

### Split screen

1. Tap `Ctrl+W` and then `V` (for vertical split) or `S` (for horizontal split).
2. Tap `Ctrl+W` and then either `L` or `H` to navigate between vertical splits OR `J` or `K` to navigate between horizontal splits.

### Copying text

1. Go into `VISUAL` mode.
2. Select all the text you want to copy.
3. Use key combo `"+y` to copy to the OS clipboard OR just `y` to copy within VIM.

### Looking at previous revisions of a file with vim-fugitive and vim-unimpaired

1. `:Gclog -10 %` will load the last ten commits that affected the currently open file into the quickfix list.
2. To navigate between revisions just use `[q` and `]q`.

### Solving git conflicts with conflict-marker.vim

- Navigate between conflict markers using `[x` and `]x`.
- Use bindings to choose what version you want to keep:
  - `ct` to keep incoming version
  - `co` to keep current version
  - `cb` to keep both versions
  - `cB` to keep both versions in reverse order
  - `cn` to keep nothing

### Going back to previous cursor position

Press `Ctrl+O`.

### Show symbol documentation in ts/js

Press `Shift+K`.

#### Some other coc.nvim shortcuts

- `gd` => go to definition
- `gi` => go to implementation
- `gr` => find all references

### Going to the beginning/end of a file

- `gg` to go to the beginning of the current file.
- `G` to go to the end of the current file.

## Potential problems

- You may have `coc.nvim` throw some errors because python is not properly configured. If the language is already installed the error might be you don't have the `neovim` package installed, which can easily be solved by running `pip install neovim`
- Does the thing look ugly AF with tons of unsupported characters? You're just missing a font, a [`Nerd Font`](https://www.nerdfonts.com/) in particular! Install one (or all fonts using the script they provide) from their repo [right here](https://github.com/ryanoasis/nerd-fonts) and set one to your terminal profile, the one I like is `Ubuntu Nerd Font Mono`.
