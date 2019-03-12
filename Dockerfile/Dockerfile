FROM ubuntu
MAINTAINER potatoformula potatoformula@gmail.com
RUN apt update
RUN apt upgrade -y
RUN apt install -y vim git curl build-essential
RUN git clone https://github.com/potatoformula/docker-rust-vim-asyncomplete
RUN cp /docker-rust-vim-asyncomplete/root/.*rc /root/
RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
RUN source $HOME/.bashrc
RUN rustup component add rls rust-analysis rust-src
RUN git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
RUN vim +PluginInstall
