
# AUTOCLEAN   SERVICE
 While initial start of my linux I faced a problem. Which says that "x session warning unable to write to /tmp"
 To solve the problem I need to enter the console and run " sudo apt-get clean". But each time doing this is no sense. So I decide to create a service to clean it automatically.
 
 ## Installation

To run this service there is ne requirements but linux environment.

Downloading from github.
```sh
cd Desktop
git clone https....
cd Autoclean
```

For production environments...

Link downloaded file to system file.
```sh
sudo ln -s autoclean.service /etc/systemd/system/ 
```

Reload the service files to include the new service.
```sh
sudo systemctl daemon-reload
```

Start your service
```sh
sudo systemctl start autoclean
```

To check the status of your service
```sh
sudo systemctl status autoclean.service
```

To enable your service on every reboot
```sh
sudo systemctl enable autoclean.service
```

To disable your service on every reboot
```sh
sudo systemctl disable autoclean.service
```

To see logs of your service
```sh
sudo journalctl -f
```

## License

MIT

