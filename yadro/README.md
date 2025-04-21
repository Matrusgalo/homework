Обновление ядра системы

1) Запустить ВМ c Ubuntu.
2) Обновить ядро ОС на новейшую стабильную версию из mainline-репозитория.
3) Оформить отчет в README-файле в GitHub-репозитории.
1  uname -r

6.8.0-53-generic
    2  mkdir kernel
    3  cd kernel/
    4  ls
    5  wget https://kernel.ubuntu.com/mainline/v6.14/amd64/linux-headers-6.14.0-061400-generic_6.14.0-061400.202503241442_amd64.deb
    6  wget https://kernel.ubuntu.com/mainline/v6.14/amd64/linux-headers-6.14.0-061400_6.14.0-061400.202503241442_all.deb
    7  wget https://kernel.ubuntu.com/mainline/v6.14/amd64/linux-image-unsigned-6.14.0-061400-generic_6.14.0-061400.202503241442_amd64.deb
    8  wget https://kernel.ubuntu.com/mainline/v6.14/amd64/linux-modules-6.14.0-061400-generic_6.14.0-061400.202503241442_amd64.deb
    9  ls
   10  sudo dpkg -i *.deb
   11  ls /boot/
   12  sudo update-grub
   13  sudo grub-set-default 0
   14  sudo reboot
   15  uname -r
6.14.0-061400-generic




