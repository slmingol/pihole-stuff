# pihole-stuff

#### [The SNAFU Blocklist](https://github.com/RooneyMcNibNug/pihole-stuff/blob/master/SNAFU.txt):
An ever-evolving blocklist of ads, analytics, tracker, and other domains. Artisinally crafted - attempting to find and include "new" domains that have yet to be added in the default Ublock Origin list(s) or in other popular hosted blocklists.

#### [Latest "Marketing Technology Landscape" Mosaic](https://github.com/RooneyMcNibNug/pihole-stuff/blob/master/martech5000k2020Apr.jpg)
One of the more painful illustrations conveying just how massive the user-targetting industry has become. At least it helps with discovering new domains to enumerate for the blocklist.

#### [Adlists I use](https://github.com/RooneyMcNibNug/pihole-stuff/blob/master/adlists_config.txt)
A compilation of lists I use within different environments, sorted by "type".

#### Python Scripts
A few poorly cobbled together `.py` scripts to find possible URLs to add to the blocklist.

#### Disabling localhost queries in pi-hole/FTL
This forum post describes it a bit [IGNORE_LOCALHOST is ignored](https://discourse.pi-hole.net/t/ignore-localhost-is-ignored/41036). I can confirm this setting:

```
$ cat /etc/pihole/pihole-FTL.conf
PRIVACYLEVEL=0
IGNORE_LOCALHOST=yes
```

Works fine:
```
$ tail -200 /var/log/pihole-FTL.log | grep -i local
[2022-03-07 22:19:35.326 7320M]    SOCKET_LISTENING: only local
[2022-03-07 22:19:35.326 7320M]    IGNORE_LOCALHOST: Hide queries from localhost
[2022-03-07 22:19:35.327 7320M]    LOCAL_IPV4: Automatic interface-dependent detection of address
[2022-03-07 22:19:35.327 7320M]    LOCAL_IPV6: Automatic interface-dependent detection of address
```

### Main docs for pi-hole
These are here:
 - [Main Docs](https://docs.pi-hole.net/)
 - [FTLLLDNS Configuration File](https://docs.pi-hole.net/ftldns/configfile/)
