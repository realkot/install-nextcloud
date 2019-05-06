# install-nextcloud
Scripts to install and optimize Nextcloud (based on Ubuntu 18.04 or Debian Stretch 9.x 64Bit) with NGINX, MariaDB or PostgreSQL, PHP 7.3, Redis-Server, fail2ban, ufw and self signed or Let's Encrypt certificates

    (1) Build your self hosted Nextcloud server on either Ubuntu or Debian with
        a) MariaDB
        b) PostgreSQL
    (2) (optionally only) Request your ssl certificate from Let’s Encrypt
    (3) Additional scripts (for Ubuntu and Debian) to maintain your Nextcloud server

The scripts called install-nextcloud-<database>-debian.sh and install-nextcloud-<database>-ubuntu.sh will install your self hosted Nextcloud within 10 minutes, fully prepared for Ubuntu 18.04.x or Debian 9.x Stretch environments and will consist of:

    Fail2Ban (Nextcloud and SSH jails)
    MariaDB 10.3 / PostgreSQL 11.x
    Nextcloud 16
    NGINX 1.15
    TLS v. 1.3
    PHP 7.3
    Redis-Server
    self signed or Let’s Encrypt SSL using the second script
    UFW (22, 80, 443)

Ready to go (?) … let’s start.

Carsten Rieger // https://www.c-rieger.de
