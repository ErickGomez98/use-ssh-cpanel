# Simple steps to connect to a server (it shouldn't matter if it has cPanel or not) using an ssh key

First you have to generate an ssh key in your local computer a.k.a your development computer
 1. Generate a key pair using the following command:
 `ssh-keygen -t rsa -b 4096 -C "your@email.com"` it will ask where you want to store the key, and also if you want to use a passphrase.
 
 2. Once the key pair is generated, the next thing that you should do is copy the generated key to the server you are trying to connect, you can use the following command: 
 `ssh-copy-id user@server.com` then it will ask you the password to log into the server using the specified account, then if everything went ok you now should be able to connect to the server using the pub key that you just generated.
 
 3. To connect to the server simply use `ssh user@server.com` and it should connect, you could also specify the location of the pub key using the following command: `ssh -i  /location/of/the/key/id_rsa.pub user@server.com`
 
 That's pretty much it :)
