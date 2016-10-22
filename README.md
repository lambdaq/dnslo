DNSLO
=====

DNS is SLOw, so cache it on [LOopback](https://en.wikipedia.org/wiki/Loopback)

## NIH

I always want a single file Python script to run on loopback as a caching DNS resolver. Because [DDoS from IoT broke the Internet](https://news.ycombinator.com/item?id=12759697).

 - It caches A/AAAA records using oldskool Sqlite3. Other types are pass-thru
 - Always returns the last-known good DNS record first. (In case o)
 - When TTL is met, a background task will update the record automatically. To achieve zero lag resolving. Everything is queried from SQLite3 directly. (Well of course except the first request.)
 - It keeps a track of history DNS changes


## Goals that might be planned to add to to-do list in the ∞ future or never:

 - AS binding and EDNS extension
 - DNSCrypt or DNSCurve or other complex shit
 - sort records by network RTT
 - HTTP DNS, [why is it even a thing?](https://developers.google.com/speed/public-dns/docs/dns-over-https)
 - multi, global DNS resolver aggregation
 - Replace system DNS cache automatically
 - Grab DHCP DNS, ISP default on the fly
 - Distinguish well-known CDNs for extra speed-ups
 - Really trying to ping or 80/443 TCP connect the results for fastest host. 

 ## License

 GPLv3. yeah suck it bitches.