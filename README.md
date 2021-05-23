# ubuntu-local-packages

Some third party software packages are available as `.deb`, but are not hosted in any proper, updateable repository. Installing them manually via `dpkg -i` will let it appear in the `Obsolete and Locally Created Packages` category in `aptitude`, and the user needs to keep around the original `.deb` if they like to uninstall and later reinstall the package.

A simple solution to this, is to create a local package repository, add the package thereto and then install it via standard Debian/Ubuntu infrastructure. Packages can be uninstalled and reinstalled, and can't go amiss.

While this is easily possible with the `dpkg-scanpackages` utility, one needs to perform certain configuration steps to set up a local repository on a new machine.

Since I'm tired of re-doing these steps, I have created this repository which itself is packaged as a `.deb` and can be installed easily on new machines.

*Warning: Alpha quality, use at your own risk.*

## Installation

```bash
# TODO
```



## Usage

```bash
cp yourDebFile.deb /opt/packages/deb
update-local-packages
# apt update
# apt install yourDeb
```

## Building

```bash
dpkg-deb --build ubuntu-local-packages_1.0-1
```



## License

MIT

