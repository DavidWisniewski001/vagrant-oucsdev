# OU Computer Science Development Environment

This is a very basic Vagrant VM which can be used for development.
In theory it should work across Windows, Mac and Linux with one of
the supported hypervisors. Ansible is used to further customise the
VM, but is performed from withinn the VM so Ansible is not necessary
on the host system.

## Requirments

- VirtualBox, VMware, HyperV or Parallels
- Vagrant
  - Install from <https://www.vagrantup.com/downloads.html>
- Git
  - Windows users should install from <https://gitforwindows.org/>

## Getting Started

Windows users should use a git bash shell from the git for windows project.

```bash
git clone https://github.com/robert4man/vagrant-oucsdev.git
cd vagrant-oucsdev
vagrant up
# wait for it...
vagrant ssh
```

Anything placed in the projects folder will be ignored by git and should be
automatically accessible from within the VM under /vagrant/projects. Once you
are done on the vm you can exit and power it off, or optioally destroy it entirely.

```bash
exit
vagrant halt # will power down the vm
vagrant destroy # will completely delete the vm
vagrant up # will re-create the vm, or power it on if still existing
```

All vagrant commands should be performed within the directory with the Vagrantfile.
Any changes made to the VM from within the VM will be persisted with a halt/up but
lost with a destroy. Changes within the project directoy should be sync'd with the
host machine and will persist even when the VM is destroyed.

## Docker image

More or less the same thing can also be done from Docker. The following will
build a re-usable docker image.

```bash
docker build -t oucsdev .
docker run -it oucsdev /bin/bash
```
