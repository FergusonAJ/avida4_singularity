# Avida 4 Singularity Container Recipe
This repository should contain all necessary files to build a [Singularity](https://sylabs.io/) container capable of running [Avida 4](https://github.com/dknoester/avida4), a digital evolution platform. 

To do this, the container installs [Boost v1.71.0](https://boost.org), [Clang v9.0.0](https://clang.llvm.org/), and [ealib](https://github.com/dknoester/ealib) (the library Avida 4 is build on) in an Ubuntu 16.04 container. 

While the recipe is designed to download and run stock Avida 4, it should be easy to modify it to run a variant of Avida, or your own code!

## Building and Running
1. Install Singularity on your machine [(Singularity's install guide)](https://sylabs.io/guides/3.4/user-guide/installation.html). 
2. Download this repo, navigate to it in a terminal, and build it via:
```
sudo singularity build avida4.simg avida4_singularity_recipe
```
This takes a few moments. After it completes, you should be able to run avida with
```
./avida4.simg
```
To add command line arguments, just append them to the end of the call (they just get passed through). For example:
```
./avida4.simg --ea.rng.seed 1234
```
