# Vagrant Base Boxes

Start by cloning this Git repository. Prerequisites therefore include Git and,
of course, the normal suite of essential build tools for Ruby.
[RVM](https://rvm.io/) is an excellent way to install Ruby.

## Mac OS X

[JewelryBox](http://unfiniti.com/software/mac/jewelrybox) is a useful front-end
to RVM; Macs will need to install a Ruby-friendly compiler, e.g. using
[Homebrew](http://mxcl.github.com/homebrew/).

	git clone git://github.com/royratcliffe/VagrantBaseBoxes.git

You may need to prefix this with `xcrun` in order to pick up the
Xcode-bundled version of `git`.

## Usage

Run Bundler to set up the necessary Ruby gems. Then build, validate and finally
export the Vagrant base box.

	bundle
	vagrant basebox build ubuntu-12.04.1-server-amd64-ruby193
	vagrant basebox validate ubuntu-12.04.1-server-amd64-ruby193
	vagrant basebox export ubuntu-12.04.1-server-amd64-ruby193 --force

## Issues

Tested successfully with VirtualBox version 4.2.4.
