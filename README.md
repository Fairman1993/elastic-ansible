# Установка
$ sudo apt install software-properties-common

$ sudo apt-add-repository ppa:ansible/ansible

$ sudo apt-get update

$ sudo apt install ansible -y

$ sudo apt install python3-pip -y

$ ansible-galaxy install elastic.elasticsearch,v7.16.0

# Запуск
## Одна нода
$ ansible-playbook -i hosts ./1.yml
## Две ноды
$ ansible-playbook -i hosts ./2.yml

# Проверить деплой
## Посмотреть ноды
$ curl -u elastic:changeme  -k 'https://127.0.0.1:9200/_cat/nodes?v'

## Проверить состояние кластера
$ curl -u elastic:changeme -k 'https://127.0.0.1:9200/_cluster/health?pretty'
