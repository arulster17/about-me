```
set linebreak                    " Do not break in the middle of words
set encoding=utf-8               " Set encoding to UTF-8
set fileencoding=utf-8
set ff=unix                      " Use Unix file format (LF endings)
set scrolloff=5                  " Keep 5 lines of context above/below the cursor
set wrap                         " Wrap long lines
set linebreak                    " Do not break in the middle of words

set wildmenu                     " Enable enhanced command-line completion
set wildmode=longest:full,full   " Show possible matches like autocomplete
set backspace=indent,eol,start   " Enable backspacing in INSERT mode

syntax on                        " Enable syntax highlighting
set number                       " Display line numbers
set cursorline                   " Highlight the current line

" Set true color if available
""if has("termguicolors")
""    set termguicolors
""endif

filetype indent plugin on        " Enable filetype-specific indentation
set tabstop=4                    " Tab width: 4 spaces
set shiftwidth=4                 " Indentation width: 4 spaces
set softtabstop=4                " Soft tab width: 4 spaces
set expandtab                    " Convert tabs to spaces
set smarttab                     " Smart tabbing
set autoindent                   " Auto indentation
set smartindent                  " Smart indentation for C-like languages
set shiftround                   " Shift to the next round tab stop

autocmd FileType c set autoindent cindent " C-specific

set breakindent                  " Enable soft line breaks
set breakindentopt=shift:4       " Indent wrapped lines by 4 spaces

set list                         " Show whitespace characters
set listchars=tab:▸\ ,trail:·    " Customize whitespace display
set ignorecase                   " Ignore case in search
set smartcase                    " Case-sensitive search when uppercase is used
set hlsearch                     " Highlight all search results

set laststatus=2                 " Always show the status line

set statusline=
set statusline+=[Ln\ %3l,\ Col\ %3c]      " Line:Column
set statusline+=\ %{&modified?'[+]':''}   " Modified flag ([+] if modified)
set statusline+=\ %{&readonly?'[RO]':''}  " Read-only flag ([RO] if read-only)
set statusline+=%=                        " Right-align the rest
set statusline+=\ (%3p%%)                 " Percent
set statusline+=\ %t                      " Shorter filename
set statusline+=\ [%{&filetype}]          " Filetype

" "inoremap ( ()<Esc>i
inoremap { {}<Esc>i
inoremap {<CR> {<CR>}<Esc>O
inoremap [ []<Esc>i
""inoremap < <><Esc>i
inoremap ' ''<Esc>i
inoremap " ""<Esc>i
```
