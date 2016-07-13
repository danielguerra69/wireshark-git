###Wireshark git version.

The leading tool, wireshark from the git repository.

https://www.wireshark.org

Debian jessie based docker image for wireshark development.
Contains fully working wireshark + development libraries.

###Basic usage
```bash
docker run -ti -v mypacapdir:/pcap danielguerra/wireshark-git
```

###X on local host
```bash
docker run -ti --net=host --privileged -v $HOME:/root:ro -e XAUTHORITY=/root/.Xauthority -e DISPLAY=$DISPLAY danielguerra/wireshark-git wireshark
```

###Elasticsearch output to stdout
```bash
docker run -ti -a stdout -v mypacapdir:/pcap danielguerra/wireshark-git tshark -r /pcap/test.pcap -T ek | curl -s -XPOST elasticsearch:9200/_bulk --data-binary @-
```
