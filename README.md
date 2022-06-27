# Ansible-CentosUpdate
Ansible Automation to update Centos Installed packages

# What is this ?
On the web you can find many tips about how to update CentOS/RHEL linux systems. Some of them are quite old and do not leverage new features available in recent Ansible versions, other has some issues or do not provide a nice way to display what’s going on.

Recently I’ve spent some time tuning ansible playbook to develop a nice way to update my RedHat family systems.

# The playbook does the following:
1. First, it checks if there are any packages to be updated and displays them.
2. Next, it starts the update.
3. After that it installs (if necessary) yum-utils package that provides needs-restarting command which tells us if the system reboot is required after the update.
4. Then it reboots host if necessary and wait for it to come back online.
5. At the end it displays a message with number of seconds that it took to reboot.

# How to use ?
first, you need to edit hosts file, that compatible with your existing infrastructure

next run this script with ansible.

ansible-playbook -i hosts Centos-Update.yml
