# Installing Wordpress and LEMP.

## Check if RedHat.
### 1. Install tar on CentOS or RHEL.
```bash
yum search tar
yum list tar
yum update
yum install tar
```

### 2. Allow HTTP and HTTPS through the firewall.
```bash
firewall-cmd --permanent --add-service={http,https}
firewall-cmd --reload
```

## Add your inventory.
```bash
cat > inventoryes/staging
```

## Edit variables in vars/wordpress-80/main.yml
```bash
server_name: "194.58.90.166"
mysql_db: "wordpress"
mysql_user: "wordpress"
mysql_password: "Ghi~36vhy$#jkbCV"
```

## Launch playbook.
```bash
ansible-playbook wordpress-80.yml
```

Tested on AlmaLinux 8, Ubuntu 20.04 LTS, Debian 11
