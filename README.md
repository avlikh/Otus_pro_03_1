# OTUS PRO Homework 03-Ansible

### Домашняя работа 03: Установка Nginx через Ansible на порту 8080

### Вариант1: Если Ansible уже развернут:

### 1) Зайдите на OS, где установлен Ansible с root доступом
   - Примечание: используйте пользователя **root** либо команды: **su - root** либо **sudo -i**

### 2) Выполните данную команду на удаленной машине:
```
apt update -y && apt install git -y ; git clone https://github.com/avlikh/Otus_pro_03_1.git /ansible;
```
### 3) Внесите изменения в файл: /ansible/hosts (измените ip-адрес хоста testdeb1 на актуальный)

### 4) Выполните данную команду на удаленной машине. Будет запущен playbook, который установит Nginx и изменит конфиг, что бы демон слушал порт 8080
```
export ANSIBLE_CONFIG=/ansible/ansible.cfg && cd /ansible/ && ansible-playbook /ansible/nginx.yaml -u root --ask-pass;
```
   - Вам потребуется ввести пароль пользователя root для подключения Ansible к удаленной машине (я не использовал rsa-ключи, что бы облегчить Вам прием этого ДЗ) 

### Вариант2: Если Ansible не развернут:

### 1) Зайдите на OS, где будет развернут Ansible с root доступом
   - Примечание: используйте пользователя **root** либо команды: **su - root** либо **sudo -i**
### 2) Выполните данную команду на удаленной машине:
```
apt update -y && apt install git -y ; git clone https://github.com/avlikh/Otus_pro_03_1.git /ansible; /ansible/install_andible_and_lesson3.ssh
```
   - Примечание: Будет выполнена установка репозиториев, основных пакетов и утилит, Ansible и запущен playbook который установит Nginx и изменит конфиг, что бы демон слушал порт 8080 на хосте testdeb1 с ip-адресом:10.68.7.11

   - Вам потребуется ввести пароль пользователя root для подключения Ansible к удаленной машине (я не использовал rsa-ключи, что бы облегчить Вам прием этого ДЗ) 
