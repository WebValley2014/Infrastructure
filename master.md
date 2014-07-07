# master server

## General info

- IP: 54.72.200.168
- Instance type: t1.small

## Python package

### Installed with apt

- numpy == 1:1.8.1-1ubuntu1
- django == 1.6.1-2
- django-jsonfield == 0.9.12-2
- pil == 2.3.0-1ubuntu3

### Installed with pip

- celery == 3.1.12
- django-celery == 3.1.10

## RabbitMQ

Installed with apt: 3.2.4-1

### Credential

- user: wvlab
- pass: ******

## NFS

### /etc/default/nfs-common

    STATDOPTS="--port 49151 --outgoing-port 49152"

### /etc/default/nfs-kernel-server

    RPCMOUNTDOPTS="--manage-gids --port 49150"

### /etc/modprobe.d/lockd.conf

    options lockd nlm_udpport=49153 nlm_tcpport=49153

## Web

Clone [WebDev repository](https://github.com/WebValley2014/WebDev.git) in /usr/share/WebDev

### gunicorn

Installed with apt: 17.5-2build1

#### upstart config

Locate [gunicorn.conf](gunicorn.conf) in /etc/init

### nginx

Installed with apt: 1.4.6-1ubuntu3

#### nginx.conf

Locate [webdev-nginx](webdev-nginx) in /etc/nginx/sites-available and create symlink in /etc/nginx/sites-enabled
