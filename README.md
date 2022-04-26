- To Work with Vagrant
    - Install vagrant
    - Install VirtualBox
    - Create/ provision the VM `vagrant up`

- Work with Vagrant VM in VS Code
    - https://medium.com/@lopezgand/connect-visual-studio-code-with-vagrant-in-your-local-machine-24903fb4a9de
        - NOTE1: Change the name of the host from default to the project name
        - NOTE2: VSCode will default to having /home/vagrant as the directory you remote to but you need to replace that with just /vagrant to access the shared folder
    - You must install usefull extensions (even if they are intalled on your local machine) because they must be installed on the VS Code in the VM
        - i.e. the Python extension
    - To run jupyter notebooks in VS code you need to have ipykernel installed in your venv (like in this example)

- Outside of VSCode, you can use terminal as usual after running `vagrant ssh` and cd-ing to /vagrant

- Set Up Git SSH connection in Vagrant VM
    - Added `config.ssh.forward_agent = true` in the Vagrantfile
    - Followed the steps in: https://github.com/jillvillany/python-dev-setup#maclinux-configure-ssh-auth
    - NOTE: when I tested `ssh -T git@github.ibm-Jillian-Villany` it didn't work but `ssh -T git@github.ibm.com` did
    - NOTE2: You should also add your git username and email in the config (so that you can use git in VS Code)
        - git config user.name Jill Villany
        - git config user.email jillian.villany@ibm.com