# mypc-galaxy

Install Ansible:
```bash
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible git -y
```

Clone the repo:
```bash
git clone https://github.com/ShubhamTatvamasi/mypc-galaxy.git
cd mypc-galaxy
```

Setup My PC:
```bash
# Set this variable if you get locale encoding to be UTF-8 error
export LC_ALL="en_US.UTF-8"

# Install everything
sed -i 's/# //g' setup.yml

ansible-playbook setup.yml -K
```


### SSH Setup

Create SSH directory:
```bash
mkdir ~/.ssh
cd ~/.ssh

chmod 400 ~/.ssh/id_rsa
chmod 400 ~/.ssh/id_ed25519
```


### Setup Git

Update remote origin:
```bash
git remote remove origin
git remote add origin git@github.com:ShubhamTatvamasi/mypc-galaxy.git
```
