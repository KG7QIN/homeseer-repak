Welcome to the HomeSeer Linux Repak repo

This repo includes the .deb files to install HomeSeer 4.2.22.4 on Debian/Ubuntu linux.

To setup this repo on your system:

## Download the homeseer_key.asc file to /etc/apt/keyrings/homeseer_key.asc
### Run
`sudo gpg --yes -o /etc/apt/keyrings/homeseer_key.gpg --dearmor /etc/apt/keyrings/homeseer_key.asc`
`sudo rm /etc/apt/keyrings/homeseer_key.asc`
`sudo chown root:root /etc/apt/keyrings/homeseer_key.gpg`
`sudo chmod ugo+r /etc/apt/keyrings/homeseer_key.gpg`
`sudo chmod go-w /etc/apt/keyrings/homeseer_key.gpg`

### Add this repository to your system by adding to to /etc/apt/sources.list/homeseer-repak.list
`deb [signed-by=/etc/apt/keyrings/homeseer_key.gpg] http://homeseer.digiflux.org/public stable main`
