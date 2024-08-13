## NOTE: 
I don't use any 3rd part plugin manager (pathen or vim-plug) anymore. Only use vim8+ built-in package management systerm.
### Where: 
  `~/.vim`
### Where config:
  `~/.vim/my_configs.vim`

### How to install/update plugins
Just 
  `git clone https://repo_url/blah.git ~/.vim/pack/myplugins/start/blah`

Or put the `name repo_git_url` as a line as in the `~/.vim/update_plugins.py`, then run
`python update_plugins.py` and it's updates all of them. 

The `update_plugins.py` (customized with my own folders)  and the files in `~/.vim/vimrcs/` were from `https://github.com/amix/vimrc`.  
