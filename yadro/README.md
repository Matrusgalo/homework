Обновление ядра системы

1) Запустить ВМ c Ubuntu.
2) Обновить ядро ОС на новейшую стабильную версию из mainline-репозитория.
3) Оформить отчет в README-файле в GitHub-репозитории.

~~~
uname -r
6.8.0-53-generic
mkdir kernel
cd kernel/
ls
wget https://kernel.ubuntu.com/mainline/v6.14/amd64/linux-headers-6.14.0-061400-generic_6.14.0-061400.202503241442_amd64.deb
wget https://kernel.ubuntu.com/mainline/v6.14/amd64/linux-headers-6.14.0-061400_6.14.0-061400.202503241442_all.deb
wget https://kernel.ubuntu.com/mainline/v6.14/amd64/linux-image-unsigned-6.14.0-061400-generic_6.14.0-061400.202503241442_amd64.deb
wget https://kernel.ubuntu.com/mainline/v6.14/amd64/linux-modules-6.14.0-061400-generic_6.14.0-061400.202503241442_amd64.deb
sudo dpkg -i *.deb
ls /boot/
sudo update-grub
sudo grub-set-default 0
sudo reboot
uname -r
6.14.0-061400-generic
~~~


