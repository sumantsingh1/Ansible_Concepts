# Loop
In Ansible, loops allow you to repeat tasks over a list of items. You can use loops to iterate over variables, files, or anything that needs to be processed multiple times.

Here are some common ways to use loops in Ansible:
## 1. Simple Loop
You can loop over a list of items using the loop keyword.
- name: Install multiple packages
  ansible.builtin.yum:
    name: "{{ item }}"
    state: present
  loop:
    - httpd
    - nginx
    - mariadb
