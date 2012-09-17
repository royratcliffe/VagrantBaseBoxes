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

Run Bundler to set up the necessary Ruby gems. Then build and validate the
Vagrant base box.

	bundle
	vagrant build basebox ubuntu-12.04.1-server-amd64-ruby193
	vagrant validate basebox ubuntu-12.04.1-server-amd64-ruby193

## Issues

Tested successfully with VirtualBox version 4.1.22. At their current versions
however, VirtualBox 4.2.0 and the `virtualbox` gem version 0.9.2 have a
compatibility issue. Roll back to 4.1.22 if you see null pointer errors.
