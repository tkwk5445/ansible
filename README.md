# Start playbook example

docker run --rm -it \
  -v ~/ansible-playbooks:/ansible \
  -v ~/.ssh:/root/.ssh \
  williamyeh/ansible:alpine3 \
  ansible-playbook -i /ansible/inventory/hosts.yml /ansible/"yml file"

