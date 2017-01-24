# node-mapnik

Bindings to [Mapnik](http://mapnik.org) for [node](http://nodejs.org). 

[![NPM version][npm-image]][npm-url]
[![Build status][ci-image]][ci-url]
[![Dependency Status][daviddm-image]][daviddm-url]

## Install

We do not provide pre-built binaries; rather, we've tested compilation on a few common platforms:

### Ubuntu 12.04 and 14.04

#### 1. Install apt packages

```sh
# install apt sources
sudo apt-get install curl software-properties-common
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo add-apt-repository ppa:mapnik/nightly-trunk
sudo apt-get update

# install mapnik libs
sudo apt-get install libmapnik libmapnik-dev mapnik-input-plugin-gdal mapnik-input-plugin-postgis mapnik-utils mapnik-vector-tile libstdc++-5-dev clang-3.8 make  
```

#### 2. Setup environment

```sh
export CXX=clang++-3.8
export CC=clang-3.8
```

### OSX

#### 1. Install brew packages

```sh
brew install freetype harfbuzz libpng libtiff proj icu4c jpeg webp boost gdal postgresql cairo llvm
```

#### 2. Compile mapnik

```sh
git clone https://github.com/mapnik/mapnik.git
cd mapnik
git checkout v3.0.9
git submodule update --init
./configure CXX=/usr/local/opt/llvm/bin/clang++-3.8 CC=/usr/local/opt/llvm/bin/clang-3.8
make
sudo make install
```

## `npm install @langa/mapnik`

## What is this Fork?

[node-mapnik](https://github.com/mapnik/node-mapnik) module is really difficult to install properly, and bad patch versions have broken our builds in the past. We will keep this module up-to-date with the upstream work to the extent it does not cause more build/install failures.

## License

BSD

## Maintained By
[<img src='http://i.imgur.com/Y03Jgmf.png' height='64px'>](http://langa.io)</img>

[npm-image]: https://img.shields.io/npm/v/@langa/mapnik.svg?style=flat-square
[npm-url]: https://npmjs.org/package/@langa/mapnik
[ci-image]: https://img.shields.io/travis/langateam/node-mapnik/master.svg?style=flat-square
[ci-url]: https://travis-ci.org/langateam/node-mapnik
[daviddm-image]: http://img.shields.io/david/langateam/node-mapnik.svg?style=flat-square
[daviddm-url]: https://david-dm.org/langateam/node-mapnik
