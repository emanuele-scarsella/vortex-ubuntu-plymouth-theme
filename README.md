# Vortex Ubuntu boot splash theme

Animated [Plymouth][plymouth] theme with the Ubuntu logo and a futuristic and
elegant look.

The splash image color wheel spins at varying speeds creating a vortex effect.
During boot, a simple but elegant progress bar is displayed. Simultaneously, the
Ubuntu logo spins in the opposite direction.

Disk encryption password prompt is supported.

## Demo

### Animated demo

![Boot splash animated demo](images/demo.gif)

## Installation

To preview the theme interactively, install the `plymouth-x11` package:

```shell
sudo apt install plymouth-x11
```

To install the theme and set it as the default, navigate to the repository
directory and invoke the `install` script:

```shell
cd path/to/vortex-ubuntu-plymouth-theme
./install
```

`install` invokes `sudo` so you will be asked for your password.

## Preview / Testing

To preview the currently active Plymouth theme, navigate to the repository
directory and invoke the `test-plymouth` script:

```shell
cd path/to/vortex-ubuntu-plymouth-theme

# Show Plymouth preview for 10 seconds
./test-plymouth

# Show Plymouth with mock password and question/answer prompts,
# then show splash for 10 more seconds
./test-plymouth prompt
```

`test-plymouth` invokes `sudo` so you will be asked for your password.

## Removal

To remove the theme, navigate to the repository
directory and invoke the `install` script with the `uninstall` argument:

```shell
cd path/to/vortex-ubuntu-plymouth-theme
./install uninstall
```

`install` invokes `sudo` so you will be asked for your password.

The uninstallation process will prompt you to set a new theme. The default
Plymouth theme in Ubuntu 22.04 is `bgrt`.

# Customization

## Logo spin

To disable the logo image spin, edit `vortex-ubuntu/vortex-ubuntu.script` and
change `logo_spin = -0.009;` to `logo_spin = 0;` near the top.

## Background color

Modify `vortex-ubuntu/bg.png` in the repository, and fill the image with your
desired background color. After modification, reinstall the theme with
`./install` as described above.

## Background image

Replace `vortex-ubuntu/bg.png` in the repository with your desired background
image. Your image must be in PNG format. After modification, reinstall the theme
with `./install` as described above.

## License

This project is licensed under the GNU General Public License (GPL) version 2.
See [`LICENSE`][license] for more information.

## Acknowledgments

* [Inspiration for aesthetic &amp; style][atom]
* [adi1090x/plymouth-themes][adi1090x-plymouth-themes] for prompt examples

## Contributions

* Created by [@emanuele-scarsella](https://github.com/emanuele-scarsella)
* Password prompt and code improvements by [@smkent](https://github.com/smkent)


[adi1090x-plymouth-themes]: https://github.com/adi1090x/plymouth-themes
[atom]: https://atom.io
[license]: /LICENSE
[plymouth]: https://freedesktop.org/wiki/Software/Plymouth/
