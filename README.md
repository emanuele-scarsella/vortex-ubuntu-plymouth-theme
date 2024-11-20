<h1 align="center">Vortex Ubuntu boot splash theme</h1>
<p align="center">
	<img src=images/vortex-ubuntu.png? >
</p>
<p align="center">
	<a href="https://www.gnome-look.org/p/1499429"><img src="https://img.shields.io/badge/Rank%20on-Gnome--look.org-%207ca5df%20?logo=gnome&logoColor=lightgrey&labelColor=303030&color=%237fa5db" ></a>
</p>

Animated [Plymouth][plymouth] theme with the Ubuntu logo and a futuristic and
elegant look.

The splash image color wheel spins at varying speeds creating a vortex effect.
During boot, a simple but elegant progress bar is displayed. Simultaneously, the
Ubuntu logo spins in the opposite direction.

Disk encryption password prompt is supported.

## Examples

|                                                      |                                                      |
| :--------------------------------------------------: | :--------------------------------------------------: |
|                        Bootup                        |                       Shutdown                       |
|         ![Boot splash animated demo][bootup]         |      ![Shutdown splash animated demo][shutdown]      |
|                       Password                       |                       Question                       |
| ![Boot splash with password animated demo][password] | ![Boot splash with question animated demo][question] |

## :gear: Installation

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

## :paintbrush: Preview / Testing

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

## :no_entry_sign: Removal

To remove the theme, navigate to the repository
directory and invoke the `install` script with the `uninstall` argument:

```shell
cd path/to/vortex-ubuntu-plymouth-theme
./install uninstall
```

`install` invokes `sudo` so you will be asked for your password.

The uninstallation process will prompt you to set a new theme. The default
Plymouth theme in Ubuntu 22.04 is `bgrt`.

# :wrench: Customization

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

# :copyright: Acknowledgments

-   [Inspiration for aesthetic &amp; style][atom]
-   [adi1090x/plymouth-themes][adi1090x-plymouth-themes] for prompt examples

# :handshake: Contributions

-   Created by [@emanuele-scarsella](https://github.com/emanuele-scarsella)
-   Password prompt and code improvements by [@smkent](https://github.com/smkent)

[adi1090x-plymouth-themes]: https://github.com/adi1090x/plymouth-themes
[atom]: https://atom.io
[license]: /LICENSE
[plymouth]: https://freedesktop.org/wiki/Software/Plymouth/
[bootup]: images/bootup.gif
[shutdown]: images/shutdown.gif
[password]: images/password.gif
[question]: images/question.gif
