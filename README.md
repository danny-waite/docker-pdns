PowerDNS Authoritative server and Poweradmin
===========

This image is available at `https://hub.docker.com/r/dannywaite/powerdns/`

# Running

Just use this command to start the container. PowerDNS will listen on port 53/tcp, 53/udp and 8080/tcp.

```docker compose up```

Login:
``` admin / admin ```

# Configuration
These options can be set:

- **PDNS_ALLOW_AXFR_IPS**: restrict zonetransfers to originate from these IP addresses. Enter your slave IPs here. (Default: "127.0.0.1", Possible Values: "IPs comma seperated")
- **PDNS_MASTER**: act as master (Default: "yes", Possible Values: "yes, no")
- **PDNS_SLAVE**: act as slave (Default: "no", Possible Values: "yes, no")
- **PDNS_CACHE_TTL**: Seconds to store packets in the PacketCache (Default: "20", Possible Values: "<integer>")
- **PDNS_DISTRIBUTOR_THREADS**: Default number of Distributor (backend) threads to start (Default: "3", Possible Values: "<integer>")
- **PDNS_RECURSIVE_CACHE_TTL**: Seconds to store packets in the PacketCache (Default: "10", Possible Values: "<integer>")
- **PDNS_RECURSOR**: If recursion is desired, IP address of a recursing nameserver (Default: "no", Possible Values: "yes, no")
- **PDNS_ALLOW_RECURSION**: List of subnets that are allowed to recurse (Default: "127.0.0.1", Possible Values: "<ipaddr>")
- **POWERADMIN_HOSTMASTER**: default hostmaster (Default: "", Possible Values: "<email>")
- **POWERADMIN_NS1**: default Nameserver 1 (Default: "", Possible Values: "<domain>")
- **POWERADMIN_NS2**: default Nameserver 2 (Default: "", Possible Values: "<domain>")
- **PDNS_API_KEY**: if set, this will enable the powerdns internal webserver on port 8081 and the api. See https://doc.powerdns.com/md/httpapi/README/ for more information.
