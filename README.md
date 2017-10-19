Requirements:

- name: install pip needed for manageiq-client
  yum:
    name: python2-pip
    state: latest

- name: install manageiq-client
  pip:
    name: manageiq-client

- name: install ansible-tower-cli
  pip:
    name: ansible-tower-cli