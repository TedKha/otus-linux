sudo rpm --import https://www.elrepo.org/RPM-GPG-KEY-elrepo.org
sudo rpm -Uvh http://www.elrepo.org/elrepo-release-7.0-2.el7.elrepo.noarch.rpm
sudo yum --disablerepo="*" --enablerepo="elrepo-kernel" list available
sudo yum --enablerepo=elrepo-kernel install kernel-ml
sudo reboot
uname -sr
sudo vi /etc/defaul/grub 
изменить значение переменной GRUB_DEFAULT на 0
sudo grub2-mkconfig -o /boot/grub2/grub.cfg
sudo reboot
