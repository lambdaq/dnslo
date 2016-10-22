DNSLO
=====

DNS is always SLOw, so I made it run on [LOopback](https://en.wikipedia.org/wiki/Loopback)



## NIH

I want a single file script to run on my loopback as a DNS resolver.

 - It caches A/AAAA records using oldschool Sqlite3. Other types are pass-thru
 - Always returns the last-known good DNS record first.
 - When TTL is met, a background task will update the record automatically.
 - It keeps a track of history


## Goals that might be planned to add to to-do list in the ∞ future or never:

 - AS binding and EDNS extension
 - DNSCrypt or DNSCurve or other complex shit
 - sort records by network RTT
 - HTTP DNS, [why is it even a thing?](https://developers.google.com/speed/public-dns/docs/dns-over-https)
 - multi, global DNS resolver aggregation.

 ## License

 GPLv3. yeah suck it bitches.