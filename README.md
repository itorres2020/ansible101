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

### Inventario
Se crea un archivo bpasico de inventario para el laboratorio.
Este consiste en un archivo de texto con las IPs de los equipos a administrar

```console
10.0.5.24
```

### Prueba
Se ejecuta el siguiente comando para verificar el acceso a los sistemas a administrar por ansible:

```console
ticss@ansible:~/ansible101$ ansible all --key-file ~/.ssh/ansible -i inventory -m ping
```

Y se espera una respuesta como esta:

```console
10.0.5.24 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3"
    },
    "changed": false,
    "ping": "pong"
}
```