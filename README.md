# vm-setup

Initial Debian system setup

This should help you set up cloned VM system with a new host name.

Get this script from the primary non-root user account as follows.

```
$ wget https://github.com/osamuaoki/vm-setup/raw/main/vm-setup
$ chmod 755 vm-setup
```
or

```
$ scp ./vm-setup <hostname>.local:vm-setup
```

Then run this command from the primary non-root user of VM system to set up
system.

If you want to call this VM as ws01

```
$ ./vm-setup ws01
```

If you want to call this VM as ws99 and want to install full GNOME

```
$ ./vm-setup ws99 task-gnome-desktop
```

After this, you want to set up easy SSH path using the host name of VM without
".local" as follows:

```
$ ./vm-setup-ssh <VM_hostname>
```

