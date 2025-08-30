# Vagrant

This is my Vagrantfile that is based on CentOS 7. I am using this one to learn more about Kubernetes.

## How to use it

Generate a ssh key:
`$ ssh-keygen -t ed25519 -f ~/.ssh/vagrant-test`

Copy the content of `~/.ssh/vagrant-test.pub` to file `authorized_keys`.
