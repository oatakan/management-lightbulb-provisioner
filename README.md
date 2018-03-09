Requirements:

- name: install packages needed
  yum:
    name: "{{ item }}"
    state: latest
  with_items:
    - python2-pip
    - python-configparser
    - httpd-tools
    - java-1.8.0-openjdk-headless

- name: install manageiq-client
  pip:
    name: manageiq-client

- name: install ansible-tower-cli
  pip:
    name: ansible-tower-cli
    
- name: install other packages:
  pip:
    name: "{{ item }}"
  with_items:
    - passlib
    - pyapi-gitlab
    - pywinrm
    - sendgrid==2.2.1