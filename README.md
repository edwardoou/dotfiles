![Dotfiles](https://energy1011.gitlab.io/monsterpenguin/assets/logo-dotfiles.png)
# dotfiles
Son mis dotfiles, no hago uso de una utilidad, primero quiero usarlos asi, en caso necesite alguno usar de referencia.
- [FreeCodeCamp](https://www.freecodecamp.org/news/dotfiles-what-is-a-dot-file-and-how-to-create-it-in-mac-and-linux/)
- [Utilidades](http://dotfiles.github.io/utilities/)
- [Alternativa de utilidad](https://github.com/CodelyTV/dotly)
- [Que son los dotfiles?](https://www.youtube.com/watch?v=r_MpUP6aKiQ)

## Steps to bootstrap a new Mac

1. Install Apple's Command Line Tools, which are prerequisites for Git and Homebrew.

```zsh
xcode-select --install
```


2. Clone repo into new hidden directory.

```zsh
git clone https://github.com/edwardoou/dotfiles ~/.dotfiles
```

3. Create symlinks in the Home directory to the real files in the repo.

```zsh
# There are better and less manual ways to do this;
# investigate install scripts and bootstrapping tools.
ln -s ~/.dotfiles/.zshrc ~/.zshrc
ln -s ~/.dotfiles/.gitconfig ~/.gitconfig
```
4. Install Homebrew, followed by the software listed in the Brewfile.

```zsh
# These could also be in an install script.
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
# Then pass in the Brewfile location...
brew bundle --file ~/.dotfiles/Brewfile
# ...or move to the directory first.
cd ~/.dotfiles && brew bundle
```

Move files:
```zsh
mv ~/.<archivo> ~/dotfiles/
```

Link files:
```zsh
ln -s ~/dotfiles/.<archivo>  ~/.<archivo>
```

## BrewFile  
- Source: [Pumpingco](https://pumpingco.de/blog/brewfile/)  
- Comando:  
```s
brew bundle --file ~/my-folder/Brewfile
```
**Antes revisar bien la documentacion**
