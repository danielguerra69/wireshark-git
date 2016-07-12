##Wireshark git version.

The leading tool, wireshark from the git repository.

https://www.wireshark.org

Debian jessie based docker image for wireshark development.
Contains fully working wireshark + development libraries.

#Basic usage
```bash
docker run -ti -v mypacapdir:/pcap danielguerra/wireshark-git
```

#X on local host


#Elasticsearch output to stdout
```bash
docker run -ti -a stdout -v mypacapdir:/pcap danielguerra/wireshark-git tshark -r /pcap/test.pcap -T ek
