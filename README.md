# dart-portscanner

This is a port scanner written in Dart; it scans a given list of IP and port ranges for open sockets, and reports back.

## Usage

Scan a single IP:

```bash
dart portscanner -p80,8000-8080 127.0.0.1
```

This will scan 127.0.0.1 for open ports on port 80, and 8000 through 8080.

Scan an IP range (using [CIDR notation](http://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)):

```bash
dart portscanner -p22 10.0.0.0/24
```

This will scan IPs from 10.0.0.0 through 10.0.0.255 for an open port 22 (SSH).

## FAQ

**Uh, why Dart?**

I wrote this utility as an exercise to help learn Dart and the Dart ecosystem (unit testing, pub, etc). It's probably terrible.

**Should I actually use this?**

As a Dart library to help find local open ports? Sure.

As a utility for finding open ports on a LAN? I guess you could.

As a tool for scanning the public internet? Definitely not. Try [masscan](https://github.com/robertdavidgraham/masscan) instead.