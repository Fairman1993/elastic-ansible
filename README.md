# Установка
$ ansible-galaxy install elastic.elasticsearch,v7.16.0

# Запуск
## Одна нода
$ ansible-playbook -i hosts ./1.yml
## Две ноды
$ ansible-playbook -i hosts ./2.yml
