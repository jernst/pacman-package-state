pacman-package-state
====================

A test / demonstration setup for the lifecycle of a pacman
([Arch Linux](https://archlinux.org/), [UBOS](https://ubos.net/))
package.

Ever wanted to know just what happens when exactly when a pacman
package is installed, removed or upgraded? Test with this.

This is how it works:

1. Clone this repo
1. `cd pacman-package-state-v1`. Then `makepkg`. This builds a
   an example package in version 1.
1. `pacman -U pacman-package-state-1...pkg...` to see what happens
   when you install it. You can see what happens because everything
   that can be scripted has been scripted and tells you, on the console,
   what is being executed. You can also remove it, install it again,
   or play with different pacman options and see what happens.
1. Then, instead of incrementing the `pkgver` inside the `PKGBUILD`,
   go to `../pacman-package-state-v2` and `makepkg` that package. It
   simulates being version 2 of the same package, but its trace messages
   are different, so you can easily tell whether the version 2 or version
   1 of a script are invoked. Try upgrading from version 1, or downgrading
   it back to 1 from 2.

Pull requests appreciated.

