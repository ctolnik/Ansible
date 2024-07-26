Disk Encryption
=========

Шифрование дисков с помощью LUKS

https://habr.com/ru/companies/macloud/articles/552040/

Requirements
------------
- Ansible 2.9 or higher
- SSH access to target servers
- Sudo privileges on target servers

Role Variables
--------------
 - `keyfile` - Путь к файлу для шифрования; По умолчанию:  /root/luks_key.yml
 - `luks_key` - Ключ шифрования, записывается в файл указанный в переменной keyfile
 - `mycrypt` - Имя Luks контейнера.
 - `target_device`: Имя дискового устройства для шифрования (Например, `/dev/sdb`)

При нахождение партиции вызывается ошибка для остановки работы PlayBook.
Для шифрования партиций следующих после /, полученные имена в диске можно передавать в цикле подставляя в `target_device`. Автоматика отключена для сохранности данных.
