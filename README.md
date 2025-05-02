# Basic-Ansible

![image](https://github.com/user-attachments/assets/9b96b1e4-7dce-437c-8833-7e0dfdd2b196)

## 📘 About

This is just me testing **Ansible** in a simple Docker environment.

I'm learning how to:
- Run Ansible from a container
- Write a basic playbook
- Use localhost as the target

I will create more examples in the future to better understand it.
## 🐳 Setup

I'm using Docker to run Ansible:

```bash
docker run -it --name ansible-test ubuntu
apt update
apt install ansible -y
echo '
- hosts: localhost
  connection: local
  tasks:
    - name: Ping localhost
      ping:' > playbook.yml
ansible-playbook -i localhost, playbook.yml
