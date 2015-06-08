This script automate the "Forwarding Incoming Connections" hack in libvirt
( http://wiki.libvirt.org/page/Networking#Forwarding_Incoming_Connections )
with a simple config file :

::

  # vmname      public_ip     pub_port nated_ip       nated_port
    vm-mail     169.254.0.1   25       192.168.122.4  25
    vm-http     169.254.0.2   80       192.168.122.5  80
    vm-mail     169.254.0.1   110      192.168.122.4  110
    vm-mail     169.254.0.1   143      192.168.122.4  143
    vm-http     169.254.0.2   443      192.168.122.5  443
    vm-mail     169.254.0.1   465      192.168.122.4  465
    vm-mail     169.254.0.1   587      192.168.122.4  587
    vm-mail     169.254.0.1   993      192.168.122.4  993
    vm-mail     169.254.0.1   995      192.168.122.4  995

Configure, regenerate with the script, restart libvirtd.

Not tested with IPv6.