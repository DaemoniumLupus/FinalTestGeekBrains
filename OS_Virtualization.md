# 1. Использование команды cat в Linux

Приведены введенные команды и результат их исполнения.

```bash
ilya-bakushkin@DLupus:~$cat>Pets.txt
dog
cat
hamster
ilya-bakushkin@DLupus:~$cat>PackAnimals.txt
horse
camel
donkey
ilya-bakushkin@DLupus:~$cat Pets.txt PackAnimals.txt > Animals.txt
ilya-bakushkin@DLupus:~$cat Animals.txt
dog
cat
hamster
horse
camel
donkey
ilya-bakushkin@DLupus:~$mv Animals.txt HumanFriends.txt
ilya-bakushkin@DLupus:~$cat HumanFriends.txt
dog
cat
hamster
horse
camel
donkey
ilya-bakushkin@DLupus:~$ls
HumanFriends.txt  PackAnimals.txt  Pets.txt  WindowsShared
```

# 2. Работа с директориями в Linux

Приведены введенные команды и результат их исполнения.

```bash
ilya-bakushkin@DLupus:~$mkdir txt
ilya-bakushkin@DLupus:~$mv HumanFriends.txt txt/HumanFriends.txt
ilya-bakushkin@DLupus:~$cd txt
ilya-bakushkin@DLupus:~/txt$ls
HumanFriends.txt
ilya-bakushkin@DLupus:~/txt$cat HumanFriends.txt
dog
cat
hamster
horse
camel
donkey
```

# 3. Работа с MySQL в Linux. 

Приведены введенные команды и результат их исполнения.

```bash
ilya-bakushkin@DLupus:~/txt$cd ../
ilya-bakushkin@DLupus:~$mkdir Downloads
ilya-bakushkin@DLupus:~$cd Downloads/
ilya-bakushkin@DLupus:~/Downloads$wget https://dev.mysql.com/get/mysql-apt-config_0.8.29-1_all.deb
mysql-apt-config_0.8.29-1_a 100%[===========================================>]  17.75K  --.-KB/s    in 0.001s
2024-04-05 14:14:52 (16.7 MB/s) - ‘mysql-apt-config_0.8.29-1_all.deb’ saved [18172/18172]
ilya-bakushkin@DLupus:~/Downloads$ls
mysql-apt-config_0.8.29-1_all.deb
ilya-bakushkin@DLupus:~/Downloads$sudo dpkg -i mysql-apt-config_0.8.29-1_all.deb
ilya-bakushkin@DLupus:~/Downloads$sudo apt-get update
ilya-bakushkin@DLupus:~/Downloads$sudo apt-get install mysql-server
ilya-bakushkin@DLupus:~/Downloads$systemctl status mysql.service
● mysql.service - MySQL Community Server
     Loaded: loaded (/lib/systemd/system/mysql.service; enabled; vendor preset: enabled)
     Active: active (running) since Mon 2024-04-05 14:18:07 UTC; 19s ago
       Docs: man:mysqld(8)
             http://dev.mysql.com/doc/refman/en/using-systemd.html
   Main PID: 2806 (mysqld)
     Status: "Server is operational"
      Tasks: 38 (limit: 9389)
     Memory: 364.2M
        CPU: 683ms
     CGroup: /system.slice/mysql.service
             └─2806 /usr/sbin/mysqld

Apr 01 23:18:06 ubuntuserver systemd[1]: Starting MySQL Community Server...
Apr 01 23:18:07 ubuntuserver systemd[1]: Started MySQL Community Server.

```

# 4. Управление deb-пакетами 

deb-пакет был установлен на предыдущем шаге. Выполняем удаление.

```bash
ilya-bakushkin@DLupus:~/Downloads$sudo dpkg -r mysql-apt-config
(Reading database ... 75168 files and directories currently installed.)
Removing mysql-apt-config (0.8.29-1) ...
```

# 5. История команд в терминале Ubuntu

История команд записана в файл и выведена в консоль.

```bash
ilya-bakushkin@DLupus:~/txt$history | tail -n 37 > IlyaBakushkin_05.04.2024.txt
ilya-bakushkin@DLupus:~/txt$cat IlyaBakushkin_05.04.2024.txt
  100  cat>Pets.txt
  101  cat>PackAnimals.txt
  102  nano PackAnimals.txt
  103  cat Pets.txt PackAnimals.txt > Animals.txt
  104  cat Animals.txt
  105  mv Animals.txt HumanFriends.txt
  106  cat HumanFriends.txt
  107  ls
  108  mkdir txt
  109  mv HumanFriends.txt txt/HumanFriends.txt
  110  cd txt
  111  ls
  112  cat HumanFriends.txt
  113  cd ../
  114  mkdir Downloads
  115  cd Downloads/
  116  man wget
  117  wget https://dev.mysql.com/downloads/file/?id=524196
  118  ls
  119  rm index.html\?id\=524196
  120  ls
  121  wget https://dev.mysql.com/get/mysql-apt-config_0.8.29-1_all.deb
  122  ls
  123  sudo dpkg -i mysql-apt-config_0.8.29-1_all.deb
  124  sudo apt-get update
  125  sudo apt-get install mysql-server
  126  systemctl status mysql.service
  127  dpgk --help
  128  dpkg --help
  129  dpkg -r mysql-apt-config
  130  sudo dpkg -r mysql-apt-config
  131  history
  132  history --help
  133  tail --help
  134  history | tail -n 35
  135  cd ../txt/
  136  history | tail -n 37 > IlyaBakushkin_05.04.2024.txt
```
