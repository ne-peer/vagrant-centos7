centos7 vagrantfile.

## Usage on Windows 10
Require [Cmder](http://cmder.net/) installed.


### Step 1
```
λ vagrant plugin install vagrant-winnfsd
λ vagrant plugin install vagrant-vbguest
λ vagrant plugin install vagrant-reload
```

### Step 2
```
λ vagrant up
```

### Step 3
```
λ vagrant ssh-config
Host default
  HostName 127.0.0.1
  User vagrant
  Port 2222
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  PasswordAuthentication no
  IdentityFile C:/Users/foobar/.vagrant.d/insecure_private_key
  IdentitiesOnly yes
  LogLevel FATAL
```

### Step 4
```
λ vagrant ssh-config --host 192.0.0.1 >> C:\Users\foobar\.ssh\config
```
### Complete
```
λ ssh 192.0.0.1
-bash: warning: setlocale: LC_CTYPE: cannot change locale (ja_JP.utf8): No such file or directory
-bash: warning: setlocale: LC_COLLATE: cannot change locale (ja_JP.utf8): No such file or directory
-bash: warning: setlocale: LC_MESSAGES: cannot change locale (ja_JP.utf8): No such file or directory
-bash: warning: setlocale: LC_NUMERIC: cannot change locale (ja_JP.utf8): No such file or directory
-bash: warning: setlocale: LC_TIME: cannot change locale (ja_JP.utf8): No such file or directory
[vagrant@local-vm-host ~]$
```

### ex. Occur Bluescreen?
Do disabled Hyper-V on Windows system.