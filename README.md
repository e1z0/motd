# motd
Simple motd scripts

# install

```
sudo apt install figlet git
git clone https://github.com/n-ham/lolcat-cc.git && cd lolcat-cc && make && sudo make install && cd .. && rm -rf lolcat-cc
sudo git clone https://github.com/e1z0/motd /etc/update-motd
sudo run-parts --lsbsysinit /etc/update-motd > /etc/motd # update actual motd
echo "* * * * * root run-parts --lsbsysinit /etc/update-motd > /etc/motd" >> /etc/crontab # always update motd
```
