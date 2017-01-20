Vagrant Puppet Boilerplate
==========================

This is a prebuilt Vagrant environment to use with Puppet and individual modules.

## Prepare

Checkout this repository

    git clone https://github.com/lazyfrosch/vagrant-puppet-boilerplate.git

Install required ruby tools:

    bundle install --path vendor/bundle
    
    # or, if you have a Ruby dev environment
    bundle install

And checkout the Puppet modules: (via r10k)

    bundle exec rake deploy

## Recommended plugin

You might need the Vagrant plugin `vagrant-vbguest` to install / update the Virtualbox tools on the VMs.

This will help you install tools before first provisioning, and updating them after a Kernel update.

    vagrant plugin install vagrant-vbguest

## Bring up machines

You can bring up the Vagrant boxes like this:

    vagrant up

Apply changes in the Puppet or hiera data:

    vagrant provision
    vagrant provision <host>

## License

    Copyright (C) 2017 Markus Frosch <markus@lazyfrosch.de>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.
