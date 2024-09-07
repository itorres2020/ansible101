# Ansible 101 Lab
Laboratorio para Ansible sobre Ubuntu

## Introducción
Este es un ejemplo para comprender mejor el uso de la tecnología de Ansible.

## Máquinas involucradas
 - 10.0.5.23 / Ansible control
 - 10.0.5.24 / Big Blue Button

## Ansible Control
Esta máquina se instala con la finalidad de realizar el despliegue de comandos de ansible.
Es un ubuntu 20.04.6 y se realizo la instalacíon de ansible seguin estos comandos:

```console
$ sudo apt-get update
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository --yes --update ppa:ansible/ansible
$ sudo apt-get install ansible
```