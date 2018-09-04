# Xonotic Startup Scripts (1.0.0)
Startup scripts for the Xonotic FPS game - uses the "screen" command to manage session. This also restarts the Xonotic process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/XonoticStartup) - [Official Forum](https://minecity.online/index.php/forum/startup-scripts)  - [Official Download Area](https://minecity.online/index.php/downloads/category/5-server-tools)

---
These start up the Xonotic server at boot time with a "screen" process.

1. Copy **xonotic** into **/etc/init.d** - make sure it is executable
2. Copy **startxonotic** into **/root/Xonotic** - make sure it is executable
4. Run "**systemctl enable xonotic**" (only needed once, will stick)
5. Run "**systemctl start xonotic**" - starts Xonotic without restarting the server

When you want to view the Xonotic console, just enter "**screen -r**" in your shell.

To disconnect from the Xonotic console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /usr/local/minetest/nostart**". To reenable it type "**rm /usr/local/minetest/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
