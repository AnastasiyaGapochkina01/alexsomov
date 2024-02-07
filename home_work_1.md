1) в домашнем каталоге создать каталог inform_фамилия (фамилия латиницей).
2) перейти в каталог inform_фамилия создать в нем каталог lab1
3) внутри каталога lab1 создать каталог catalog1, файл file1, каталог catalog2. Перейти в каталог catalog2.
4) внутри каталога catalog2 создать файлы file3 и file4, каталог catalog3
5) внутри каталога catalog3 создать файл file5, жесткую ссылку на файл file1
6) создать в каталоге lab1 символическую ссылку s_link на файл file5
7) вывести полученную структуру каталогов командой tree
8) в каталоге lab1 создать директорию files
9) перейти в каталог files, создать в нем 10 файлов file1.txt, file2.txt, file3.txt ... file10.txt (идеальное решение в одну команду)
10) скопировать всю директорию files в files2
11) удалить файлы file2.txt, file3.txt и file5.txt в директории files2
12) скопировать файлы file2.txt, file3.txt и file5.txt из директории files в директорию files2
13) переименовать ВСЕ файлы в директории files2 из file(1,2,3...).txt в text_file_(1,2,3...).txt
14) удалить директорию files
15) переименовать директорию files2 в text_files
16) удалить директорию text_files
17) в директории lab1 создать пустой файл output
18) перенаправить вывод команды tree -a ~/inform_фамилия в файл output
19) По умолчанию ls сортирует вывод по алфавиту. Отсортировать вывод команды ls по
- размеру файла
- по времени модификации файла
и перенаправить в файл output (ДОПИСАТЬ в него, а не ПЕРЕзаписать)
20) с помощью команды lsblk вывести список дисков, подключенных к ВМ
- найти в каталоге /dev основной диск
- посмотреть его содержимое утилитой hexdump
21) Посмотреть первые шесть записей любого лога из /var/log
22) Посмотреть последние двадцать записей любого лога из /var/log
33) С помощью cat, grep и cut вывести id (3 поле в строке) пользователя www-data (если такого пользователя нет, то выбрать любого существующего пользователя и выполнить задание для него)
24) С помощью grep вывести и пронумеровать все строки из /etc/passwd, где встречается строка /bin/bash
25) Из файла /proc/meminfo выести всю информацию о HugePages (там скорее всего будет всё по нулям, это норма)
26) Из файла /proc/stat высести информацию про softirq
27) Вывести участников группы docker
28) Выпонить команду ```ip -o a``` и получить ip машины (нужно получить только ip)

то есть если вывод будет иметь такой вид
```
root@ruvds-wil5w:~# ip -o a
1: lo    inet 127.0.0.1/8 scope host lo\       valid_lft forever preferred_lft forever
1: lo    inet6 ::1/128 scope host \       valid_lft forever preferred_lft forever
2: eth0    inet 195.133.199.48/24 scope global eth0\       valid_lft forever preferred_lft forever
2: eth0    inet6 fe80::215:5dff:fe0c:33e5/64 scope link \       valid_lft forever preferred_lft forever
3: docker0    inet 172.17.0.1/16 brd 172.17.255.255 scope global docker0\       valid_lft forever preferred_lft forever
3: docker0    inet6 fe80::42:ffff:fe83:f708/64 scope link \       valid_lft forever preferred_lft forever
49: br-7f6b2a795952    inet 172.21.0.1/16 brd 172.21.255.255 scope global br-7f6b2a795952\       valid_lft forever preferred_lft forever
49: br-7f6b2a795952    inet6 fe80::42:6eff:fed1:17a/64 scope link \       valid_lft forever preferred_lft forever
50: br-bcb69017f222    inet 172.22.0.1/16 brd 172.22.255.255 scope global br-bcb69017f222\       valid_lft forever preferred_lft forever
50: br-bcb69017f222    inet6 fe80::42:92ff:fefa:4b8c/64 scope link \       valid_lft forever preferred_lft forever
55: br-e66bd26eec4f    inet 172.23.0.1/16 brd 172.23.255.255 scope global br-e66bd26eec4f\       valid_lft forever preferred_lft forever
55: br-e66bd26eec4f    inet6 fe80::42:b3ff:fe9f:3ac1/64 scope link \       valid_lft forever preferred_lft forever
56: br-6a21e8afa4e8    inet 172.24.0.1/16 brd 172.24.255.255 scope global br-6a21e8afa4e8\       valid_lft forever preferred_lft forever
56: br-6a21e8afa4e8    inet6 fe80::42:afff:feb3:bca8/64 scope link \       valid_lft forever preferred_lft forever
61: br-1a68cb1ae613    inet 172.25.0.1/16 brd 172.25.255.255 scope global br-1a68cb1ae613\       valid_lft forever preferred_lft forever
61: br-1a68cb1ae613    inet6 fe80::42:a5ff:fe56:fd1d/64 scope link \       valid_lft forever preferred_lft forever
62: br-70eaefbd8c8a    inet 172.26.0.1/16 brd 172.26.255.255 scope global br-70eaefbd8c8a\       valid_lft forever preferred_lft forever
62: br-70eaefbd8c8a    inet6 fe80::42:b6ff:fe61:dafc/64 scope link \       valid_lft forever preferred_lft forever
67: br-e578a222aff7    inet 172.27.0.1/16 brd 172.27.255.255 scope global br-e578a222aff7\       valid_lft forever preferred_lft forever
67: br-e578a222aff7    inet6 fe80::42:8dff:fe9c:4b7d/64 scope link \       valid_lft forever preferred_lft forever
68: br-c2aad6b2db24    inet 172.28.0.1/16 brd 172.28.255.255 scope global br-c2aad6b2db24\       valid_lft forever preferred_lft forever
68: br-c2aad6b2db24    inet6 fe80::42:5cff:fef1:3077/64 scope link \       valid_lft forever preferred_lft forever
75: br-8d6fa7670f10    inet 172.29.0.1/16 brd 172.29.255.255 scope global br-8d6fa7670f10\       valid_lft forever preferred_lft forever
75: br-8d6fa7670f10    inet6 fe80::42:33ff:fe9b:322c/64 scope link \       valid_lft forever preferred_lft forever
90: br-728dc5cb31e8    inet 192.168.32.1/20 brd 192.168.47.255 scope global br-728dc5cb31e8\       valid_lft forever preferred_lft forever
90: br-728dc5cb31e8    inet6 fe80::42:1fff:feda:3223/64 scope link \       valid_lft forever preferred_lft forever
126: vethe56e01c    inet6 fe80::ac37:efff:feb9:9ac/64 scope link \       valid_lft forever preferred_lft forever
128: vethb1a3c0d    inet6 fe80::20d3:e5ff:fe17:aef2/64 scope link \       valid_lft forever preferred_lft forever
129: br-51f290e1b149    inet 192.168.112.1/20 brd 192.168.127.255 scope global br-51f290e1b149\       valid_lft forever preferred_lft forever
129: br-51f290e1b149    inet6 fe80::42:dbff:fe6c:beea/64 scope link \       valid_lft forever preferred_lft forever
131: veth504b973    inet6 fe80::2c3b:caff:fe7b:1f7d/64 scope link \       valid_lft forever preferred_lft forever
170: veth12752b5    inet6 fe80::909b:2eff:fe6b:a551/64 scope link \       valid_lft forever preferred_lft forever
171: br-2c78a6fa2013    inet 192.168.208.1/20 brd 192.168.223.255 scope global br-2c78a6fa2013\       valid_lft forever preferred_lft forever
171: br-2c78a6fa2013    inet6 fe80::42:67ff:fe6b:e922/64 scope link \       valid_lft forever preferred_lft forever
173: vethb64904a    inet6 fe80::9846:24ff:feea:8935/64 scope link \       valid_lft forever preferred_lft forever
root@ruvds-wil5w:~#
```
то отсюда нужно вывести только 195.133.199.48

29) Из вывода команды ```lscpu``` получить частоту работы процессора
30) Из вывода команды ```mount``` получить опции монтирования для ```/dev/sda1```
31) Из вывода команды ```lsb_release -a``` получить полную версию системы
32) Из вывода команды ```df -Th``` получить объем ФС под ```/dev/sda1``` (у тебя на ВМ может отличаться)
