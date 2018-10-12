### Ansible Configuration for office RaspberryPi

## Setup instructions:

1. Checkout this codebase: `mkdir -p ~/sites/ && cd ~/sites/ && git clone git@github.com:newscred/rpi-ansible.git` (You can specify your own fork if you don't want to clode newscred fork)
2. Create a new virtualenv: `mkdir -p ~/python-env && virtualenv ~/python-env/office-rpi`
3. Activate virtualenv: `source ~/python-env/office-rpi/bin/activate`
4. `cd ~/sites/rpi-ansible && pip install -r requirements.txt`

## Setup ssh env:
1. Navite to code directory in terminal: `cd ~/sites/rpi-ansible && chmod 600 key-files/id_rsa-rpi`
2. Run this command to add the private key: `eval $(ssh-agent -s) && ssh-add -D && ssh-add key-files/id_rsa-rpi`


## To Run the playbooks:
1. Activate virtualenv and navite to the code directory in terminal. `cd ~/sites/rpi-ansible && pip install -r requirements.txt`
2. Run playbook with: `ansible-playbook -i rpi-hosts playbooks/office-rpi.yaml`


<!-- Test comment -->

