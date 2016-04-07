# asdf-riak

Riak plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

## Dependencies
1. Your default ulimits will be low.  You'll most likely need to increase your ulimits.
1. You will need a compiler.
  * Mac
    1. ```gcc```
    1. Hit the ok button and it will install.  If it already has it, then you are good.
  * Ubuntu  
    1. ```sudo apt-get install linux-headers-$(uname -r) build-essential```
1. You're going to need some libs
  * Mac
    1. None known yet
  * Ubuntu
    1. ```sudo apt-get install libpam0g-dev```
    1. ```sudo apt-get install libncurses-dev```
    1. ```sudo apt-get install openssl libssl-dev```
1. You will need erlang > R16B02, but not R18 yet.  I'm recommending 17.5
  * Mac and Ubuntu 
    1. ```asdf plugin-add erlang https://github.com/asdf-vm/asdf-erlang.git``` 
    1. ```asdf install erlang 17.5```
    1. then make sure and set up your .tool-versions file.  Check out the [asdf](https://github.com/asdf-vm/asdf) docs for more detail
  * Ubuntu 

## Install
```
asdf plugin-add riak https://github.com/smashedtoatoms/asdf-riak.git
```

## Use

Check [asdf](https://github.com/asdf-vm/asdf) readme for instructions on how to install & manage versions of Riak.

When installing Riak using `asdf install`, you can pass custom configure options with the following env vars:

* `RIAK_CONFIGURE_OPTIONS` - use only your configure options
* `RIAK_EXTRA_CONFIGURE_OPTIONS` - append these configure options along with ones that this plugin already uses
