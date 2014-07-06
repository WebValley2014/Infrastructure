# master server

## General info

- IP: 54.72.200.168
- Instance type: t1.small

## Python package

### Installed with apt

- numpy == 1:1.8.1-1ubuntu1

### Installed with pip

- celery == 3.1.12

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
