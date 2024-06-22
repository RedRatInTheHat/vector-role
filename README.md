vector-role
=========

В очень упрощённом виде скачивает и устанавливает [Vector](https://vector.dev/)

Requirements
------------

* Ansible core 2.16.7 и выше.
* На стороне хоста: 
    * SSH service;
    * Python версии, [соответствующей Ansible core](https://docs.ansible.com/ansible/latest/reference_appendices/release_and_maintenance.html#ansible-core-support-matrix).
    * RPM-based дистрибутив (требуется yum в качестве пакетного менеджера).

Role Variables
--------------

[defaults/main.yml](defaults/main.yml)

| Параметр | Default | Что это |
|----------|---------|---------|
| vector_version | "0.38.0" |  Версия Vector |

[vars/main.yml](vars/main.yml)

| Параметр | Default | Что это |
|----------|---------|---------|
| vector_user | "vector" | Пользователь для запуска Vector |
| vector_group | "vector" | Группа пользователей для запуска Vector |


Example Playbook
----------------

```yml
- hosts: vector
  roles:
    - vector-role
```