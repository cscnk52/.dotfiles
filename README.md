# My dotfiles...

Before using:

- generate ssh key
- generate gpg key

```bash
cd ~
git clone git@github.com:cscnk52/.dotfiles.git
cd .dotfiles
sudo pacman -S stow
stow ...
```

## Important stuff:

### pacman

```bash
cp ~/.dotfiles/pacman/pacman.conf /etc/pacman.conf
```

### Vim

#### install [vim-plug](https://github.com/junegunn/vim-plug)

```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

reference from: https://github.com/junegunn/vim-plug#unix

#### link files via stow

```bash
cd ~/.dotfiles
stow vim
```

### Zsh

install [zinit](https://github.com/zdharma-continuum/zinit) 

```bash
bash -c "$(curl --fail --show-error --silent --location https://raw.githubusercontent.com/zdharma-continuum/zinit/HEAD/scripts/install.sh)"
```

reference from: https://github.com/zdharma-continuum/zinit#install

#### link file via stow

```bash
cd ~
rm .zshrc
cd .dotfiles
stow zsh
```

remember to restart zsh