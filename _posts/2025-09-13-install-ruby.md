## Install Ruby

Referring to this site: https://github.com/rbenv/rbenv?tab=readme-ov-file#installing-ruby-versions
> benv is a version manager tool for the Ruby programming language on Unix-like systems. It is useful for switching between multiple Ruby versions on the same machine and for ensuring that each project you are working on always runs on the correct Ruby version.

### Install rbenv
```bash
# install rbenv with Homebrew
brew install rbenv
```

```bash
# set up shell to load rbenv
rbenv init
```

```bash
# restart zsh
exec zsh
```

### Install specific version of Ruby

```bash
# list latest stable versions:
rbenv install -l

# install a Ruby version:
rbenv install 3.1.2
```

**Useful commands**
```bash
# list all locally installed Ruby versions known to rbenv
rbenv versions

# view the currently active Ruby version and where it is set from
rbenv version

# set the Ruby version for this directory
rbenv local 3.1.2

# set the default Ruby version for this machine
rbenv global 3.1.2   
```
\* It seems that although my rbenv has changed the global version to 3.1.2, `ruby -v` still shows version 2.6.0. 

To fix this, do the following:
```bash
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(rbenv init -)"' >> ~/.zshrc

source ~/.zshrc
```

```bash
ruby -v
-> ruby 3.1.2p20 (2022-04-12 revision 4491bb740a) [arm64-darwin24]
```

## Install gem

```bash
gem install bundler
```

Error happens here! 
> ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /Library/Ruby/Gems/2.6.0 directory.

Just simply do the following and rerun `gem install bundler`
```bash
sudo chown -R $USER /Library/Ruby/Gems/
```

