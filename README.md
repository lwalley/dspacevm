# DSpace VM

Configuration files for provisioning a virtual machine with DSpace using Vagrant and Chef Solo.

## Rough guide

* Install [VirtualBox](http://virtualbox.org). Add VirtualBox to path e.g.

    export PATH=$PATH:/Applications/VirtualBox.app/Contents/MacOS/

* Install [Vagrant](http://vagrantup.com) from [package](http://downloads.vagrantup.com) as recommended by [Vagrant docs](http://docs.vagrantup.com/v1/docs/getting-started/index.html). Alternatively uncomment Vagrant gem dependency in Gemfile before running bundle install.

* Download/clone [DSpace VM](https://github.com/lwalley/dspacevm)

* Install bundler gem

    $ gem install bundler

* Optionally configure bundler to pass options to chef install

    $ bundle config build.chef --no-ri --no-rdoc

* Install gems

    $ bundle install

* Download cookbooks with librarian-chef

    $ librarian-chef install

* Optionally override cookbook attributes in Vagrantfile.

* Create and provision virtual machine with Vagrant

    $ vagrant up

* SSH to virtual machine

    $ vagrant ssh

* Create dspace adminstrator for logging into the UI:

    $ /dspace/bin/dspace create-administrator


