# Описание
Репозиторий, где я аккумулирую все playbook для конфигурации серверов через Ansible

## Предварительные требования
- Настроенный сервер SSH на узле
- Пользователь (ansible_user из файла инвентаризации) должен быть добален в группу sudo

## Проверка доступности узлов
```ansible srv -i inventory/inv.ini -m ping -k```

## Запуск первоначальной настройки хостов
```ansible-playbook -i inventory/inv.ini initialSetup/main.yml -K```