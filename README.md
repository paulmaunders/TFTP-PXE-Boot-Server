TFTP-PXE-Boot-Server
====================

This project contains the basic files and folder setup needed for a TFTP PXELINUX server.

To use it, you need to

1. Set up a TFTP server
2. Checkout this project on the TFTP server, and ensure the tftp root points at this project folder.
3. Setup your DHCP to point at the TFTP server (using DHCP option 66 "next-server" if located on a different IP to the DHCP server)
4. Setup your DHCP to offer the PXELINUX.0 as the boot filename (DHCP option 67).
