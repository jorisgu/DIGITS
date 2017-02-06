## Dependencies

Install some dependencies with Deb packages:
```sh
sudo apt-get install --no-install-recommends git graphviz python-dev python-flask python-flaskext.wtf python-gevent python-h5py python-numpy python-pil python-pip python-protobuf python-scipy
```

## Download source

```sh
# example location - can be customized
DIGITS_ROOT=~/soft/digits
git clone https://github.com/NVIDIA/DIGITS.git $DIGITS_ROOT
```



## Python packages

Several PyPI packages need to be installed:
```sh
sudo pip install -r $DIGITS_ROOT/requirements.txt
```

If bug with setuptools/easy-install :
```sh
sudo pip install -r $DIGITS_ROOT/requirements.txt --ignore-installed
```


# [Optional] Enable support for plug-ins
```
sudo pip install -e $DIGITS_ROOT
```

# Starting the server

```sh
./digits-devserver
```

Starts a server at `http://localhost:5000/`.
```
$ ./digits-devserver --help
usage: __main__.py [-h] [-p PORT] [-d] [--version]

DIGITS development server

optional arguments:
  -h, --help            show this help message and exit
  -p PORT, --port PORT  Port to run app on (default 5000)
  -d, --debug           Run the application in debug mode (reloads when the
                        source changes and gives more detailed error messages)
  --version             Print the version number and exit
```
