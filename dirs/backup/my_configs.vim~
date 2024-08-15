
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Files, backups and undo
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Turn backup off
" set nobackup
" set nowb " nowritebackup"
" set noswapfile
"
" but NO, Ray need backup, so setting up a backup directory
set backup
if !isdirectory($HOME."/.vim/dirs/backup")
    silent! execute "!mkdir ~/.vim/dirs/backup"
endif
set backupdir=~/.vim/dirs/backup
"not generate .swap
set noswapfile

"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Text, tab and indent related
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Be smart when using tabs ;)
set smarttab

" Use spaces instead of tabs
set expandtab
" 1 tab == 4 spaces
set shiftwidth=4
set tabstop=4 " set ts=4"

" to convert the current tab to space:
" retab (map F2 for retab)
map <F2> :retab <CR> :wq! <CR>

set ai "Auto indent
set si "Smart indent

""""""""""""""""""""""""""""""
" => Visual mode related
""""""""""""""""""""""""""""""
if has("autocmd")
    autocmd BufWritePre *.tf,*.yml,*.txt,*.js,*.py,*.wiki,*.sh,*.coffee :call CleanExtraSpaces()
endif


" Mark if a line goes beyond 81 
" highlight OverLength ctermbg=red ctermfg=white guibg=#592929
" match OverLength /\%81v.\+/

" Another short way
" match ErrorMsg '\%>80v.\+'
"
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Fast editing and reloading of vimrc configs
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
map <leader>e :e! ~/.vim/my_configs.vim<cr>
autocmd! bufwritepost ~/.vim/my_configs.vim source ~/.vim/my_configs.vim


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" => Turn persistent undo on 
"    means that you can undo even when you close a buffer/VIM
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
try
    set undodir=~/.vim/dirs/undo
    set undofile
catch
endtry
