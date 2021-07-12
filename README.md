<img src="https://github.com/vinceliuice/Sierra-gtk-theme/blob/imgs/logo.png" alt="Logo" align="right" /> NordSur Gtk Theme
======
## Fork to make theme colours easier to hack.
NordSur is a MacOS Big Sur like theme for GTK 3, GTK 2 and Gnome-Shell which supports GTK 3 and GTK 2 based desktop environments like Gnome, Pantheon, XFCE, Mate, etc.
Based on WhiteSur by [Vince Liuice](https://github.com/vinceliuice)

NordSur is currently far from complete. I haven't finished applying the palette to all the themes of the original WhiteSur. It is currently only tested for GTK3/GNOME. Pull requests are welcome.

## Requirements
### GTK2 Murrine engine requirements.

- gtk-murrine-engine  `Fedora/RedHat`
- gtk2-engines-murrine  `Ubuntu/Mint/Debian`
- gtk-engine-murrine  `Arch/Manjaro`

### GTK2 pixbuf engine requirements.

- gtk2-engines  `Fedora/RedHat`
- gtk2-engines-pixbuf  `Ubuntu/Mint/Debian`
- gtk-engines  `Arch/Manjaro`

### Installed Dependency requirements.

- sassc
- optipng
- inkscape
- dialog
- libglib2.0-dev-bin  `ubuntu 20.04`
- libglib2.0-dev  `ubuntu 18.04` `debian 10.03` `linux mint 19`
- libxml2-utils  `ubuntu 18.04` `debian 10.03` `linux mint 19`
- glib2-devel  `Fedora` `Redhat`

## Installation

### From source

After all dependencies are installed, you can run:
```bash
./install.sh
```
#### Install tips

Usage:  `./install.sh`  **[OPTIONS...]**

|  OPTIONS:           | |
|:--------------------|:-------------|
|-d, --dest           | Specify theme destination directory (Default: $HOME/.themes)|
|-n, --name           | Specify theme name (Default: NordSur)|
|-c, --color          | Specify theme color variant(s) **[light/dark]** (Default: All variants)|
|-o, --opacity        | Specify theme opacity variant(s) **[standard/solid]** (Default: All variants)|
|-a, --alt            | Specify titlebutton variant(s) **[standard/alt]** (Default: All variants)|
|-t, --theme          | Change the theme color **[default/blue/purple/pink/red/orange/yellow/green/grey]** (Default: MacOS blue)|
|-p, --panel          | Change the panel opacty **[default/25/35/45/55/65/75/85]** (Default: 16)|
|-s, --size           | Change the nautilus sidebar width size **[default/220/240/260/280]** (Default: 200px)|
|-i, --icon           | Activities icon variant(s) **[standard/normal/gnome/ubuntu/arch/manjaro/fedora/debian/void]** (Default: standard variant)|
|-g, --gdm            | Install GDM theme, you should run this with sudo!|
|-r, --remove         | Remove theme, this will remove all installed themes!|
|-dialog, --dialog    | Run terminal dialog, this will Run terminal dialog to install themes!|
|-h, --help           | Show this help|

### <p align="center" > 1. Change theme accent color </p>
If you want to change theme accent! (Default color is default MacOS color)
then you can run:
```bash
./install.sh -t green  # Install green accent color version
```
![1](pictures/install-tip-01.png)

### <p align="center" > 2. Install GDM theme </p>
If you want to install GDM theme!
then you can run:
```bash
sudo ./install.sh -g      # install default dark version

sudo ./install.sh -g -c light     # install light version

sudo ./install.sh -g -r     # remove installed GDM theme
```
![2](pictures/install-tip-02.png)

### <p align="center" > 3. Change nautilus sidebar width size </p>
If you want to change nautilus sidebar width size! (Default size is 200px)
(Nautilus cannot change the structure of the sidebar, so I added a picture as a background to achieve the effect of bigsur)
then you can run:
```bash
./install.sh -s 260    # Install 260px width version
```
![3](pictures/install-tip-03.png)

### <p align="center" > 4. Change gnome-shell activities icon </p>
If you want to change gnome-shell activities icon! (Default icon is Apple)
then you can run: (For example: Install Manjaro icon)
```bash
./install.sh -i manjaro
```
![4](pictures/install-tip-04.png)

### On Snapcraft

<a href="https://snapcraft.io/whitesur-gtk-theme">
<img alt="Get it from the Snap Store" src="https://snapcraft.io/static/images/badges/en/snap-store-black.svg" />
</a>

You can install the theme from the Snap Store, or by running:

```bash
sudo snap install whitesur-gtk-theme
```
To connect the theme to an app, run:
```bash
sudo snap connect [other snap]:gtk-3-themes whitesur-gtk-theme:gtk-3-themes
```
```bash
sudo snap connect [other snap]:icon-themes whitesur-gtk-theme:icon-themes
```
To connect the theme to all apps which have available plugs to gtk-common-themes, you can run:
```bash
for i in $(snap connections | grep gtk-common-themes:gtk-3-themes | awk '{print $2}'); do sudo snap connect $i whitesur-gtk-theme:gtk-3-themes; done
```

### Suggested themes
|  Suggested themes   | Links | Preview |
|:--------------------|:-------------|:-------------|
| Firefox theme       | [NordSur firefox theme](src/other/firefox)| ![firefox](src/other/firefox/preview.png) |
| Dash to Dock theme  | [NordSur dash-to-dock theme](src/other/dash-to-dock)|  |

## Theme Preview
![gtk](pictures/preview-gtk.png)
