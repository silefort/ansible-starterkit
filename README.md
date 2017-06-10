# Ansible Starter Kit

## Prepare Starter-Kit
* Fill the `hosts` file with you groups and hosts.
* Modify the `ssh.cfg` config file to fit your needs.
* Add you 'deploy' ssh key to keys directory
* Operate from the project root so that `ansible.cfg` and `ssh.cfg` are 
taken into account by all ansible commands.
* Run `ansible all -m ping`: if you get `pong` response from all hosts, you are
ready to operate.

## Bootstrap a new server

* Fill the `hosts` file 'newservers' group with your new server infos
* Run the bootstrap playbook

    ANSIBLE_HOST_KEY_CHECKING=false; ansible-playbook -i hosts playbooks/bootstrap.yml --sudo --ask-pass

## References

* Run `ansible-galaxy install -fr ansible-requirements.yml` to install additional roles.

Here are some project that will give you examples of advanced usages of Ansible:

* [DebOps project](https://github.com/debops)
* [Galaxie project](https://github.com/Tuuux/galaxie)

Some slidedecks to enlight you:

* [FR - Ansible hors des sentiers battus](https://speakerdeck.com/aurelienmaury/ansible-hors-des-sentiers-battus)
