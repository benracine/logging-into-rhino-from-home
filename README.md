logging-into-rhino-from-home
============================

How to log into rhino from home

I think that in order to log into rhino from home that you will need to tell your mac a little bit more about what rhino really is. 

This is done by editing the `~/.ssh/config` file aka `/Users/kitcurtius(sp?)/.ssh/config`. Use sublime for this I suppose. 

Copy and paste the following into the bottom of that file. Caveat: if this file doesn't exist, you'll have to create this folder and this file (notes: `cd` alone returns you to ~ aka /Users/kitcurtius, `mkdir .ssh` makes a .ssh directory, `cd .ssh` moves you into the `.ssh directory`, and `touch config` makes a config file). 

  Host rhino              # rhino is a handy alias name 
  HostName 192.168.1.45   # the number is the IP address of the machine, I don't know what it really is  
  Port 2222               # very unlikely to be a different port number, this is the de facto port number for ssh connections 
  
And edit the IP address on line #2 to be whatever IT tells you it is or whatever you can find on the (nonfunctioning :( ) documentation.

Then I would think you could ssh in from home... though there might be more to it, e.g. some "tunneling" or something that I would need to look up.