# Omnisci_install

```
sudo apt update
sudo apt upgrade
```

```
sudo mkdir /opt/omnisci-installs/
sudo wget https://releases.omnisci.com/ee/tar/omnisci-ee-latest-Linux-x86_64-cpu.tar.gz -O /opt/omnisci-installs/omnisci.tar.gz
```

```
cd /opt/omnisci-installs/
sudo tar -xvf omnisci.tar.gz
```

```
cd /opt
sudo ln -s /opt/omnisci-installs/omnisci-ee-4.8.1-20190827-0f29e432f1-Linux-x86_64-cpu omnisci
```

```
cd
sudo nano .bashrc
```
append this
```
export OMNISCI_USER=omnisci
export OMNISCI_GROUP=omnisci
export OMNISCI_STORAGE=/var/lib/omnisci
export OMNISCI_PATH=/opt/omnisci
export OMNISCI_LOG=/var/lib/omnisci/data/mapd_log
```

<img width="304" alt="image" src="https://user-images.githubusercontent.com/77326619/193449208-5eca22a2-7b3f-4f5b-a832-bc3ab777b12a.png">

```
cd $OMNISCI_PATH/systemd
./install_omnisci_systemd.sh
```
<img width="425" alt="image" src="https://user-images.githubusercontent.com/77326619/193449248-6720d1b5-4ff3-4ff7-809c-6dd6d3e357a3.png">

```
sudo systemctl start omnisci_server
sudo systemctl start omnisci_web_server
sudo systemctl enable omnisci_server
sudo systemctl enable omnisci_web_server
```

<img width="944" alt="image" src="https://user-images.githubusercontent.com/77326619/193449287-e6324030-6455-4bc1-8989-b5e77e582a56.png">
