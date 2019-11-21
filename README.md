# Machine Learning

## Setup Python Virtual Environment

Follow [docs](https://github.com/pyenv/pyenv) to install Pyenv.  

Verify the following commands were run
```
brew install pyenv
brew install pyenv-virtualenv
```

Install Python on the virtual environment
```
pyenv install <version>
```

Now it's time to create the virtual environment. Generally for the environment name, I like to add `env_version` to the end to signify it's a virtual environment and easy to know what Python version is being used. For example, my env name would be something like `machine_learning_env_3.6.8`

```
pyenv virtualenv <version> <environment_name>
```

Next, we need to modify our `.zshrc` or `.bash_profile` so that we can work with `pyenv` and `virtualenv`. Add these lines to the bottom of the file

```
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

To initialize our virtual environment, we need to create a file called, `.python-version`. Within the file, add the virtual environment name. When you navigate to that directory within a terminal, it will auto activate. The other option is to manually activate like so

```
pyenv activate <virtual_environment_name>
```

## Tensorflow Setup

Using `pip3` install the requirements. Generally they include
```
tensorflow
numpy
matplotlib
```

When working on a project, I will list my dependencies in a `.requirements.txt` file. Then using `pip3`, I can install everything by running `pip3 install -Ur ./requirements.txt`
