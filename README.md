Обновление ядра


При попытке выполнить команду 


sudo yum install -y https://www.elrepo.org/elrepo-release-8.el8.elrepo.noarch.rpm 

Ругался, что не может найти имя. 
Думал, что проблема в ДНС, но в итоге пришлось выключить репозиторий extras-common

после этого порядок был такой 

curl -O https://www.elrepo.org/elrepo-release-8.el8.elrepo.noarch.rpm
yum localinstall -y elrepo-release-8.el8.elrepo.noarch.rpm
yum --enablerepo=elrepo-kernel install kernel-ml -y
grub2-mkconfig -o /boot/grub2/grub.cfg
grub2-set-default 0
reboot


После выполненных действий ядро обновилось с 
4.18.0-516.el8.x86_64
на 
6.12.9-1.el8.elrepo.x86_64
