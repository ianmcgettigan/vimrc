# My VIMRC

```vim
call plug#begin('~/.vim/plugged')
Plug 'lervag/vimtex'
Plug 'sirver/ultisnips'
call plug#end()
syntax enable
filetype plugin on
filetype indent on
set ruler
set backspace=eol,start,indent
set whichwrap+=<,>,h,l
set ignorecase
set smartcase
set hlsearch
set incsearch
set magic
set showmatch
set mat=2
set encoding=utf8
set tabstop=4
set shiftwidth=4
set expandtab
set smarttab
set lbr
set tw=500
set ai
set si
set wrap
set number
set relativenumber
set nu
inoremap {<CR> {<CR>}<Esc>ko
inoremap [<CR> [<CR>]<Esc>ko
inoremap (<CR> (<CR>)<Esc>ko
let g:vimtex_view_method = 'skim'
let g:tex_flavor='latex'
let g:vimtex_quickfix_mode=0
let g:UltiSnipsExpandTrigger       = '<Tab>'    " use Tab to expand snippets
let g:UltiSnipsJumpForwardTrigger  = '<Tab>'    " use Tab to move forward through tabstops
let g:UltiSnipsJumpBackwardTrigger = '<S-Tab>'  " use Shift-Tab to move backward through tabstops
:inoremap WW <Esc>:w<CR>
:noremap WW :w<CR>

colorscheme default

if system("defaults read -g AppleInterfaceStyle") =~ '^Dark'
   set background=dark
else
  set background=light
endif

set clipboard=unnamed

"spell check
set spell spelllang=en_us

autocmd BufWritePost *.md silent !pandoc % -o %:r.pdf
```
