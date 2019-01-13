# meta-wrapper
Routes SSL traffic through port 443 without requiring the certs.

Ever wanted to host several HTTPs apps on the same IP? Common solutions mean running them HTTP unwrapped and using a single app to encrypt (nginx, apachemodproxy, etc), meta-wrapper uses sniproxy to connect to your favourite HTTPS enabled app and without the need of passing the master certs for each domain (as long as they DO match the request).

Uses sniproxy so you'll need a list of ports and routes. Check out a [default sniproxy config](https://github.com/steamcache/sniproxy/blob/master/overlay/etc/sniproxy.conf)

Run via ```docker-compose up```

Requires:
* Docker
* docker-compose that at least parses v3

