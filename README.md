[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)

Welcome to the HomeSeer Linux Repak repo

This repo includes the .deb files to install HomeSeer 4.2.22.4 on Debian/Ubuntu linux.

To setup this repo on your system:

### Download the homeseer_key.asc file
```
sudo wget https://homeseer.digiflux.org/homeseer_key.asc
sudo mv homeseer_key.asc /etc/apt/keyrings/
```

### Now add the key to system's package repository keychain
```
sudo gpg --yes -o /etc/apt/keyrings/homeseer_key.gpg --dearmor /etc/apt/keyrings/homeseer_key.asc
sudo rm /etc/apt/keyrings/homeseer_key.asc
sudo chown root:root /etc/apt/keyrings/homeseer_key.gpg
sudo chmod ugo+r /etc/apt/keyrings/homeseer_key.gpg
sudo chmod go-w /etc/apt/keyrings/homeseer_key.gpg
```

### Add this repository to your system by adding to to /etc/apt/sources.list/homeseer-repak.list
```
deb [signed-by=/etc/apt/keyrings/homeseer_key.gpg] http://homeseer.digiflux.org/public stable main
```

### Update your packages
```
sudo apt update
```

### Now download and install home HomeSeer .deb package
```
sudo apt install homeseer
```


