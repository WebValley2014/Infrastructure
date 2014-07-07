# slave server

## General info

- IP: 54.77.29.115
- Instance type: m3.large

## Python package

### Installed with apt

- scipy == 0.13.3-1build1
- sklearn == 0.14.1-2

### Installed with pip

- celery == 3.1.12
- biom-format == 1.3.1

### Installed with source

- mlpy == [3.5.0](http://downloads.sourceforge.net/project/mlpy/mlpy%203.5.0/mlpy-3.5.0.tar.gz)

#### Installation command

    sudo easy_intall mlpy-3.5.0.tar.gz

## Celery

### Init script

Locate [init script](https://raw.githubusercontent.com/celery/celery/master/extra/generic-init.d/celeryd) in /etc/init.d

### Config

Locate [celeryd](celeryd) in /etc/default

### User

    useradd -d /opt/Pipeline -g celery -s /bin/bash celery

## Biological software

### mothur

Installed with apt: 1.31.2+dfsg-2build1

### qiime

Installed with apt: 1.8.0+dfsg-2

#### Config

Locate [qiime_config](qiime_config) in /etc/qiime and create symlink at /home/ubuntu/.qiime_config and /opt/Pipeline/.qiime_config

#### FastTree

Locate [FastTree](http://www.microbesonline.org/fasttree/FastTree) in /usr/local/bin

#### Greengenes OTU

Locate [13_8](ftp://greengenes.microbio.me/greengenes_release/gg_13_5/gg_13_8_otus.tar.gz) in /usr/share/qiime/gg_13_8_otus

#### Greengenes core

Locate [greengenes core set data file](http://greengenes.lbl.gov/Download/Sequence_Data/Fasta_data_files/core_set_aligned.fasta.imputed) and [greengenes alignment lanemask file](http://greengenes.lbl.gov/Download/Sequence_Data/lanemask_in_1s_and_0s) in /usr/share/qiime/greengenes_core_sets

#### /etc/bash.bashrc

    source /usr/lib/qiime/shell/qiime_environment

## NFS

### /etc/default/nfs-common

    STATDOPTS="--port 49151 --outgoing-port 49152"

## Pipeline

Clone [pipeline](https://github.com/WebValley2014/Pipeline.git) in /opt/Pipeline
