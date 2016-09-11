TFTP-PXE-Boot-Server
====================

This project contains the basic files and folder setup needed for a TFTP PXELINUX server.

It currently has support for network (PXE) installing:

* Centos 6.x
* Centos 7.0
* Fedora 24
* Ubuntu 16.04 (Xenial)

To use it, you need to

1. Set up a TFTP server. If you are using a Mac you could use this one - http://ww2.unime.it/flr/tftpserver/
2. Checkout this project code on the TFTP server, and ensure the tftp root points at this project folder.
  ```git clone git@github.com:paulmaunders/TFTP-PXE-Boot-Server.git```
3. Setup your DHCP to point at the TFTP server (using DHCP option 66 "next-server" if located on a different IP to the DHCP server)
4. Setup your DHCP to offer the PXELINUX.0 as the boot filename (DHCP option 67).
5. Edit the pxelinux.cfg/default file to add in your PXE boot options. I've included an example one for CentOS


Further instructions
====================

If you have a Synology NAS then you can follow [these instructions](http://www.pyrosoft.co.uk/blog/2013/01/13/setting-up-a-pxe-boot-server-on-synology-dsm-4-2-beta/) to set up a working PXE boot system:
