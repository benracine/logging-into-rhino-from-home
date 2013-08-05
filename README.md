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

- Copy and paste the following into the bottom of that file. 

```
Host rhino              # rhino is a handy alias name 
HostName 192.168.1.45   # the number is the IP address of the machine, I don't know what it really is  
Port 2222               # very unlikely to be a different port number, this is the de facto port number for ssh connections 
```

- Edit the IP address on line #2 to be whatever IT tells you it is.

### This is a very brief first pass that will likely need to be refined.
Then I would think you could ssh in from home... though there might be more to it, e.g. some "tunneling" or something that I would need to look up.