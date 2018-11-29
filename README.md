[![Build Status](https://travis-ci.org/unxnn/ansible-rhel7-kernel4.svg?branch=master)](https://travis-ci.org/unxnn/ansible-rhel7-kernel4)

# ansible-rhel7-kernel4

Role for upgrading kernel of RHEL7 to version 4.X

Although some people use the word Linux to represent the operating system as a whole, it is important to note that, strictly speaking, Linux is only the kernel. On the other hand, a distribution is a fully-functional system built on top of the kernel with a wide variety of application tools and libraries.

Sometimes the standard kernel doesn't enough for normal working of your services, for example `overlay` in `Docker`.

> NOTE: If you use OverlayFS, use the overlay2 driver rather than the overlay driver, because it is more efficient in terms of inode utilization. To use the new driver, you need version 4.0 or higher of the Linux kernel.

This role installs the kernel version 4.X from the http://elrepo.org/tiki/kernel-ml repository.

# Dependenices

None.

# Example Playbook

    - hosts: docker
      roles:
        - { role: unxnn.ansible-rhel7-kernel4 }

# License

MIT