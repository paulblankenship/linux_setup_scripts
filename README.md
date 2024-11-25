# linux_setup_scripts
Various scripts to aid in initial system configuration(s).  These should all end up being rather light, intended for basic setup before handing over to some form of configuration management or other tool that is better suited for long term management of system configuration.

Once visible outside of a working branch, each script will be well commented as for usage.  They should require minimal, if any, interaction to complete the task they are written for.  Below will be a 'best effort' to summarize what each script and associated file(s) are for.

## Debian
Scripts listed here are primarily written for Debian.  They may or may not work with (K|X)Ubuntu, Mint, etc unless mentioned that they have been tested to have worked with the downstream distributions.

### bin/deb_base_setup (Bookwork/LMDE)
Performs a bare minimum configuration after install from CD/DVD/USB to allow for basic editing or external bootstrapping.  

This script performs the following actions:

1. Installs sudu and vim
2. Sets VIM for visudo
3. Adds user to sudo group
4. Switches `%sudo` group to `NOPASSWD`
5. Replaces user's `.bashrc` with `files/.bashrc``

Command dump to run from CLI
```
wget https://github.com/paulblankenship/linux_setup_scripts/archive/refs/heads/master.tar.gz
tar xvzf master.tar.gz
cd linux_setup_scripts-master/
su root -c "bin/deb_base_setup <username>"
cd .. && rm -rf linux_setup_scripts-master/
```
