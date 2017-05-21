openwrt-tor
===========

configure tor aspects of your openwrt system.

Dependencies
------------

* python installed (in ram at least)

Role Variables
--------------

| variable name     | type   | description/structure                | default |
|-------------------|--------|--------------------------------------|---------|
| dns_port          | number | DNS server port                      | 9053    |
| proxy_port        | number | Tor proxy port                       | 9040    |
| socks_port        | number | Tor socks proxy port                 | 9050    |
| server_address    | text   | tor server ip address                | 192.168.2.1 |
| network_address   | text   | tor network ip address               | 192.168.2.0/24 |
| torrc_path        | text   | absolute path of the torrc config file | /etc/tor/torrc |
| tor_data_directory_path | text | absolute path of tor data directory | /var/lib/tor  |
| tor_log_directory_path  | text | absolute path of tor logging directory | /var/log/tor |
| tor_pid_file_path       | text | absolute path of tor pidfile           | /var/run/tor.pid |

Example Playbook
----------------

```  
    - role: openwrt-tor
      dns_port: 5353
      server_address: "192.168.3.1"
      network_address: "192.168.3.0/24"
```
