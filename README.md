# Use Example
## 1. pull image in Central Server(Grafana,loki,prometheus)
docker pull williamyeh/ansible:alpine3

## 2. git clone repo

## 3. update inventory/hosts.yml

## 4. Generate ssh key
ssh-keygen -t rsa -b 4096

ssh-copy-id root@target_server_ip

   
## 4. Install Python into hosts
docker run --rm -it \
  -v ~/ansible-playbooks:/ansible \
  -v ~/.ssh:/root/.ssh \
  williamyeh/ansible:alpine3 \
  ansible-playbook -i /ansible/inventory/hosts.yml /ansible/install_python.yml


## 5. Ping Test into hosts
docker run --rm -it \
  -v ~/ansible-playbooks:/ansible \
  -v ~/.ssh:/root/.ssh \
  williamyeh/ansible:alpine3 \
  ansible -i /ansible/inventory/hosts.yml all -m ping


## 6. Start playbook example
docker run --rm -it \
  -v ~/ansible-playbooks:/ansible \
  -v ~/.ssh:/root/.ssh \
  williamyeh/ansible:alpine3 \
  ansible-playbook -i /ansible/inventory/hosts.yml /ansible/"yml file"

## Made by Wookjin
