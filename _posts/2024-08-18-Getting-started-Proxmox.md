## Getting started Proxmox

Well today I decided to try out my old computer which was lying around. I had been procrastinating this for almost a year now.

I had few basic ideas which I knew I wanted to do.

- Hardware
- Networking
- Software

### Hardware

I had my old cpu which was Intel Core 2 Quad Q6600. I don't know how good this will be but I had to try. My rig has 4 GB ram ddr2 and no hard disk. I have an extra 80 GB hard disk but my old case doesn't have a hard disk caddy. I connected them and placed it on top.

![](/assets/20240818_175015.jpg)

And the only monitor that has the right connector for it

![](/assets/20240818_175051.jpg)

### Network

Now after that I needed ethernet. The router is on the first floor so I had to get my old router and set it up in Bridge Mode to act as a extender. This also gave me better download and upload speeds. I connected both my home pc and the homelab (V1) with it.

https://phoenixnap.com/kb/install-proxmox

This guide for reference if needed ^

For running `apt-get update` I ran into issues where it had enterprise repositories set, got it fixed by commenting out the lines in the list.

![](lol1.png)

The enterprise repository lives in:

```
/etc/apt/sources.list.d/pve-enterprise.list
```

https://pve.proxmox.com/wiki/Package_Repositories

Use the web interface, go to Node -> Updates -> Repositories menu and you should be able to add/remove package repositories easily and disable pve-enterprise component. Alternative approach.

![](lol2.png)

After that I have setup a VM, obviously downloaded kali-linux.

![](lol3.png)
