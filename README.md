wcache
======

This shell script is intended to be used as a lightweight proxy. It will cache the resources it downloads for faster or offline future accesses.
For example when setting up provisioning scripts for Vagrant, you may require download of large files. This is annoying when you are developing these scripts
as large file download means slow tests. If you use a small lightweight proxy like *wcache*, you may save the download time, and even work offline.

Usage
=====

First start up a *wcache* instance on port 9090 with the `start`command

```
$ wcache start 9090	
```

You may check the status of your running *wcache* instance with the `status`command.

```
$ wcache status
```

should return something like this
`7312 9090`
The first column is the PID of the wcache instance, the second is the port it is listening to.

Finally, when you are done using wcache, you may use the `stop`command to shut down an instance you have previously started. For
example, assuming you have previously started an instance on port 9090 with the `start`command, you would shut it down like this:

```
$ wcache stop 9090
```

There are more commands available for monitoring wcache. Run *wcache* without argument or use the `help` command to check them all.
