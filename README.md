# Vim-Settings

# [플러그인](https://github.com/junegunn/vim-plug)


# 현재 설정된 vim

```
" Install vim-plug
" curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
"   https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
"

call plug#begin('~/.vim/plugged')
" Plug 'tpope/vim-sensible'
" Plug 'neoclide/coc.nvim', {'branch': 'release'}
" tagbar
" nerdtree
" indent-guides
" gitgutter
" fugitive
"
" 'nanotech/jellybeans.vim' - https://github.com/nanotech/jellybean...
" 'majutsushi/tagbar' - https://github.com/majutsushi/tagbar
" 'scrooloose/nerdtree' - https://github.com/scrooloose/nerdtre...
" 'nathanaelkane/vim-indent-guides' - https://github.com/nathanaelkane/vim-...
" 'airblade/vim-gitgutter' - https://github.com/airblade/vim-gitgu...
" 'tpope/vim-fugitive' - https://github.com/tpope/vim-fugitive
" 'vim-airline/vim-airline' - https://github.com/vim-airline/vim-ai...
" 'vim-airline/vim-airline-themes' - https://github.com/vim-airline/vim-ai...
" 'blueyed/vim-diminactive' - https://github.com/blueyed/vim-dimina...
" 'junegunn/vim-easy-align'
" '*/gv.vim'

" Plug 'neoclide/coc.nvim', {'branch': 'release', 'do': './install.sh'}
Plug 'scrooloose/nerdtree'
Plug 'Xuyuanp/nerdtree-git-plugin'
Plug 'nanotech/jellybeans.vim'
Plug 'majutsushi/tagbar'
Plug 'nathanaelkane/vim-indent-guides'
Plug 'airblade/vim-gitgutter'
Plug 'tpope/vim-fugitive'
Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'
Plug 'blueyed/vim-diminactive'
Plug 'junegunn/vim-easy-align'
Plug 'Valloric/YouCompleteMe'
Plug 'honza/vim-snippets'
Plug 'SirVer/ultisnips'
Plug 'terryma/vim-multiple-cursors'

call plug#end()

if has("syntax")
    syntax on
endif

set nocompatible
set number
set cindent
set ts=4
set sw=4
set backspace=indent,eol,start
set smarttab
set smartindent
set expandtab
set relativenumber

" for vim-airline
let g:airline#extensions#tabline#enabled = 1 " turn on buffer list
let g:airline_theme='hybrid'
set laststatus=2 " turn on bottom bar

" let g:UltiSnipsExpandTrigger="<Tab>"
" let g:multi_cursor_use_default_mapping=0
" let g:multi_cursor_next_key='<C-n>'
" let g:multi_cursor_prev_key='<C-p>'
" let g:multi_cursor_skip_key='<C-x>'
" let g:multi_cursor_quit_key='<Esc>'

" YouCompleteMe
let g:ycm_global_ycm_extra_conf='~/.vim/.ycm_extra_conf.py'
let g:ycm_key_list_select_completion = ['<C-j>', '<Down>']
let g:ycm_key_list_previous_completion=['<C-p>', '<Up>']
let g:ycm_collect_identifiers_from_comments_and_strings = 1
let g:ycm_complete_in_strings = 1
let g:ycm_complete_in_comments = 1
let g:ycm_min_num_of_chars_for_completion = 1
" let g:ycm_filetype_blacklist = {}

" UltiSnips
let g:UltiSnipsExpandTrigger='<Tab>'
let g:UltiSnipsJumpForwardTrigger='<Tab>'
let g:UltiSnipsJumpBackwardTrigger='<S-Tab>'
let g:UltiSnipsEditSplit="vertical"

"Change Pmenu
hi Pmenu ctermfg=255 ctermbg=Darkgray guibg=Yellow
hi PmenuSel ctermfg=White ctermbg=0 guibg=White
```
