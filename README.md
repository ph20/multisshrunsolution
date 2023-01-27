# Solution for multirun command on remote hosts through ssh
## Task
Run user-selected command on many servers (user-provided as param) with ssh in parallel, collect output from all nodes. The script should print collected output from all nodes on stdout, w/o using temp files.
## Solution
### Installations
#### Install pssh
```bash
sudo apt-get install pssh
```

### Usage
put credentials in `hosts.pssh` file
```bash
$ cat ./hosts.pssh 
uptime@bob.sysadmin.pm:2222
uptime@alice.sysadmin.pm:2222
```
run command on remote hosts
```bash
$ pssh -h hosts.pssh -i uptime
```


