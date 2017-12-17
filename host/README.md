# Host
All scripts that fall under this category are host-sided scripts. In other words, these scripts
are executed on your PC, not your reMarkable. Host scripts will however in most cases require
connection to your reMarkable, either trough USB or Wireless.

## rezone.sh
> [Source](https://github.com/reHackable/scripts/blob/master/host/rezone.sh)

reZone is a small script that can set the timezone on your reMarkable according to the host, or specified timezone.
This is done trough SSH by replacing the environmental `TZ` variable in `/etc/profile`.

### Usage:
```
Usage: rezone.sh [SSH | -h | -help | --help]

Arguments:
SSH                     Devices SSH address (default 10.11.99.1)
-h -help --help         Displays script usage (this)
```

## repush.sh
> [Source](https://github.com/reHackable/scripts/blob/master/host/repush.sh)

Host sided script that can push one or more provided documents to the reMarkable via the web client. Files can be pushed trough USB, as well as remotely trough the `-r` option

#### Supported document types:

* PDF
* EPUB

### Usage:
```
Usage: repush.sh [-r ip] [-p port] doc1 [doc2 ...]

Options:
-r                      Push remotely via ssh tunneling
-p                      If -r has been given, this option defines port to which the webui will be tunneled (default 9000)
```