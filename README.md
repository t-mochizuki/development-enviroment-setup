## How to use

I assume that you installed Command Line Tools for Xcode and pyenv on OSX.

If you have not yet installed them, You can install them with a following command line.

``` sh
$ xcode-select --install
$ git clone https://github.com/yyuu/pyenv.git ~/.pyenv
```

And add a following to `~/.bash_profile` or `~/.zshenv`.

``` sh
export PYENV_ROOT=$HOME/.pyenv
export PATH=$PYENV_ROOT/bin:$PATH
eval "$(pyenv init -)"
```

To build Ansible, you do a following command line.

``` sh
$ env LDFLAGS="-L$(brew --prefix openssl)/lib" CFLAGS="-I$(brew --prefix openssl)/include" pip install ansible
```

To run an ansible playbook, you will need to install Python and Ansible.

``` sh
$ git clone https://github.com/t-mochizuki/setup-simple.git
$ cd setup-simple
$ pyenv install 2.7.10
$ pyenv shell 2.7.10
$ pip install ansible
$ ansible-playbook -i hosts site.yml
```

Maybe you need to install gnu-tar. you can install gnu-tar with Homebrew. The command-line is `brew install gnu-tar`.

If you want to dry-run the ansible playbook, try a following.

``` sh
$ ansible-playbook -i hosts site.yml --check
```
