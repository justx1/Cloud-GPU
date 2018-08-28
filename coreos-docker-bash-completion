# Run this as CoreOS user

set -e
cd $HOME
toolbox dnf -y install bash-completion wget \
  && toolbox wget https://raw.githubusercontent.com/docker/cli/master/contrib/completion/bash/docker -O /usr/share/bash-completion/completions/docker \
  && toolbox cp /usr/share/bash-completion /media/root/var/ -R 

cp $(readlink .bashrc) .bashrc.new && mv .bashrc.new .bashrc

echo "source /var/bash-completion/bash_completion" >> ~/.bashrc
