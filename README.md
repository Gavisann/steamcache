# steamcache
Cache steam games using nginx

**Introduction**

These config files configure nginx to be a fairly quick caching proxy to make downloading games multiple times less WAN intensive

***Usage***

0. Install nginx
1. Place the nginx.conf in /etc/nginx/
2. Place the nginx-steam-cache.conf in /etc/ngnix/conf.d/
3. Restart nginx

You will need to configure your client(s) DNS to direct requests for *.steamcontent.com to your nginx server. This can be done with dnsmasq or a host override on your DNS server of choice. 

**Is it working?**

Use the following command to see if subsequent game downloads being sourced from cache (HIT):
> tailf /var/log/nginx/steamcontent.access.log
