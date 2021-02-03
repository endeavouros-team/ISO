# ISO For EndeavourOS

[![Maintenance](https://img.shields.io/maintenance/yes/2021.svg)]()  [![Downloads](https://img.shields.io/github/downloads/endeavouros-team/ISO/total)]()

[EndeavourOS download page](https://endeavouros.com/latest-release)

[Release archive](https://github.com/endeavouros-team/ISO/releases/tag/1-EndeavourOS-ISO-releases-archive)

[Development Releases](https://github.com/endeavouros-team/ISO/releases/tag/0-EndeavourOS-development-ISO-releases)

![Live-Session-Screenshot](https://raw.githubusercontent.com/endeavouros-team/screenshots/master/Live-Session-EndeavourOS.png)

---


**How to handle ISO releases:**

import private key:
`gpg --import private_key_endeavour.gpg`

sign the iso-file:

`gpg --default-key info@endeavouros.com --output endeavouros-2021.02.02-x86_64.iso --detach-sig endeavouros-2021.02.02-x86_64.iso`

verify:

for check:
`gpg  --recv CB23504F`
`gpg --verify endeavouros-2021.02.02-x86_64.iso.sig`

sha512sum creation:

`sha512sum endeavouros-2019.12.03-x86_64.iso > endeavouros-2021.02.02-x86_64.iso.sha512sum`


create torrent:

`mktorrent --announce=udp://tracker.openbittorrent.com:80 -a udp://tracker.torrent.eu.org:451/announce -a udp://thetracker.org:80/announce -a udp://tracker.dutchtracking.com:6969/announce -a udp://tracker.opentrackr.org:1337/announce -c endeavouros-2021.02.02-x86_64.iso -n endeavouros-2021.02.02-x86_64.iso -o endeavouros-2021.02.02-x86_64.iso.torrent -v /path/to/iso/endeavouros-2021.02.02-x86_64.iso -w https://mirror.alpix.eu/endeavouros/iso/endeavouros-2021.02.02-x86_64.iso -p` 
