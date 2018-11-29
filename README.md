# gitlab-ce_ubuntu-16.04
ansible playbook install gitlab-ce_ubuntu 16.04
Installs GitLab, a Ruby-based front-end to Git, on Ubuntu 16.04  linux system.

Master server. - Deploy your Linux system. Install ssh package, install Ansible package (version not lower than 2.5). Recommended - Ubuntu 18.04 + Ansible 2.7.2

The Managed server must have the following version of Linux - Ubuntu 16.04 + installed sshd package.

On the Master server -

1) Create user l: alexandrk
2) Copy the key files (id_rsa.pub and id_rsa) and the inventory file (hosts) that were emailed to you (22.11) in the following directories -

keys (id_rsa.pub id_rsa) - /home/alexandrk/.ssh/
inventory (hosts) - /etc/ansible/

The inventory key check in the ansible.cfg file should have the following value: /etc/anslibe/hosts (the configuration file for the test with version 2.7.2 is in the repository)

3) Copy the playbook8.yml file locally to the computer in the /home/Alexandrk/ ansible directory and run the following command from this directory - ansible-playbook ./playbook8.yml
4) The script has 8 tasks: check the availability of the managed server to directly install the necessary gitlab-ce package, the tasks will be executed sequentially with the output of the information report. For a more detailed report, you should run with the -vvv options.
