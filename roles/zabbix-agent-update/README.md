zabbix-agent-update
ставит определенную версию пакета только на Debian 9

```
Пример запуска
ansible-playbook zabbix-agent-update.yml -i last.list --extra-vars "variable_host=all" | tee out/last_list

Где last.list - inventory file
    extra-vars - нужная группа в списке
    tee out/... - вывод в файл, и так же доп. гарантия что плейбук не захлебнется
```

версия пакета, или же пакетов (стоит цикл)
ставится в defaults/main.yml

```
package_name:
  - zabbix-plugins-pan=0.3.385
```
