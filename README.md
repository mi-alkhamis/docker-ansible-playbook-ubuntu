# ansible-docker - Ansible Playbook for Docker

## Overview

If you are looking for a playbook to automate install docker for you, this playbook preapared based on [docker.io](https://docs.docker.com/engine/install/ubuntu/) for ubuntu (or ubuntu based distro only )
**USE on your own risk for non-ubuntu based distro**

## Requirements

- ansible 2.10
- Python 3.8

## How to use 

1. write your `hosts.ini` or `hosts.yaml` file like 

```ini
[all]
VM1 
VM2
```

2. get clone of   [Ansible-docker](https://github.com/mi-alkhamis/docker-ansible.git)
3. run `ansible-playbook  -i hosts.ini -b install-docker.yaml`
4. enjoy it :smile:



## Use it with tags!!!

Some useful tags:

- update_cache :arrow_right: update cache of apt
- all :arrow_right: run whole of script
- install_pre :arrow_right:  install some requirements (based on  [docker.io]())
- add_gpg :arrow_right:  add docker repository gpg key
- add_repo :arrow_right: add docker repository
- install :arrow_right: install docker
- check_ver :arrow_right: check version of docker(if installed)
- check_service :arrow_right: check docker service status

## Examples

-  `ansible-playbook  -i hosts.ini -t all -b install-docker.yaml`
-  `ansible-playbook  -i hosts.ini -t check_service install-docker.yaml`
- `ansible-playbook  -i hosts.ini -t check_ver install-docker.yaml`

# Contribute

All contributions are welcome:

- Read the issues, fork the project and do a Pull Request.
- Request a new topic creating a New issue with the enhancement tag.
- Find any kind of errors in the cheat sheet and create a New issue with the details or fork the project and do a Pull Request.



## License

This project is licensed under the Apache-2.0 License  - see the [LICENSE](https://github.com/mi-alkhamis/docker-ansible/blob/main/LICENSE) file for details.

