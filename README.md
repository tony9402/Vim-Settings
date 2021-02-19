# Vim Setting

[![Vim](https://img.shields.io/badge/version-v8.2-brightgreen)](#)

### My .vimrc

```
" # Vim Plugin
"  - vim-plug
"
" **** How to Install ****
" curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
"   https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
"
" **** Useful Vim Guide ****
" https://github.com/johngrib/simple_vim_guide
"
"
" MEMO
"  :wq! == :x == ZZ

" Plugin List
" 1. nanotech/jellybeans.vim
"  - https://github.com/nanotech/jellybeans.vim
" 2. preservim/tagbar
"  - https://github.com/preservim/tagbar
" 3. scrooloose/nerdtree
"  - https://github.com/preservim/nerdtree
" 4. Xuyuanp/nerdtree-git-plugin
"  - https://github.com/Xuyuanp/nerdtree-git-plugin
" 5. nathanaelkane/vim-indent-guides
"  - https://github.com/nathanaelkane/vim-indent-guides
" 6. airblade/vim-gitgutter
"  - https://github.com/airblade/vim-gitgutter
" 7. tpope/vim-fugitive
"  - https://github.com/tpope/vim-fugitive
" 8. vim-airline/vim-airline
"  - https://github.com/vim-airline/vim-airline
" 9. vim-airline/vim-airline-themes
"  - https://github.com/vim-airline/vim-airline-themes
" 10. blueyed/vim-diminactive
"  - https://github.com/blueyed/vim-diminactive
" 11. junegunn/vim-easy-align
"  - https://github.com/junegunn/vim-easy-align
" 12. Valloric/YouCompleteMe
"  - https://github.com/ycm-core/YouCompleteMe
" 13. honza/vim-snippets
"  - https://github.com/honza/vim-snippets
" 14. SirVer/ultisnips
"  - https://github.com/SirVer/ultisnips
" 15. terryma/vim-multiple-cursors
"  - https://github.com/terryma/vim-multiple-cursors
" 16. shime/vim-livedown
"  - https://github.com/shime/vim-livedown
" 17. wakatime/vim-wakatime
"  - https://github.com/wakatime/vim-wakatime

call plug#begin('~/.vim/plugged')

Plug 'nanotech/jellybeans.vim'
Plug 'majutsushi/tagbar'
Plug 'scrooloose/nerdtree'
Plug 'Xuyuanp/nerdtree-git-plugin'
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
Plug 'shime/vim-livedown'
Plug 'wakatime/vim-wakatime'

call plug#end()

" Setting For colorscheme & syntax
" Using Jellybeans
colorscheme jellybeans

if has("syntax")
    syntax on
endif

" Setting
" :help [ option ]
set autoindent   " Enter the entry in INSERT mode and go down to the next line, which automatically indents it.
set autoread     " Automatically re-read if the contents of the file change outside of the VIM.
set autowrite    " Automatically saves the file whenever you run a specific command with changes in place.
set backspace=indent,eol,start
set cindent 
set smartindent
set clipboard=unnamed
set nocompatible " [ compatible ] Set compatibility with VI. OFF
" set complete
set cursorcolumn " Highlight the column with the cursor.
set cursorline   " Highlight the line with the cursor.
set expandtab    " Press the tab key to enter a set number of spaces, not tabs.
set tabstop=4    " number of <Space>
set hlsearch     " Highlight the search results, the string that matches the search term.
set ignorecase   " Ignore case when searching.
set smartcase    " using with 'ignorecase'
set incsearch    " Perform a search each time you type one character at a time of search.
set langmap=ㅁa,ㅠb,ㅊc,ㅇd,ㄷe,ㄹf,ㅎg,ㅗh,ㅑi,ㅓj,ㅏk,ㅣl,ㅡm,ㅜn,ㅐo,ㅔp,ㅂq,ㄱr,ㄴs,ㅅt,ㅕu,ㅍv,ㅈw,ㅌx,ㅛy,ㅋz
set laststatus=2 " You can set whether the status line is displayed in the last window.
set linebreak    " One line is so long that if you cross the screen, you will express one line in multiple lines, and if you set this option, the line will be cut by word.
set list         " Shows blank characters with the characters set in 'listchars'.
set listchars=tab:»\ ,trail:·
set matchpairs=(:),{:},[:],<:>
set omnifunc=syntaxcomplete#Complete " Using with youcompleteme
set relativenumber
set ruler
set scrolljump=1
set shiftwidth=4
set showbreak=+++\
set showmatch
set smarttab
set visualbell
set whichwrap+=h,l
set wildignore=*o,*.in,*.out
set wildignorecase
set wildmenu
set wrap

" Pmenu
hi Pmenu ctermfg=255 ctermbg=Darkgray guibg=Yellow
hi PmenuSel ctermfg=White ctermbg=0 guibg=White

" Setting for Each Plugin

" vim-airline
let g:airline#extensions#tabline#enabled=1 " turn on buffer list
let g:airline_theme='hybrid'
set laststatus=2

" YouCompleteMe
let g:ycm_server_python_interpreter='/usr/local/bin/python3'
let g:ycm_global_ycm_extra_conf='~/.vim/.ycm_extra_conf.py'
let g:ycm_key_list_select_completion=[ '<C-j>', '<Down>' ]
let g:ycm_key_list_previous_completion=[ '<C-p>', '<Up>' ]
let g:ycm_collect_identifiers_from_comments_and_string=1
let g:ycm_complete_in_string=1
let g:ycm_complete_in_comments=1
let g:ycm_min_num_of_chars_for_completion=1

" UltiSnips
let g:UltiSnipsExpandTrigger='<Tab>'
let g:UltiSnipsJumpForwardTrigger='<Tab>'
let g:UltiSnipsJumpBackwardTrigger='<S-Tab>'
let g:UltiSnipsEditSplit="vertical"

" Markdown Live 
let g:livedown_port=1337
let g:livedown_open=1
let g:livedown_autorun=0
let g:livedown_browser="chrome"

" Setting Mapping

" NERDTREE 
nmap <S-e> :NERDTreeToggle<CR>

" ctags
nmap <C-[> <Esc>:po<CR>

" Markdown Live
nmap <F10> <ESC> :LivedownToggle<CR>

" C++ Compile && Useful PS or CP
let &g:makeprg="(g++ -o run %:r.cpp -O2 -std=c++17 -Wall && time ./run < input)"
nmap <C-J> <ESC>:wa<CR>:make!<CR>:copen<CR><CR>
nmap <C-K> <ESC>:q<CR>
nmap <C-Q> <ESC>:!sed -n '2,$p' %:r.cpp \| pbcopy<CR><CR>
```

### My VIM Info

```
VIM - Vi IMproved 8.2 (2019 Dec 12, 빌드한 날짜 Dec  6 2020 16:01:42)
macOS 버젼
포함된 패치: 1-2100
Compiled by Homebrew
Huge 버젼 GUI 없음.  기능 (+: 포함됨, -: 포함 안 됨):
+acl               -farsi             +mouse_sgr         +tag_binary
+arabic            +file_in_path      -mouse_sysmouse    -tag_old_static
+autocmd           +find_in_path      +mouse_urxvt       -tag_any_white
+autochdir         +float             +mouse_xterm       -tcl
-autoservername    +folding           +multi_byte        +termguicolors
-balloon_eval      -footer            +multi_lang        +terminal
+balloon_eval_term +fork()            -mzscheme          +terminfo
-browse            +gettext           +netbeans_intg     +termresponse
++builtin_terms    -hangul_input      +num64             +textobjects
+byte_offset       +iconv             +packages          +textprop
+channel           +insert_expand     +path_extra        +timers
+cindent           +ipv6              +perl              +title
-clientserver      +job               +persistent_undo   -toolbar
+clipboard         +jumplist          +popupwin          +user_commands
+cmdline_compl     +keymap            +postscript        +vartabs
+cmdline_hist      +lambda            +printer           +vertsplit
+cmdline_info      +langmap           +profile           +virtualedit
+comments          +libcall           -python            +visual
+conceal           +linebreak         +python3           +visualextra
+cryptv            +lispindent        +quickfix          +viminfo
+cscope            +listcmds          +reltime           +vreplace
+cursorbind        +localmap          +rightleft         +wildignore
+cursorshape       +lua               +ruby              +wildmenu
+dialog_con        +menu              +scrollbind        +windows
+diff              +mksession         +signs             +writebackup
+digraphs          +modify_fname      +smartindent       -X11
-dnd               +mouse             -sound             -xfontset
-ebcdic            -mouseshape        +spell             -xim
+emacs_tags        +mouse_dec         +startuptime       -xpm
+eval              -mouse_gpm         +statusline        -xsmp
+ex_extra          -mouse_jsbterm     -sun_workshop      -xterm_clipboard
+extra_search      +mouse_netterm     +syntax            -xterm_save
        시스템 vimrc 파일: "$VIM/vimrc"
        사용자 vimrc 파일: "$HOME/.vimrc"
 사용자 두 번째 vimrc 파일: "~/.vim/vimrc"
         사용자 exrc 파일: "$HOME/.exrc"
       defaults 파일: "$VIMRUNTIME/defaults.vim"
  fall-back for $VIM: "/usr/local/share/vim"
컴파일: clang -c -I. -Iproto -DHAVE_CONFIG_H   -DMACOS_X -DMACOS_X_DARWIN  -g -O2 -U_FORTIFY_SOURCE -D_FORTIFY_SOURCE=1       
링크: clang   -L. -fstack-protector-strong -L/usr/local/lib -L/usr/local/opt/libyaml/lib -L/usr/local/opt/openssl@1.1/lib -L/usr/local/opt/readline/lib  -L/usr/local/lib -o vim        -lm  -lncurses -liconv -lintl -framework AppKit  -L/usr/local/opt/lua/lib -llua5.4 -mmacosx-version-min=11.0 -fstack-protector-strong -L/usr/local/lib  -L/usr/local/Cellar/perl/5.32.0/lib/perl5/5.32.0/darwin-thread-multi-2level/CORE -lperl  -L/usr/local/opt/python@3.9/Frameworks/Python.framework/Versions/3.9/lib/python3.9/config-3.9-darwin -lpython3.9 -framework CoreFoundation  -lruby.2.7     
```
