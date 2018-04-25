# IRC Server for Raspberry Pi (no ident needed)

>For our first project we were tasked with creating an IRC server; IRC stands for Internet Relay Chat. IRC is an application layer protocol that uses text as a form of communication using a client/server networking model. The Pi will act as the server that forwards text messages to clients using the servers’ resources. Opensource software will make this not only inexpensive, but easier since those in the opensource community set up configuration files with comments for easy customization of the security, name, and more on. 

# Installaton of 'ircd-hybrid'
> First was the installation of a client to manage the server itself, ‘ircd-hybrid’ is an opensource program obtained through apt-get as seen below.

```sh
sudo apt-get install ircd-hybrid
```

# Navigate to the config file
> Once installed there are changes that can be configured in the configuration file, accessible by the command below.
```sh
sudo nano /etc/ircd-hybrid/ircd.conf
```
###### Change features as you wish
# I used 'vim' to make my changes

> I changed the lines below as follows:
```sh
default_max_clients = 7;
```
```sh
max_nick_length = 15;
```
>The lines above allowed me to modify the number of users to 7 and allow only 15< as nickname length for the chat

# Commit the changes
> If you used 'vim' you can now enter ":wq!" to write the contents to the conf file and quit the 'vim' editor

#  Restart 'ircd-hybrid'
```sh
sudo /etc/init.d/ircd-hybrid restart
```
 
>Once the restart is over you can run your preferred IRC chat client from your PC; I will be using mIRC for Windows. The set up of the IRC client I will not discuss but do note the IP address of your Pi is needed for server setup within your IRC chat client. 
