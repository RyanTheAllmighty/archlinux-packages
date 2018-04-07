# archlinux-packages

Repository containing all of my arch linux packages.

## Packages

### 

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
