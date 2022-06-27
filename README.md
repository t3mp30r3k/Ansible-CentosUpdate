# Ansible-CentosUpdate
Ansible Automation to update Centos Installed packages

# The playbook does the following:

1. First, it checks if there are any packages to be updated and displays them.
2. Next, it starts the update.
3. After that it installs (if necessary) yum-utils package that provides needs-restarting command which tells us if the system reboot is required after the update.
4. Then it reboots host if necessary and wait for it to come back online.
5. At the end it displays a message with number of seconds that it took to reboot.
