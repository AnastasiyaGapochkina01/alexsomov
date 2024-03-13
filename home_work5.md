1) Написать скрипт, который будет мониторить использование дискового пространства (исключить tmpfs, cdrom). Необходимо получить
Size, Use%. Если Use% больше 60, то нужно записать в файл /var/log/disk_space.log алерт вида:
    ```
    The partition "$файловая_система" on $hostname has used Use% at дата время
    ```
    - написать юнит-файл для запуска скрипта, запустить, проверить

2) Написать скрипт, который получает LA (15) в системе, сравнивает полученное значение с лимитом (0.02), и если полученное значение больше лимита, то записывает в 
/var/log/la.log строку вида
    ```
    дата время ALERT: current LA ($значение_la) is too high
    ```
    например
    ```
    02.08.2023 08:11:31 ALERT: current LA 3.15 is too high
    ```
    - написать юнит-файл для запуска скрипта, запустить, проверить

3) НЕОБЯЗАТЕЛЬНО
попробовать создать второй экземпляр sshd сервиса по аналогии с
https://access.redhat.com/documentation/ru-ru/red_hat_enterprise_linux/8/html/using_systemd_unit_files_to_customize_and_optimize_your_system/assembly_working-with-systemd-unit-files_working-with-systemd#proc_creating-custom-unit-files_assembly_working-with-systemd-unit-files
