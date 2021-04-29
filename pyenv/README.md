## pyenv

#### Install Dependencies

`
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl
`

#### pyenv-installer

`
curl https://pyenv.run | bash
`

#### Paste to bashrc/zshrc
```
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

#### Eg. list python version starting with 3.

`
pyenv install --list | grep " 3\."
`

#### Installing python version

`
pyenv install 3.8-dev
`

#### Show installed
`
pyenv versions
`

#### Set global version
`
pyenv global 2.7.15
`

#### Local version (folder specific - it creates .python-version file)
`
pyenv local 2.7.15
`

#### Shell - just to test specific version (just current shell window)
`
pyenv shell 3.8-dev
`

#### Creating Virtual Environments
`
pyenv virtualenv 3.6.8 myproject
`

#### Activating Your Version (it will put environment to .python-version)
`
pyenv local myproject
`

#### Activate / Deactivate environments
```
pyenv activate <environment_name>
pyenv deactivate
```
