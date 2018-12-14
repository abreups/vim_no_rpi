# vim_no_rpi
instalando vim no RaspberryPi com plugin Vundle e YouCompleteMe


Principal fonte de informação: https://github.com/Valloric/YouCompleteMe#linux-64-bit

1. instale vim do zero, compilando suporte para Python: https://github.com/Valloric/YouCompleteMe/wiki/Building-Vim-from-source
2. dica para compilar o plugin sem erro no RPi: https://nallerooth.com/post/building_ycm_on_raspberry_pi_3/ (usar `YCM_CORES=1 ./install.py --ts-completer`
3. instale o plugin YouCompleteMe: https://github.com/Valloric/YouCompleteMe#linux-64-bit
4. se não deu erro no processo, vim está pronto para usar.


Meu arquivo .vimrc:
```
set nocompatible	" requerido para Vundle
filetype off		" requerido para Vundle

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim

call vundle#begin()
" let Vundle manage Vundle (required)
Plugin 'VundleVim/Vundle.vim' " o próprio Vundle
Plugin 'scrooloose/nerdtree'  " NERDTree plugin
Plugin 'Valloric/YouCompleteMe' "plugin YouCompleteMe

" All of your Plugins must be added before the following line
call vundle#end()	" required
filetype plugin indent on	" required by Vundle
syntax on
set number	" mostra os números da linhas
autocmd vimenter * NERDTree	" carrega o vim já com o plugin NERDTree ativado
```


Alguns plugins para vim com dicas: http://www.dotnetsurfers.com/blog/2016/02/08/using-vim-as-a-javascript-ide
