# standard-file-unit
Quick and dirty unit to start/stop the Ruby/Puma implementation of Standard File:

https://github.com/standardfile/ruby-server

- Tested on ubuntu 18.04

# Installation
Clone repo to server
- `git clone https://github.com/Tsiklon/standard-file-unit`

Replace the following fields with those appropriate to you
 - 'User' - the service user for Standard File
 - 'Group' - the service group for Standard File
 - 'WorkingDirectory' - the directory where your Standard file instance is located

Copy the unit file to the appropriate location to be used by systemd.
- ` sudo cp -a Path/To/standard-file.service /etc/systemd/system/standard-file.service`

Reread the system's units
- `sudo systemctl daemon-reload`

Start the unit
- `sudo systemctl start standard-file.service`

if you wish to have the unit start at boot:
- `sudo systemctl enable standard-file.service`
