libgnomecanvas Download And Installation
========================================

I am making available i386 and amd64 Debian archives of libgnomecanvas with my
fix for the serious paint memory leak as the bug has been ignored [upstream](https://bugzilla.gnome.org/attachment.cgi) and in [Debian](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=753621) -
the extremely trivial patch is debian/patches/omega-paint-memoryleak.diff

Download all packages in your architecture folder - click on the filename, then
click View Raw. **DO NOT** right click on a link, as this will save the web page,
not the file.

These archives are signed by my GPG key - to verify:

1. Install dpkg-sig: sudo aptitude install dpkg-sig gpg
2. Fetch my public key: gpg --keyserver keys.gnupg.net --recv-keys 0xFDC2F38F
3. Confirm that the fingerprint of the key matches (so that you can trust my key): E760 95EC DACD 5DEC 7653 A996 17D2 3C7D FDC2 F38F
4. Verify the debian archives: dpkg-sig --verify *.deb

If you haven't imported my key, you'll get this:

===============================

UNKNOWNSIG _gpgbuilder FDC2F38F

===============================

Otherwise:

=======================================================================

GOODSIG _gpgbuilder E76095ECDACD5DEC7653A99617D23C7DFDC2F38F 1407865602

=======================================================================

Once the archives are installed (e.g. with 'sudo dpkg -i *.deb'), you will need
to hold the packages to prevent aptitude/apt immediately reinstalling the normal
versions (see [instructions](http://askubuntu.com/a/18656)).
