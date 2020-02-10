# packer-ansible-example
I recently discovered that the ansible provisioner in packer is "community" supported and not actually maintained by hashicorp despite being built into packer. It's rather broken at the moment and I needed to use ansible from packer, they recommend you use shell provisioners instead.

The issue with using shell provisioners in this situation is I want to run ansible from the packer local machine (docker) against the instance I've spun up with packer as I reboot the machine in a few places due to certain package requirements. They don't provide the IP or ssh key to the shell-local provider so I had to write this dodgy workaround
