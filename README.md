# linux_setup_scripts
Various scripts to aid in initial system configuration(s).  These should all end up being rather light, intended for basic setup before handing over to some form of configuration management or other tool that is better suited for long term management of system configuration.

Once visible outside of a working branch, each script will be well commented as for usage.  They should require minimal, if any, interaction to complete the task they are written for.  Below will be a 'best effort' to summarize what each script and associated file(s) are for

## Debian
Scripts listed here are primarily written for Debian.  They may or may not work with (K|X)Ubuntu, Mint, etc unless mentioned that they have been tested to have worked with the downstream distributions.  The primary distributions I personally use is either Debian proper or Linux Mint Debian Edition (LMDE).

1. `bin/deb_base_setup` (Bookworm/LMDE) - This script performs a bare minimum configuration to allow for external bootstrapping
   1. Installs sudo and vim
   2. Sets vim as default editor for visudo
   3. Sets `%sudo` group to `NOPASSWD:ALL`
   4. Adds $user to sudo group
   5. Sets ~/.bashrc (files/.bashrc) for $user to switch PS1 'w' to 'W' (prompt only shows current directory, not full path)
