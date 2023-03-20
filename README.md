# anisble-ee-template-example
This is a repository for Ansible EE template

An example command to use to build an ansible execution environment;

$ ansible-builder build --tag djoo_ee_aws --container-runtime podman -c /home/djoo/AAP21-demo/Exec-Envs/AWS/ -f /home/djoo/AAP21-demo/Exec-Envs/AWS/execution-environment.yml -v3

For MAC, followings need to be done.
* Prereqs
** ansible, ansible-builder & ansible-navigator are installed using brew
** docker desktop is installed

1. Set an env variable to make amd64 a default platform
$ export DOCKER_DEFAULT_PLATFORM=linux/amd64

2. Use below command to make sure that you use docker as a container runtime
$ ansible-builder build --tag djoo_ee_aws --container-runtime docker -c /home/djoo/AAP21-demo/Exec-Envs/AWS/ -f /home/djoo/AAP21-demo/Exec-Envs/AWS/execution-environment.yml -v3
