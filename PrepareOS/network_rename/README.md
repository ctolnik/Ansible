##Network_rename
=========

Переименование сетевого интерфейса по умолчанию в "net0"

##Requirements
------------
- Netplan on ansible_host
- Ansible 2.9 or higher
- SSH access to target servers
- Sudo privileges on target servers

##Role Variables
--------------
  - `netplan_filename` - Имя файла, где будут искаться настройки интерфейса; По умолчанию: `50-cloud-init.yaml`
  - `new_iface_name` - Имя в которое будет переименован интерфейс. По умолчанию: `net0`