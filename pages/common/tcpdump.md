# tcpdump

> Dump traffic on a network.

- Capture the traffic of Http Get:

`tcpdump -A -i any -s 0 'tcp dst port 80 and tcp[((tcp[12]>>4)<<2):4]=0x47455420'`

- Capture the traffic of Http Post:

`tcpdump -A -i any -s 0 'tcp dst port 80 and tcp[((tcp[12]>>4)<<2):4]=0x504F5354'`

- Capture the traffic of Http Response:

`tcpdump -A -i any -s 0 'src host {{10.96.153.226}} and tcp[((tcp[12]>>4)<<2):4]=0x48545450'`

- List available network interfaces:

`tcpdump -D`

- Capture the traffic of a specific interface:

`tcpdump -A -i {{eth0}}`

- Capture all traffic except traffic over port 22 and save to a dump file:

`tcpdump -w {{dumpfile.pcap}} not port {{22}}`
