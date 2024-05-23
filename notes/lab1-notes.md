Exercise 1.1: Configuring the System for sudo

- on linux distributions, we can gran users sudo access by editing the file `/etc/sudoers.d`. Setting something like:
`USER_NAME ALL=(ALL) ALL` will give the USER_NAME user all sudo access.

- there are other methods to configure sudo bu this method is well documented

- even though we configured our system for sudo with the above, we would still need to enter the full path from our root user when trying to access certain system utilities. To get around this, we can update the PATH to the system utilities in our `.bashrc`. Adding the following will reconfigure our path so we do not have to deal with this:

`PATH=$PATH:/usr/sbin:/sbin`
