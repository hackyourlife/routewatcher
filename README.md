Routewatcher
============

This tool watches IP adresses by continuously resolving DNS names. These
addresses are then routed via the default gateway. This does not look useful?
By itself, it is not useful. But if you use it in conjunction with a dynamic
routing protocol (e.g. OSPF) and redistribute static routes, you can easily
avoid geo blocking with this. Of course, you have to make sure, that names are
resolved via the same host, because it could happen, that addresses are based
on the geographic location. If you use a resolver, you can redirect specific
domains by using a “forwarder”.

Usage
-----

Edit `domains.json` to include all the domains you want to watch.

```
su -c ./routewatcher
```
