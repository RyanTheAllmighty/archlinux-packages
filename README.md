# archlinux-packages

Repository containing all of my arch linux packages.

## Usage

This repository is controlled all through the `aur` script.

To get started run:

```shell
./aur setup_hooks
```

This will setup the git hooks which will auto build the `.SRCINFO` file before committing so it can never be forgotten.

Next you can import packages already existing in AUR:

```shell
./aur import $package
```

If you want to add a new package, run:

```shell
./aur add $package
```

To pull changes to a package (such as if there are more than 1 person maintaining the package), run:

```shell
./aur pull $package
```

To push up the changes to a package, run:

```shell
./aur push $package
```

## Packages

### hyper-appimage

Arch package for hyper based on the AppImage.

Based on the existing [upwork-appimage](https://aur.archlinux.org/packages/upwork-appimage/).

#### Why?

The `hyper` package from AUR installs NPM, Yarn, NodeJS and Electron just to install, which is not
ideal for me as I want to control my own versions of those softwares and not have one package
pollute that.

#### How does it work?

This works by downloading the AppImage distribution for Hyper and then extracting the `app/`
directory out of that (which contains fully working binary).

This means we don't need to compile the application and can just use it out of the AppImage.

This may not be as intended, but sure works a treat.

### hyper-bin

Arch package for hyper installed by the deb binary.

#### Why?

The `hyper` package from AUR installs NPM, Yarn, NodeJS and Electron just to install, which is not
ideal for me as I want to control my own versions of those softwares and not have one package
pollute that.

### luna-bin

Alternative to [luna](https://aur.archlinux.org/packages/luna/) package with dependencies correct.

At the time of creation, the luna package had too many dependencies.

### nodejs-fake

Creates a fake package to install which provides (and conflicts with) `node` and `nvm` so that people using `nvm` do
not have to install a global `node` or `nvm` when installing packages that require it, such as `yarn`.

### opendesktop-app-appimage

This is the opendesktop-app built from the official AppImage file.
