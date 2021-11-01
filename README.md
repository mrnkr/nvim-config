# init.vim

My nvim config, from Uruguay to the world xD

I wanted to keep it as minimal as possible. The goal is to work with react+node while being able to find my files using fzf, finding text within them using `Ag` and having keybindings be as similar to `vscode`'s as possible.

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


## Potential problems

* You may have `coc.nvim` throw some errors because python is not properly configured. If the language is already installed the error might be you don't have the `neovim` package installed, which can easily be solved by running `pip install neovim`

