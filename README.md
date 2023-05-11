# ansible_nginx_demo

# How To Write Ansible Playbooks

Edit the included `inventory` file to include your remote node(s):

```command
nano inventory
```

```ini

[dev]
192.168.0.1

[all:vars]
ansible_python_interpreter=/usr/bin/python3
```

Save and close the file. 

You can run the playbooks with:

```command
ansible-playbook -i inventory playbook-01.yml -u REMOTE_USER
```

If the playbook has a `become` directive it means you'll most probably will have to provide the `sudo` password for your connecting user. You dan do that by including the `-K` parameter:

```command
ansible-playbook -i inventory playbook-01.yml -u REMOTE_USER -K
```

For more details, please refer to the tutorial series: [How To Write Ansible Playbooks](https://www.digitalocean.com/community/tutorial_series/how-to-write-ansible-playbooks).
