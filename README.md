# vm-setup

Initial Debian system setup

## Phase 1: hostname and basic packages

This should help you set up cloned VM system with a new hostname .

Pull this script from the primary non-root user account on the VM as:

```
user@VM:~$ wget https://github.com/osamuaoki/vm-setup/raw/main/vm-setup
user@VM:~$ chmod 755 vm-setup
```

or push it from the host WS as:

```
user@WS:~$ scp ./vm-setup <VM_hostname>.local:vm-setup
```

Then run this command from the primary non-root user of VM system to set up
system.

If you want to call this VM as ws01

```
user@VM:~$ ./vm-setup ws01
```

If you want to call this VM as ws99 and want to install full GNOME

```
user@VM:~$ ./vm-setup ws99 task-gnome-desktop
```

## Phase 2: SSH keys

After this, you set up easy SSH path between the host WS and the guest VM using
the hostname of VM without ".local" by issuing a command from the host WS as:

```
user@WS:~$ ./vm-setup-ssh <VM_hostname>
```

