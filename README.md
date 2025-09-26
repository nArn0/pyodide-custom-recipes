pyodide-custom-recipes
======================

Custom recipes to build the pillow wheel for pyodide with libimagequant feature activated.

Versions used for the build:
- `pyenv install 3.12.7`
- `git clone -b 0.27.7 --recursive https://github.com/pyodide/pyodide`
- `git clone -b 20240824 https://github.com/pyodide/pyodide-recipes`

Versions of the packages used:
- libimagequant: 2.18.0
- pillow: 10.2.0

The pyodide version was chosen in order to try and make it available in @gradio/lite. 


Personal notes
--------------

For pyenv:
```
sudo apt-get install libncurses-dev libbz2-dev libreadline-dev libffi-dev libssl-dev liblzma-dev libsqlite3-dev libltdl-dev libpng-dev -y

For pyodide:
```
export PATH := $(PYODIDE_ROOT)/emsdk/emsdk/node/22.16.0_64bit/bin:$(PATH)
```

For rustup:
```
rustup default nightly
rustup target add wasm32-unknown-emscripten
```
