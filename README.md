![Nix|Direnv](./logo.baked.svg)
==========
*reproducible environments to the moon!*

![shield](./shield.baked.svg)</br>
![shield-long](./shield-long.baked.svg)

This project is aimed to popularize and make it easier to use reproducible Nix environments, preferably with direnv.

It provides **(todo)** manuals to link to and clickbait-y shields, so you can guide potential new maintainers through setting up Nix and Direnv more quickly.

There's a short installation guide I've started writing below, but it's WIP.

Ideally there would be an interactive installation script, supporting WSL, MacOS and Linux **(todo)**

-----

## Development

This project uses **direnv** and **Nix** to manage environment.

### Nix
Nix is a clean package manager.</br>
It allows managing system dependencies like compilers and shared libraries in a portable way, without cluttering or breaking your existing system.

You can install Nix on Linux/MacOS/WSL with the following command
```sh
sh <(curl -L https://nixos.org/nix/install) --daemon
```
- *[More installation info](https://nixos.org/guides/install-nix.html)*
- *[Learn more about Nix](https://nixos.org/)*

### Direnv
Direnv is an environment manager.</br>
It runs scripts and loads environment variables from `.envrc` as you switch between folders.</br>
We prefer nix-direnv implementation, as it works faster with Nix.

You can install it with the following command
```sh
nix-env -f '<nixpkgs>' -i nix-direnv
```
If you use bash, zsh or tcsh, append the following to your `~/.profile`
```sh
eval "$(direnv hook $(basename $0))"
```
- [*Installing direnv for other shells (fish/elvish)*](https://direnv.net/docs/hook.html)
- [*Installation options for NixOS and home-manager users*](https://github.com/nix-community/nix-direnv#installation)
- [*Learn more about direnv*](https://direnv.net/)
