# ansible_examples
ansible_my_examples

=================================
#multiple packages install
---
- hosts: clients
  become: yes
  tasks:
  -  name: installing multiple  packages
    yum: state=latest name= { { item } }
    with_items:
       - git
       - unzip
       - httpd
       - wget
================================================
