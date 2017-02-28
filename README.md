compose-etcd
============

Had a hard time finding one of these.

Prerequisites
-------------

A MacOS installed Docker requires the following

Update hosts file with:

    172.16.238.11 etcd-01
    172.16.238.12 etcd-02
    172.16.238.13 etcd-03

Add aliases

    $ sudo ifconfig lo0 alias 172.16.238.11
    $ sudo ifconfig lo0 alias 172.16.238.12
    $ sudo ifconfig lo0 alias 172.16.238.13

Usage
-----

Start the cluster:

    $ docker-compose up -d

Stop the cluster:

    $ docker-compose down

Verify the cluster's health:

    $ source .env
    $ etcdctl --endpoints ${ENDPOINTS} cluster-health

License
-------

MIT
