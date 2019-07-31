# Nexuiz Startup Scripts (1.0.0)
Startup scripts for the Nexuiz game server software - uses the "screen" command to manage the session. This also restarts the Nexuiz server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/NexuizStartup)

---

These start up the Nexuiz server at boot time with a "screen" process.

1. Copy **nexuiz** into **/etc/init.d** - make sure it is executable
2. Copy **startnexuiz** into **/root/Nexuiz** - make sure it is executable
3. Run "**systemctl enable nexuiz**" (only needed once, will stick)
4. Run "**systemctl start nexuiz**" - starts Nexuiz server without restarting the OS.

When you want to view the Nexuiz console, just enter "**screen -r**" in your shell.

To disconnect from the Nexuiz console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/Nexuiz/nostart**". To reenable it type "**rm /root/Nexuiz/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
