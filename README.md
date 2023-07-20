# ZSH Customization

**This guide provides instructions to customize your Zsh shell with various enhancements, including the installation and configuration of the *Powerlevel10k* theme, *LSD* (a modern replacement for the `ls` command), and *Batcat* (an improved alternative to the `cat` command). Additionally, it covers the configuration of custom aliases in your `.zshrc` file.**

---

#### Powerlevel10k

**Instructions to install and configure the Powerlevel10k theme in your terminal**:

1. Clone the Powerlevel10k repository by running the following command in your terminal:
```shell
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
```
2. Add the following line to your ~/.zshrc file to load the theme:
```shell
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >> ~/.zshrc
```
3. Restart your terminal or run the following command to load the theme:
```shell
zsh
```

---

#### LSD
**Instructions to install LSD, a modern replacement for the ls command, on your system**:

1. Download the `.deb` file from the official LSD repository on GitHub: [Download LSD](https://github.com/lsd-rs/lsd/releases)

2. Install the downloaded package using the following command: 
```shell
sudo dpkg --install [File.deb]
```

---

#### Batcat

**Instructions to install Batcat, an improved alternative to the cat command**: [Download Batcat](https://github.com/sharkdp/bat/releases)

1. Download the `.deb` file from the official Batcat repository on GitHub:

Download Batcat

2. Install the downloaded package using the following command:

```shell
sudo dpkg --install [File.deb]
```

---

#### .zshrc

1. Run the following command to open the `.zshrc` file in the nano text editor:
```shell
sudo nano ~/.zshrc
```
*This will open the .zshrc file with superuser permissions so you can edit it.*

2. Scroll to the end of the file using the keyboard navigation keys.

3. Copy and paste the following code block at the end of the `.zshrc` file:
```shell
# Custom Aliases
alias ls='lsd -l --group-dirs=first'
alias ll='lsd -lh --group-dirs=first'
alias la='lsd -a --group-dirs=first'
alias lla='lsd -lha --group-dirs=first'
alias l='lsd --group-dirs=first'
alias cat='bat'
alias catn='/bin/cat'
alias catnl='/bin/bat --paging=never'
```
*These aliases will add custom functionality to your commands, such as additional options for the ls command and an enhanced replacement for the cat command.*

5. Save the changes to the .zshrc file by pressing `Ctrl + o`, then press `Enter` to confirm the file name and save the changes.

6. Close the nano editor by pressing `Ctrl + x`.

7. Restart your terminal or open a new terminal window for the changes in the `.zshrc` file to take effect.

---

**If you have any further questions or need assistance with the ZSH customization described in this guide, please feel free to reach out to me, Luciano Griffa. I'll be glad to help you.**

---

**By Luciano Griffa | 2023**
