# Ansible Starter Kit

## Prepare Starter-Kit
* Fill the `inventory/hosts` file with you groups and hosts.
* Modify the `ssh.cfg` config file to fit your needs.
* Add you 'deploy' ssh key to keys directory
* Operate from the project root so that `ansible.cfg` and `ssh.cfg` are 
taken into account by all ansible commands.
* Run `ansible -i inventory/hosts all -m ping`: if you get `pong` response from all hosts, you are
ready to operate.

## Bootstrap a new server
* Fill the newservers group of the `inventory/hosts_to_bootstrap` file
* Run the bootstrap playbook ( you might need to add ask-pass if ssh password is needed)

        ansible-playbook -i inventory/hosts_to_bootstrap playbooks/bootstrap.yml --become

## Run a playbook

        ansible-playbook -i inventory/hosts playbooks/apply_common.yml --ask-become-pass


## References

* Run `ansible-galaxy install -fr ansible-requirements.yml` to install additional roles.

Here are some project that will give you examples of advanced usages of Ansible:

* [DebOps project](https://github.com/debops)
* [Galaxie project](https://github.com/Tuuux/galaxie)

Some slidedecks to enlight you:

* [FR - Ansible hors des sentiers battus](https://speakerdeck.com/aurelienmaury/ansible-hors-des-sentiers-battus)
