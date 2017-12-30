# .one dot
oh-my-tmux, powerline, should just effing work



```zsh 
cd "${HOME}" &&
git clone https://github.com/jradd/.one.git && echo -n Done
cd "${HOME}"/.one/ && fc-cache fonts 3&>/dev/null  && echo -n Done
cd .tmux
git submodule update --init --recursive --remote;
cd ../fonts && wget -O "${HOME}"/.one/fonts/Inconsolata\ for\ Powerline.otf https://github.com/powerline/fonts/raw/master/Inconsolata/Inconsolata\ for\ Powerline.otf
cd "${HOME}" && ln -s -f .one/.tmux.conf.local
ln -s -f .one/.zshrc
[ -f "~/.vimrc" ] || ln -s -f .one/.vimrc && mkdir -p ~/.vim/bundle/ && cd $_; git clone https://github.com/VundleVim/Vundle.vim.git
~/.vim/bundle/Vundle.vim
cd ~
ln -s -f .one/.zshenv
ln -s -f .one/.zshfunc
ln -s -f .one/.tmux .tmux && source ~/.zshrc;
echo -en "Finally Done. I think" &&
zsh
```

## zshfunc
`_gc_repo <user> <repo>`


## REVERT

```
[ -f "~/.one" ] && rm -rf ~/.one

all_syms=($(find . -maxdepth 1 -type l |xargs stat -f "%Y")) && printf "%s" "\nRemoving Broken
SymLinks\n"
for v in ${all_syms[@]}; do [ -f "$v" ] || echo $v; done && echo -en "Done"
```
