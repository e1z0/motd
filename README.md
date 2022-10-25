# motd
Simple motd scripts for Raspberry PI


<img width="1057" alt="Screenshot 2022-10-05 at 15 01 01" src="https://user-images.githubusercontent.com/7213361/194055689-190ca33a-9ba6-4d20-973b-3ca70831c605.png">


# install

```
sudo apt install figlet git
git clone https://github.com/n-ham/lolcat-cc.git && cd lolcat-cc && make && sudo make install && cd .. && rm -rf lolcat-cc
sudo git clone https://github.com/e1z0/motd /etc/update-motd.d
sudo rm /etc/motd
# it should update upon new login
# If you want to use oldschool /etc/motd you can update it every minute
echo "* * * * * root run-parts --lsbsysinit /etc/update-motd > /etc/motd" >> /etc/crontab # always update motd
```



You can add user defined services in **$HOME/.srvc** (please note that motd generation works in super user privileges as root)
```
services=("docker" "nfs-server")
```
