# [seccion 5: Trabajar con ficheros](https://www.udemy.com/course/aprende-linux-desde-cero-hasta-programar-en-shell-script/learn/lecture/13334200#overview)

## [1. Presentación de la sección](https://www.udemy.com/course/aprende-linux-desde-cero-hasta-programar-en-shell-script/learn/lecture/13334200#overview)

## [2. Sistema de ficheros en Linux](https://www.udemy.com/course/aprende-linux-desde-cero-hasta-programar-en-shell-script/learn/lecture/13226334#overview)
- En Unix las particiones y los discos están representados como directorios
- Arbol de directorios
  - ![](https://trello-attachments.s3.amazonaws.com/5da0d7fb764b8b74e4c44bc9/812x479/e4545cc0ecac8c3e1e6a2f12fdac577a/image.png)
- Sistema de ficheros
  - ![](https://trello-attachments.s3.amazonaws.com/5da0d7fb764b8b74e4c44bc9/624x328/5bd645552de9cde0e5507a8ff4b7561a/image.png)
## [3. Comandos pwd y ls](https://www.udemy.com/course/aprende-linux-desde-cero-hasta-programar-en-shell-script/learn/lecture/13226336#overview)
- **cmd**: **`pdw y ls`**
## [4. Comando cd](https://www.udemy.com/course/aprende-linux-desde-cero-hasta-programar-en-shell-script/learn/lecture/13226338#overview)
- **cd (a secas)** te lleva a tu home
## [5. Practicas comando cd](https://www.udemy.com/course/aprende-linux-desde-cero-hasta-programar-en-shell-script/learn/lecture/13238272#overview)
- [práctica pdf comando cd](https://a2.udemycdn.com/2019-02-15_13-16-25-7f9c5aef2b39498d052584b5a32057fe/original.pdf?nva=20191012112205&download=True&filename=cd.pdf&token=0c77be799fa8ea0f9d950)
```js
//cd /usr/lib
(uiserver):/usr/lib$ ls
GraphicsMagick-1.3.20  gnupg                           libgs.so.9            libnetpbm.so.10            mc          python3.4
X11                    gnupg2                          libgs.so.9.26         libnetpbm.so.10.0          mime        rssh
apache                 gold-ld                         libgsasl.so.7         libopcodes-2.25-system.so  openssh     ruby
apt                    ispell                          libgsasl.so.7.9.6     librrd.so.4                os-release  sasl2
aspell                 ldscripts                       libisc.so.95          librrd.so.4.2.1            perl5       sendmail
browscap.ini           libGraphicsMagick.so.3          libisc.so.95.5.0      librrd_th.so.4             php4.4      sftp-server
cbi                    libGraphicsMagick.so.3.12.0     libisccc.so.90        librrd_th.so.4.2.1         php5.2      ssl
ccron                  libGraphicsMagickWand.so.2      libisccc.so.90.0.6    libsqlite.so.0             php5.4      susshi
cgi-bin                libGraphicsMagickWand.so.2.7.0  libisccfg.so.90       libsqlite.so.0.8.6         php5.5      tar
compat-ld              libbfd-2.25-system.so           libisccfg.so.90.1.0   libtidy-0.99.so.0          php6        tc
coreutils              libbind9.so.90                  libjbig2dec.so.0      libtidy-0.99.so.0.0.0      php7.1      tmpfiles.d
dbus-1.0               libbind9.so.90.0.9              libjbig2dec.so.0.0.0  libtidy.so                 php7.3      ui-infong-disable-utils
dpkg                   libc-client.so.2007e            liblwres.so.90        libxapian.so.22            pkgconfig   valgrind
emacsen-common         libc-client.so.2007e.0          liblwres.so.90.0.7    libxapian.so.22.6.6        python2.6   x86_64-linux-gnu
gcc                    libdns.so.100                   libmcrypt.so.4        locale                     python2.7
git-core               libdns.so.100.2.2               libmcrypt.so.4.4.8    man-db                     python3

vagrant@homestead:/usr/lib$ ls
accountsservice  dconf            gnupg            language-selector       libmcrypt.so.4.4.8   lxd                  os-prober    rsyslog              tar
apt              dkms             gnupg2           libann.so.0             libnetpbm.so.10      man-db               os-probes    sasl2                tasksel
aspell           dpkg             gold-ld          libann.so.0.0.0         libnetpbm.so.10.0    mime                 os-release   sendmail             tc
at-spi2-core     dracut           groff            libc-client.so.2007e    libvgauth.so.0       modules-load.d       php          sftp-server          tmpfiles.d
avahi            eject            grub             libc-client.so.2007e.0  libvgauth.so.0.0.0   mysql                pm-utils     snapd                ubuntu-release-upgrader
bfd-plugins      emacsen-common   grub-legacy      libDeployPkg.so.0       libvmtools.so.0      networkd-dispatcher  policykit-1  software-properties  update-notifier
binfmt.d         environment.d    heroku           libDeployPkg.so.0.0.0   libvmtools.so.0.0.0  nginx                postfix      ssl                  valgrind
binfmt-support   file             initcpio         libguestlib.so.0        linux                node_modules         postgresql   sudo                 X11
byobu            gcc              initramfs-tools  libguestlib.so.0.0.0    linux-boot-probes    notification-daemon  python2.7    sysctl.d             x86_64-linux-gnu
clang            gettext          ispell           libhgfs.so.0            llvm-6.0             ntp                  python3      sysstat
compat-ld        git-core         kernel           libhgfs.so.0.0.0        locale               openssh              python3.6    systemd
dbus-1.0         glib-networking  klibc            libmcrypt.so.4          lxcfs                open-vm-tools        python3.7    sysusers.d

vagrant@homestead:/var/log$ ls -lat
total 3504
-rw-r-----   1 syslog    adm                1496 Oct 12 06:55 syslog
-rw-r-----   1 syslog    adm              489322 Oct 12 06:55 auth.log
drwxrwxr-x  16 root      syslog             4096 Oct 12 06:25 .
drwxr-xr-x   2 root      adm                4096 Oct 12 06:25 nginx
drwxr-x---   2 mysql     adm                4096 Oct 12 06:25 mysql
-rw-r-----   1 syslog    adm             2026113 Oct 12 06:25 syslog.1
-rw-rw-r--   1 root      utmp             292292 Oct 11 19:15 lastlog
-rw-rw-r--   1 root      utmp              46080 Oct 11 19:15 wtmp
-rw-r--r--   1 root      root                 61 Oct 11 19:10 vboxadd-setup.log
-rw-r-----   1 syslog    adm              797358 Oct 11 19:10 kern.log
-rw-------   1 root      root               5901 Oct 11 19:10 php7.3-fpm.log
-rw-r-----   1 syslog    adm                3345 Oct 11 19:10 mail.log
-rw-------   1 root      root               5897 Oct 11 19:10 php7.1-fpm.log
-rw-------   1 root      root               5901 Oct 11 19:10 php7.0-fpm.log
-rw-------   1 root      root               5902 Oct 11 19:10 php7.2-fpm.log
-rw-------   1 root      root               5898 Oct 11 19:10 php5.6-fpm.log
-rw-r--r--   1 root      root                 61 Oct  7 18:37 vboxadd-setup.log.1
-rw-r--r--   1 root      root                 61 Oct  6 13:25 vboxadd-setup.log.2
-rw-r--r--   1 root      root                 61 Oct  6 13:16 vboxadd-setup.log.3
-rw-r--r--   1 root      root                 61 Oct  6 09:20 vboxadd-setup.log.4
-rw-rw----   1 root      utmp               4224 Oct  5 16:23 btmp
drwxr-xr-x   2 root      root               4096 Sep 15 13:35 supervisor
drwxr-x---   2 root      adm                4096 Sep 15 13:35 unattended-upgrades
drwxrwxr-t   2 root      postgres           4096 Sep 15 13:35 postgresql
drwxr-sr-x+  4 root      systemd-journal    4096 Sep 15 13:34 journal
drwxr-x---   2 redis     redis              4096 Aug 31 11:55 redis
drwxr-xr-x  14 root      root               4096 Aug 31 11:55 ..
drwxr-xr-x   2 root      root               4096 Aug 31 11:55 apt
drwxr-xr-x   2 landscape landscape          4096 Aug 31 11:55 landscape
-rw-------   1 root      root              64064 Aug 31 11:54 tallylog
-rw-r--r--   1 root      root              32032 Aug 31 11:54 faillog
drwxr-xr-x   2 root      root               4096 Jun 19 16:49 dist-upgrade
drwxr-x---   2 root      adm                4096 May 23 12:06 samba
drwxr-xr-x   2 root      root               4096 Nov 23  2018 lxd
drwxr-xr-x   2 ntp       ntp                4096 Jul  6  2018 ntpstats
drwxr-xr-x   2 root      root               4096 Dec 23  2017 sysstat

(uiserver):/var/log$ ls -lat
total 4
drwxr-xr-x  2 mail mail   60 Oct 12 00:01 nemesis
drwx------  2 root root   60 Oct  1 12:48 oneclick
drwxr-xr-x  4 root root   80 Oct  1 12:48 .
drwxr-xr-x 12 root root 4096 Apr  8  2016 ..

//ls -lt
//order by mdate desc, cdate desc

//cd .
//moverse al directorio actual, es quedarse en el mismo :)
```

## 6.
- 
```js

```
## 7.
- 
```js
```
## 8.
- 
```js
```
## 9.
- 
```js
```
## 10.
- 
```js
```
## 11.
- 
```js
```
## 12.
- 
```js
```
## 13.
- 
```js
```
## 14.
- 
```js
```
## 15.
- 
```js
```
## 16.
- 
```js
```
## 17.
- 
```js
```
## 18.
- 
```js
```
## 19.
- 
```js
```
## 20.
- 
```js
```
## 21.
- 
```js
```
## 22.
- 
```js
```

