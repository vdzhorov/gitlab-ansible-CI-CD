# gitlab-ansible-CI-CD

A prototype setup for using Gitlab pipelines along with Ansible and ansistrano.deploy role.

## Requirements

python >= 2.7
ansible >= 2.9

## Prerequisites

* Adjust inventories accordingly in `ansible-setup/inventories` and `project/ansible/inventories`.
* Adjust group_vars accordingly in `ansible-setup/inventories/group_vars` and `project/ansible/inventories/group_vars`.

## Description

This project is separated into 2 parts:

* gitlab/ansible-setup - This is where you should start when setting up your GitLab and GitLab runners.
..* Start by `cd gitlab/ansible-setup` and running `ansible-playbook playbooks/gitlab.yml`. After succesfull installation of GitLab, get a token ID for registering gitlab-runners. Read more about it here: https://docs.gitlab.com/runner/register/. After that, run `ansible-playbook playbooks/gitlab-runners.yml` in order to setup your GitLab runners.
* gitlab/project - This contains a dummy Wordpress installation, .gitlab-ci.yml and ansible automation. These are the files which should be uploaded into a new new repository inside the newly installed GitLab.

### License

MIT

### Author Information

* Valentin Dzhorov
