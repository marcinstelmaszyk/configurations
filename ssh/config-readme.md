
## Easy connection to a machine
Simplify ssh connnection to another machine to just the following command:
```zsh
ssh <shortname>
```

### Configuration

Create a file `~\.ssh\config` with the following content:
```sshconfig
Host <shortname>
    HostName <host_address>
    User <username_on_host>
    RemoteCommand cd <dir_on_host> && <shell_name>
    RequestTTY yes
    IdentityFile ~/.ssh/id_rsa
```
### Example:

Command used to connect: `ssh host`
```sshconfig
Host host
    HostName heeps-tir.gmv.es
    User mast
    RemoteCommand cd /home/mast/repos/heeps-tir && zsh
    RequestTTY yes
    IdentityFile ~/.ssh/id_rsa
```
