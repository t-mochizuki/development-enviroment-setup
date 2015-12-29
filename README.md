## How to use

I assume that you installed Command Line Tools for Xcode and pyenv on OSX.

If you have not yet installed them, You can install with the following command line.

``` sh
$ xcode-select --install
$ git clone https://github.com/yyuu/pyenv.git ~/.pyenv
```

And add the following to `~/.bash_profile` or `~/.zshenv`.

``` sh
export PYENV_ROOT=$HOME/.pyenv
export PATH=$PYENV_ROOT/bin:$PATH
eval "$(pyenv init -)"
```

To run the ansible playbook, you will need to install Python and Ansible.

``` sh
$ mkdir work
$ cd work
$ git clone https://github.com/t-mochizuki/setup-simple.git
$ cd setup-simple
$ pyenv install 2.7.10
$ pyenv shell 2.7.10
$ pip install ansible
$ ansible-playbook -i hosts site.yml
```
