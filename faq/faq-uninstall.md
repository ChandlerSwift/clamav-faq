# Uninstalling ClamAV

## If you installed from source

    `./configure`

    `sudo make uninstall`

---

## If you installed from packages

* Debian: 

  `dpkg --remove clamav*`

* Redhat/Fedora: 

  `yum remove clamav*`

* Mandriva: 

  `urpme clamav`

* Gentoo: 

  `emerge -C clamav`

* FreeBSD:

  `pkg delete clamav`

* OpenBSD:

  `pkg_delete clamav`

* NetBSD:

  `pkgin remove clamav`

* Slackware:

  `/etc/rc.d/rc.clamav stop; removepkg clamav`

---

## Caveats

Make sure that you haven’t got old libraries (_libclamav.so_) lying around your filesystem. You can verify it using:

<pre>
    $ ldd `which freshclam`
</pre>

Also make sure there is really only one version of ClamAV installed on your system:

    `$ whereis freshclam`

    `$ whereis clamscan`
