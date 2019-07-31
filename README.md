# Megamek Startup Scripts (1.0.0)
Startup scripts for the MegaMek game server software - uses the "screen" command to manage the session. This also restarts the Megamek server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/MegamekStartup) - [Official Forum](https://mymegamek.mekcity.com/index.php/forum/our-server-tools)

---

These start up the MegaMek server at boot time with a "screen" process.

1. Copy **megamek** into **/etc/init.d** - make sure it is executable
2. Copy **startmegamek** into **/root/megamek** - make sure it is executable
3. Copy **MegaMekProcess** into **/root/megamek** - make sure it is executable
4. Run "**systemctl enable megamek**" (only needed once, will stick)
5. Run "**systemctl start megamek**" - starts MegaMek server without restarting the OS.

When you want to view the Megamek console, just enter "**screen -r**" in your shell.

To disconnect from the Megamek console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/megamek/nostart**". To reenable it type "**rm /root/megamek/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
