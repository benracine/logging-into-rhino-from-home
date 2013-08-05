# Logging into Rhino from home

### Useful terminal commands:
- `cd` -> [__C__hange the shell working __D__irectory](http://linuxcommand.org/lc3_man_pages/cdh.html)
- `ls` -> [__L__i__S__t directory contents](http://linux.die.net/man/1/ls)
- `mv` -> [__M__o__V__e (rename) files](http://linux.die.net/man/1/mv)
- `pwd` -> [__P__resent __W__orking __D__irectory](http://linux.die.net/man/1/pwd)

### Some aliases
- `..` -> parent directory
- `.` -> current directory
- `~` -> "home" directory

### The action

I think that in order to log into rhino from home that you will need to tell your mac a little bit more about what rhino really is. I am probably bungling your usernames throughout. This is done by:

- Editing the `~/.ssh/config` file also known as `/Users/kitcurtius/.ssh/config` (use sublime for this I suppose).

- Copy and paste the following into the bottom of that file if it exists. You'll need to create it if it doesn't, skip ahead to the next step for that.

```
Host rhino              # rhino is a handy alias name 
HostName 192.168.1.45   # the number is the IP address of the machine. 
                        # I don't know what it really is  
Port 2222               # very unlikely to be a different port number. 
                        # This is the de facto port number for ssh connections 
```

- If you need to create this file:
  - `cd` alone returns you to the home directory = `~` = `/Users/kitcurtius`
  - `mkdir .ssh` makes a `/Users/kitcurtius/.ssh` directory
  - `cd .ssh` moves you into the `.ssh directory`
  - `touch config` makes a config file

- Finally: __Edit the IP address on line #2 to be whatever IT tells you it is.__

### This is a very brief first pass that will likely need to be refined.
There may be some "tunneling" or something that necessary, but I'm curious to see how far this gets your first before going there.