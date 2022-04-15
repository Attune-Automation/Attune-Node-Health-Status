# Using Attune to dump vital health status to Attune's running log on popular Linux distributions

In this blueprint, we will use common commands to check the health status of the system, print the commands' output to `stdout`(they will be directed to Attune's running log -- can be seen in real time when a job is executing, or from `Jobs -> history` interface afterwards) .  
The main purpose of this blueprint is to let other blueprints inspect the results of this one, and create health report etc. accordingly.  So, it's used as the beginning(data generation / gathering) of a data processing pipeline.  
Users can also learn from this blueprint the commands used to check heath status of Linux.  

This has been tested on Ubuntu 20.04.2 LTS / Debian 11.0.0 / CentOS 8

## Pre-Blueprint Attune setup

1. On the Inputs tab, create a Linux node for the host you wish to check health status.
1. On the Inputs tab, create a Linux credential to connect to the host you wish to check health status.
1. On the Inputs tab, create a Linux credential with `Sudo To root` set to connect to the host you wish to check health status. This is required for some health check commands to successfully run, and also needed for installing packages when command not found.