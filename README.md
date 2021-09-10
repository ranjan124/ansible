# ansible
Ansibel commands

ll
ssh -v
openssh -v
ip a
sudo apt autoremove ifconfig
history
ssh worker1@192.168.99.111
ssh worker2@192.168.99.112
ls -la .ssh
ssh-keygen -t ed25519 -C "Default Master"
ls -la .ssh
cat .ssh/id_ed25519.pub
cat .ssh/id_ed25519
ssh-copy-id -i ~/.ssh/id_ed25519.pub worker1@192.168.99.111
ssh-copy-id -i ~/.ssh/id_ed25519.pub worker2@192.168.99.112
ssh 192.168.99.111
ssh worker1@192.168.99.111
ssh-keygen -t ed25519 -C "Ansible"
ls -la .ssh
ssh-copy-id -i ~/.ssh/ansible.pub worker1@192.168.99.111
ssh-copy-id -i ~/.ssh/ansible.pub worker2@192.168.99.112
ssh worker1@192.168.99.111
ssh -i ~/.ssh/ansible worker1@192.168.99.111
history
alias ssha='eval $(ssh-agent) && ssh-add'
ssha
nano .bashrc
sudo nano .bashrc
alias ssha
ssha


sudo apt update ansible -y
ansible all --key-file ~/.ssh/ansible -i inventory -m ping
ansible all --list-hosts
ansible all -m gather_facts
ansible all -m gather_facts --limit 192.168.99.111
ansible all -m apt -a update_cache=true --become --ask-become-pass
ansible all -m apt -a name=vim-nox --become --ask-become-pass
ansible all -m apt -a name=tmux --become --ask-become-pass

# ansible play book
ansible-playbook --ask-become-pass provision.yml





