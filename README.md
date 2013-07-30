dotfiles.git
============
Clone and run this on a new EC2 instance running Ubuntu 12.04.2 LTS to
configure your `bash` and `vim` development environment as follows:

```sh
cd $HOME
git clone https://github.com/startup-class/dotfiles.git
ln -sb dotfiles/.screenrc .
ln -sb dotfiles/.bash_profile .
ln -sb dotfiles/.bashrc .
ln -sb dotfiles/.bashrc_custom .
test -e .vim/bundle && mv .vim/bundle .vim/bundle.old
test -e .vim/autoload/pathogen.vim && .vim/autoload/pathogen.vim.old
ln -s dotfiles/.vim/bundle .
ln -s dotfiles/.vim/autoload/pathogen.vim .
```

See also http://github.com/startup-class/setup to install prerequisite
programs. See the
[Startup Engineering Video Lectures 4a/4b](https://class.coursera.org/startup-001/lecture/index)
for more details.
