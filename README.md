Configuration system for the SMB servers
========================================

Server configurations system designed to simplify and easily maintain server configs  
While this is designed for the SMB servers, it may be used on any server that dares to use it



Requirements
============

Git - http://git-scm.com/book/en/v2/Getting-Started-Installing-Git


Usage
=====

Run the following command from your server's data folder (~/.xonotic/data on Linux/Mac, C:\Users\username\Saved Games\xonotic\data on Windows):  
		git clone https://github.com/MarioSMB/configs.pk3dir  
Copy the server_mod.cfg file into xonotic/data/configs on your server (exact directory can be found in previous step)  
Modify the new copy of server_mod.cfg to suit your needs  
Run server to make sure everything is working   


Multiple Servers
================

Running multiple servers on a single machine? No problem! Follow the below steps to make sure this system is working on all of them  

NOTE: This guide is for servers which use the recommended multi-server setup (starting the game with -game data_otherserver to separate the game data between servers)  
If your server is running multiple servers from the same data folder, please refer to the Unrecommended Multiple Server Setup section below  

Follow regular usage steps to get the configs.pk3dir folder into your main data folder (not the per-server data folder)  
Copy server_mod.cfg to your per-server data/configs folder (e.g. xonotic/data_otherserver/configs)  
Modify the copy to suit your needs  


Unrecommended Multiple Server Setup
===================================

For running multiple servers in the same data directory  
NOTE: If you are using separate data directories per server, please read the Multiple Servers section instead  

Follow the regular steps to get the configs.pk3dir folder into your data folder  
Copy both server_multi.cfg and server_mod.cfg into your data folder  
Rename server_mod.cfg to something like server_otherserver_mod.cfg then move it to data/configs  
Rename server_multi.cfg to something like server_otherserver.cfg  
Edit server_otherserver.cfg and change _server_multi to otherserver (using the actual server name here and in config names, of course)  
Make sure your server points to server_otherserver.cfg by using +serverconfig server_otherserver.cfg when you start the server binary  


Updating
========

Change to the configs.pk3dir directory on your server (cd ~/.xonotic/data/configs.pk3dir on Linux/Mac, cd "Saved Games"\xonotic\data\configs.pk3dir on Windows)  
Run the following command (method here may differ on Windows servers, a GUI like TortoiseGit can make things easier): git pull  
If you see any changes to server_mod.cfg, you may look through the file and copy anything new to your modified copy 



If you have any questions or problems, don't be afraid to ask us on IRC at http://webchat.quakenet.org/?channels=smb  