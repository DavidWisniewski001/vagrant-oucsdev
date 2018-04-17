# Linux (Debian) Usage Issues & Fixes

Vagrant in the apt library is not up to date
  -To fix this issue install directly from Hashi corp.
  -Install from <https://www.vagrantup.com/downloads.html>

## Installing Virtual box

The virtual box in the apt library is up to date and runs with the latest version of vagrant to install do the following:

  ```bash
  sudo apt-get update
  sudo apt-get upgrade
  # Ensures that all of the packages are up to date
  sudo apt-get install virtualbox
  # This installs VirtualBox
  ```

## Installing Docker

To run the Docker File you will need to install Docker on your hoat machine to install do the following:

  ```bash
  sudo apt-get update
  sudo apt-get upgrade
  # Makes sure everything is up to date
  sudo apt-get install docker
  ```

If this does not work then Docker provides excellent documentation here <https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce-1>

## Setting permissions

In  Linux you have to give yourself permission to use things like docker and virtualbox

  ```bash
  cat /etc/group .
  # First check are you part of the virtualbox group
  # If not add your name to the group by opening the file in an editor of your choice
  nano /etc/group
  ```
