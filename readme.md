# Awesomebox
This is my chef+vagrant setup for node.js development. It's currently a
work in progress but out of the box it'll give you

* mongodb 2.0.2
* redis 2.4.8
* node.js 0.6.8
* coffee-script
* less
* nginx

## Running it
Requires that you have a vagrant box named ubuntu-1110-server-amd64 installed.

```bash
git clone git@github.com:inf0rmer/nodejs-vagrant.git
cd nodejs-vagrant
git submodule init && git submodule update
vagrant up
```

## Soon!

* Companion node.js app that uses capistrano to deploy
