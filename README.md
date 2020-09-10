# myzsh
My repo to sync zsh settings 

Originally influenced by https://medium.com/wearetheledger/oh-my-zsh-made-for-cli-lovers-installation-guide-3131ca5491fb
and https://github.com/romkatv/powerlevel10k

If workstation on Windows, first we need the fonts:
https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k
- DejaVu Sans Mono for Powerline (https://github.com/powerline/fonts/tree/master/DejaVuSansMono)
- Droid Sans Mono for Powerline (https://github.com/powerline/fonts/tree/master/DroidSansMono)




sh -c '$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)'

sudo apt install fonts-powerline

curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | bash


It might not be the correct place, but lets add some k8s tools here too.

https://itnext.io/kubernetes-command-line-tools-acad11683794
https://github.com/ahmetb/kubectx#installation

cd /tmp
git clone https://github.com/ahmetb/kubectx
cd kubectx
sudo cp kubectx kubens /usr/local/bin
sudo chmod +x /usr/local/bin/kubectx /usr/local/bin/kubens

mkdir -p ~/.oh-my-zsh/completions
chmod -R 755 ~/.oh-my-zsh/completions
ln -s /opt/kubectx/completion/kubectx.zsh ~/.oh-my-zsh/completions/_kubectx.zsh
ln -s /opt/kubectx/completion/kubens.zsh ~/.oh-my-zsh/completions/_kubens.zsh


