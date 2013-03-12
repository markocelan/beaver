======
Beaver
======

python daemon that munches on logs and sends their contents to logstash

NOTE
============

This repositories is forked from https://github.com/josegonzalez/beaver. There is lovely tutorial how to use beaver.
Here I'll try to cover new/different stuff.

Installation
============

Using PIP:

From Github::

    pip install git+git://github.com/markocelan/beaver.git#egg=beaver

Usage
=====

usage::

    beaver [-h] [-c CONFIG] [-d] [-D] [-f FILES [FILES ...]]
            [-F {json,msgpack,string,raw,__rawjson__}] [-H HOSTNAME] [-m {bind,connect}]
            [-l OUTPUT] [-p PATH] [-P PID]
            [-t {rabbitmq,redis,stdout,zmq,udp}] [-v] [--fqdn]

optional arguments::

    -h, --help            show this help message and exit
    -c CONFIG, --configfile CONFIG
                          ini config file path
    -d, --debug           enable debug mode
    -D, --daemonize       daemonize in the background
    -f FILES [FILES ...], --files FILES [FILES ...]
                          space-separated filelist to watch, can include globs
                          (*.log). Overrides --path argument
    -F {json,msgpack,string,raw,__rawjson__}, --format {json,msgpack,string,raw,__rawjson__}
                          format to use when sending to transport
    -H HOSTNAME, --hostname HOSTNAME
                          manual hostname override for source_host
    -m {bind,connect}, --mode {bind,connect}
                          bind or connect mode
    -l OUTPUT, --logfile OUTPUT, -o OUTPUT, --output OUTPUT
                          file to pipe output to (in addition to stdout)
    -p PATH, --path PATH  path to log files
    -P PID, --pid PID     path to pid file
    -t {rabbitmq,redis,stdout,zmq,udp}, --transport {rabbitmq,redis,stdout,zmq,udp}
                          log transport method
    -v, --version         output version and quit
    --fqdn                use the machine's FQDN for source_host


Upgrades
========
  New format 'rawjson'.

Usage
=======
  If you configure your logs as per http://blog.pkhamre.com/2012/08/23/logging-to-logstash-json-format-in-nginx/ or similar,
  you want to deliver parsable JSON to logstash. 'rawjson' enables you to do that.


Credits
=======

    Original project: https://github.com/josegonzalez

    License: MIT
