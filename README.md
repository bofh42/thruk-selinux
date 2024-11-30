# thruk-selinux
SELinux policies for Thruk.

# Description
SELinux policies written for Thruk.  
This is far from beeing perfect, but i want to try and run Thruk in enforcing mode on RHEL 9.  
The policies are collected from audit2allow.

## Dependencies
selinux-policy-devel

## Installation
* clone the repository
* `make -f /usr/share/selinux/devel/Makefile`
* `semodule -i thruk_42.pp`
* `restorecon restorecon -Rv /etc/thruk /var/log/thruk /var/cache/thruk /var/lib/thruk`
* `setsebool -P httpd_can_network_connect 1`
