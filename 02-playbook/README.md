# Домашнее задание к занятию «Работа с Playbook»

1. Подготовил inventory-файл `prod.yml`:

Используется виртуальная машина Centos 7, созданная при помощи admin.

2 - 4. Дописан playbook для установки Vector. Playbook использует модули `get_url`, `template`, `unarchive`, `file` и `shell`

Выполняется скачивание, разархивирование в указанную директорию, добавление конфигурации из файла шаблона и запуск Vector.

5. Запустил `ansible-lint site.yml`, увидел наличие ошибок. В данном случае в playbook отсутствовали права на скачиваемые и исполняемые файлы, присутствовали лишние отступы в коде, использовался устаревший синтаксис.

6. Запустил playbook с флагом `--check`. Флаг `--check` не вносит изменения в конечную систему.

![1](https://github.com/troshinvlaad/ansible_practice/blob/main/02-playbook/image-1.PNG?raw=true)

На данный момент возникли трудности с тем, что Ansible не может найти библиотеку firewall версии 0.2.11 или новее на целевой машине. На ВМ устаневлена данная библиотека версии 0.2.0 и нет возможности поставить выше.
