# Vagrantfile to Rails development with PostgreSQL 10

This Vagrantfile configure two machines using the provider VirtualBox, one VM with Rails and another with PostgreSQL 10.

## Usage

1. Have the vagrant installed.
2. Copy or clone or make download the Vagrantfile to target directory.
3. Run in your terminal `vagrant up && vagrant ssh rails`.
4. Wait the both VMs installation and configuration.
5. If everything went right you will be logged in Rails VM.
6. Good look and enjoy!

## VMs details
|Attributes|Values|
|----|----|
|Box | **CentOS 7**|
|CPU | **2**|
|Memory | **512**|
|Synced folder | host: **.** <br> guest: **/vagrant**

### More details
- The VIM is installed in both VM.
- You can change the guest mount point at variable **GUEST_MOUNT_POINT**

___
## Rails VM details

### Forwarded ports
|Host|Guest|
|---|---|
|3000|3000|

### More details
- The Ruby is installed by rbenv.
- The Javascript runner is the Nodejs.

___
## PostgreSQL VM details

|Database attributes|Values|
|----|----|
Address| **192.168.1.10**
Username|**vagrant**
Password|**vagrant**

### Forwarded ports
|Host|Guest|
|---|---|
|none|none|

### More details
- The PostgreSQL is installed from the official PostgreSQL repositories.

- This VM uses static IP, you can change it by variable **DATABASE_SERVER_IP**.

- The PostgreSQL is starded on boot.
