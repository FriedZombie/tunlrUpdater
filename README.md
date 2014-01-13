Simple scripts to update tunlr gatekeeper stuff


Because I'm sometimes blessed with an changing ip address I wrote this nice script, it will function on most Linux systems and OpenWrt/GarGoyle
Also the tunlr team is going to add an API to do the same thing, when this happens I adapt my scripts accordingly :)
A good thing to have for the API would be the option to use a none https link, since wget from BusyBox doesn't support ssl.

To run the script simply get https://raw.github.com/FriedZombie/tunlrUpdater/master/gatekeeper/gatekeeperUpdate
and make the downloaded file executable and change the settings in the script itself to suit your needs.
When the script is ran, it updates your public ip to tunlr gatekeeper.

To use/install tunlrupdater on OpenWrt copy and paste the following command in the cli:
wget http://goo.gl/vmTCAz -O /tmp/instTunlr && chmod +x /tmp/instTunlr && /tmp/instTunlr

To uninstall the update scripts from OpenWrt, simply run the following commands in the cli:
rm /sbin/gatekeeperUpdate
rm /etc/hotplug.d/iface/80-gatekeeperUpdate
opkg remove wget 

p.s. The OpenWrt setup script is split into two parts and the first part uploaded to a pastebin clone, simply because github only uses https and the default wget of OpenWrt doesn't support that. this way it is easier to use and it is still easy to update the scripts.
