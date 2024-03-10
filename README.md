# Radhika Ayyangar's Portfolio Site

Based on:
![photorama](https://raw.githubusercontent.com/sunbliss/photorama/gh-pages/photorama_thumb.gif)

## Local devel

### Ruby Env Setup

```
cd $HOME
sudo apt update 
sudo apt install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libxml2-dev libxslt1-dev libcurl4-openssl-dev libffi-dev

git clone https://github.com/rbenv/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
exec $SHELL

git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
exec $SHELL

rbenv install 3.3.0
rbenv global 3.3.0
ruby -v

gem install bundler
gem install jekyll
rbenv rehash
```

### Running Dev Server

```
jekyll serve --config _config.yml,_config_dev.yml
```

> NOTE: The way the above invocation of jekyll works is that it uses the `config.yml` as base and applies those params in `_config_dev.yml` as overrides.
