# Objective

The purpose of this script is to reduce the setup time for a 'plain vanilla´ web application with all the standard bits and pieces already in place.

When you find yourself repeatedly adding more things manually, please update the script to save time in the future.

# Usage

```
make setup NAME=mynewproject
```

or if you do not have the makefile in the same directory:
```
make -f <path_to_makefile>\Makefile setup NAME=<mynewproject>
```

The directory `mynewproject` will be created under the current directory and the structure to create both frontend (JS/Vue/Vuex/router) and backend (Python/CDK/FastAPI) generated.

Additionally a git repository will be initiated, but no commits made.

# Requirements
You will need to have (at least) the following components installed:
* [Node](https://nodejs.org/en/download/)
* [Python](https://www.python.org/downloads/release/python-399/) (3.10 is bnot yet supported in Lambda runtime)
* CDK (`npm install -g aws-cdk`)
* Vue CLI (`npm install -g @vue/cli`)
* [git](https://git-scm.com/downloads)
* make

## make
`make` is available on most linux systems set up for development, but
is lacking on Windows.

The easiest way to install make is to download the mingw [build of make](https://sourceforge.net/projects/mingw/files/MinGW/Extension/make/mingw32-make-3.80-3/) and drop it into
git's bin-folder.

Download the `.tar.gz` file and unpack it (use [7zip](https://www.7-zip.org/download.html)). Rename the file `bin/mingw32-make.exe` to `bin/make.exe` and copy it to `C:\Program Files\Git\mingw64\bin` (or wherever you have installed `git`).
