# install-nextcloud
Scripts to install and optimize Nextcloud (based on Ubuntu 18.04.x (AMD64/ARM64) or Debian Stretch 9.x / Debian 10.x Buster (AMD64)) with NGINX 1.17.x, MariaDB 10.4 (or PostgreSQL), PHP 7.3.x, Redis-Server, fail2ban, ufw and self signed or Let's Encrypt certificates

    Build your self hosted Nextcloud server on either Ubuntu or Debian with
        a) MariaDB 10.4 (recommended!)
        b) PostgreSQL
    
The scripts called install-nextcloud-<database>-debian.sh and install-nextcloud-<database>-ubuntu.sh will install your self hosted Nextcloud within 10 minutes, fully prepared for Ubuntu 18.04.x or Debian 9.x Stretch environments and will consist of:

    Fail2Ban (Nextcloud and SSH jails)
    MariaDB 10.4 / PostgreSQL 11.x
    Nextcloud 16.x
    NGINX 1.17.x
    TLS v. 1.3
    PHP 7.3.x
    Redis-Server
    self signed or Let’s Encrypt SSL (acme.sh)
    UFW (22, 80, 443)

Ready to go (?) … let’s start.

Carsten Rieger: https://www.c-rieger.de


# Short example for Ubuntu 18.04 LTS
Copy and paste:

    sudo -i
    apt purge mariadb* mysql* postgresql* nginx* php* redis* -y && apt autoremove -y
    rm -R /var/www/nextcloud
    apt update && apt upgrade -y && apt install git -y

Then copy and paste this:

    cd /usr/local/src
    git clone https://github.com/criegerde/install-nextcloud.git
    cd install-nextcloud
    find /usr/local/src/install-nextcloud -type f -name "*.sh" -exec chmod 0755 {} \;
    ./install-nextcloud-mariadb-ubuntu.sh

More info at https://www.c-rieger.de/nextcloud-using-one-shell-script/
