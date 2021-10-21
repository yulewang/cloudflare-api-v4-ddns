Cloudflare API v4 Dynamic DNS Update in Bash, without unnecessary requests
Now the script also supports v6(AAAA DDNS Recoards)

```
bash <(curl -Ls https://git.io/cloudflare-ddns) -k cloudflare-api-key \
 -h host.example.com \     # fqdn of the record you want to update
 -z example.com \          # will show you all zones if forgot, but you need this
 -t A|AAAA                 # specify ipv4/ipv6, default: ipv4
```
