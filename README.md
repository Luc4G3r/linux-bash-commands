# linux-bash-commands

Miscellaneous bash command aliases / shell scripts for php web development

## Contents
1. [PHP XDebug](https://github.com/Luc4G3r/linux-bash-commands/tree/main/php_xdebug)
2. [Creating Bash Commands](https://github.com/Luc4G3r/linux-bash-commands/#creating-bash-commands)
3. [Creating Linux Services](https://github.com/Luc4G3r/linux-bash-commands/#creating-linux-services)



### Creating Bash Commands
- Create shell script (f.e.: /etc/custom_commands/script.sh)
    - Don't forget to add `#!/bin/bash` or another interpreter
- Symlink shell script to /usr/local/bin  
  `ln -s /etc/custom_commands/script.sh /usr/local/bin/script`

### Creating Linux Services
- [Create Bash Command](https://github.com/Luc4G3r/linux-bash-commands/#creating-bash-commands)
- Create a service file `/lib/systemd/system/my.service`
  ```
  [Unit]
  Description=<description about this service>

  [Service]
  User=<user e.g. root>
  WorkingDirectory=<directory_of_script e.g. /home/user>
  ExecStart=/usr/local/bin/script

  [Install]
  WantedBy=multi-user.target
  ```
- Link service file to systemd  
  `ln -s /lib/systemd/system/my.service /etc/systemd/system/my-service.service`
- Reload service configurations  
  `sudo systemctl daemon-reload`
- Start service  
  `sudo systemctl start my`
- Check service status  
  `sudo systemctl status my`
