# Nginx webserver with Passenger module for Archlinux

## About

This is custom PKGBUILD for Nginx which adds Phusion Passenger support.

## Instalation

In order to build this package you need to have _passenger_ gem installed on your system:

    gem install passenger

Now make sure _passenger-config_ script is available in your path:

    passenger-config --root

This should print path to passenger installation directory. Use it later as a path given to _passenger\_root_ option in Nginx's config.

Now you can build the package:

    cd nginx-passenger
    makepkg
    sudo pacman -Su nginx-passenger-....pkg.tar.xz

