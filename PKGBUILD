# Maintainer: justbrowsing <developer4linux+aur@gmail.com>
pkgname=jb-config
pkgver=1.0
pkgrel=1
pkgdesc="A gtkdialog GUI and backend to manage settings for JustBrowsing that allows loading/saving from a config file"
arch=('any')
url="https://github.com/justbrowsing/jb-config"
license=('GPL3')
depends=('justbrowsing-systemd' 'gtkdialog-svn' 'systemd' 'diffutils' 'xorg-xrandr' 'cups')
optdepends=('justbrowsing-adeskbar: Panel with systray that is reloaded' 
			'jbxkb: Switch between keymaps'
			'network-manager-applet-gtk2: Connect to wired/wireless networks' 
			'pnmixer: Adjust volume' 
			'nitrogen: Update background/wallpaper')
groups=("justbrowsing")
source=("https://github.com/justbrowsing/${pkgname}/archive/master.zip")
install="jbconfig.install"
md5sums=('SKIP')
 
package() {
  cd "$srcdir/${pkgname}-master"
  mkdir -p "$pkgdir/usr/local/sbin" "$pkgdir/usr/bin"

  # Browser Wrappers
  install -Dm555 firefox "$pkgdir/usr/local/sbin/firefox"
  install -Dm555 google-chrome "$pkgdir/usr/local/sbin/google-chrome"
  install -Dm555 x-www-browser "$pkgdir/usr/bin/x-www-browser"
  install -Dm555 launch-webapp "$pkgdir/usr/bin/launch-webapp"

  # GUI Executables
  install -Dm555 jb-config "$pkgdir/usr/bin/jb-config"
  install -Dm555 savejb-config "$pkgdir/usr/bin/savejb-config"
  install -Dm555 loadjb-config "$pkgdir/usr/bin/loadjb-config"
  install -Dm555 loadjb-help "$pkgdir/usr/bin/loadjb-help"
  install -Dm555 loadjb-panel "$pkgdir/usr/bin/loadjb-panel"
  install -Dm555 loadjb-systray "$pkgdir/usr/bin/loadjb-systray"
  install -Dm555 loadjb-toggle "$pkgdir/usr/bin/loadjb-toggle"

  # Back-end Executables
  install -Dm555 setjb-clean "$pkgdir/usr/bin/setjb-clean"
  install -Dm555 setjb-default "$pkgdir/usr/bin/setjb-default"
  install -Dm555 setjb-display "$pkgdir/usr/bin/setjb-display"
  install -Dm555 setjb-gpu "$pkgdir/usr/bin/setjb-gpu"
  install -Dm555 setjb-keymap "$pkgdir/usr/bin/setjb-keymap"
  install -Dm555 setjb-locale "$pkgdir/usr/bin/setjb-locale"
  install -Dm555 setjb-url "$pkgdir/usr/bin/setjb-url"
  install -Dm555 setjb-zone "$pkgdir/usr/bin/setjb-zone"

  # Desktop launcher
  install -Dm644 "jbconfig.png" "$pkgdir/usr/share/pixmaps/jbconfig.png"
  install -Dm644 "jbconfig.desktop" "$pkgdir/usr/share/applications/jbconfig.desktop"
  install -Dm644 LICENSE ${pkgdir}/usr/share/licenses/jb-config/LICENSE
}


