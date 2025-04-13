# 26 Домашнее задание:  LDAP
Задание:
  1) Установить FreeIPA
  2) Написать Ansible-playbook для конфигурации клиента

ДЗ выполнялось по инструкции на VM centos/stream9 v.20250331.0.
Vagrantfile создает 3 VM ipa server, client1, client2.

Необходимые настройки и установку ip сервера выполнаяет ansible-workbook ldap_ipasrv.yml


Конфигурирование ipa сервера:
![Image alt](https://github.com/AlexndrVakulenko/homework26/blob/main/screenshots/01_ipa_srv_install.png)

Проверим, что сервер Kerberos может выдать нам билет:
![Image alt](https://github.com/AlexndrVakulenko/homework26/blob/main/screenshots/02_check_srv.png)

Настройку клиентов выполнаяет ansible-workbook ldap_clients.yml

Создание пользователя на сервере:
![Image alt](https://github.com/AlexndrVakulenko/homework26/blob/main/screenshots/03_create_user.png)

Проверка на клиенте client1:
![Image alt](https://github.com/AlexndrVakulenko/homework26/blob/main/screenshots/04_check_on_client1.png)

Web интерфейс из хостовой машины:
![Image alt](https://github.com/AlexndrVakulenko/homework26/blob/main/screenshots/05_web_ipa.png)

Проверка на клиенте client2:
![Image alt](https://github.com/AlexndrVakulenko/homework26/blob/main/screenshots/06_check_on_client2.png)
