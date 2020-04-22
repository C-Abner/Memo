
# vim shortcut
- b : prev work
- w : next work
- [C-w] r : switft tab page

# about mapping
- nnoremap 	: normal mode
- inoremap 	: input mode
- vnoremap 	: v mode

# neovim
- https://liginc.co.jp/409849
- [neovim release](https://github.com/neovim/neovim/releases/tag/v0.4.3)
- vim-go for neovim [Here](https://qiita.com/tobita0000/items/22d314515f009e721740)
- copy to clipboard
```
 # install vim-gnome (only ubuntu supported)
 sudo apt-get install vim-gnome
 
 # add this cammnd into vimrc
 set clipboard=unnamedplus
```

# vimdiff
```
do : copy from other tab
dp : push to other tab
[[ : prev diff
]] : next diff
```

# vim plugins
https://github.com/junegunn/vim-plug

# vim : copy to clipboard
- http://tateren.hateblo.jp/entry/2017/07/21/213020

# cscope for vim

- execute command
`/usr/local/bin/ctags   -a  -f tags  -R .`

- cscope for vim
	https://github.com/tsuyopon/memo/blob/master/DEVTOOLS/Cscope.md
- cscope for vim's ERROR fix method
	add `set nocsverb` into cscope.vim
	
- ctags for golang
   [gotags - github](https://github.com/jstemmer/gotags)	

- cmd for cscope ctages make
```
find -L . -name '*.go' -o -name '*.c' -o -name '*.h' > cscope.files
gotags -R ./* > tags
cscope -R -b
```
- reset cscope in vim
```
:!cscope -Rbq
:cs reset
```
