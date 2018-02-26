# Bluetooh Cheatsheet

## Find bluetooth interfaces

`sudo hcitool dev`

## Scan devices

`sudo hcitool lescan`

## Query device services and characteristics

`sudo gatttool -i [hciX] -b [ble-address] -I`
`connect`
`primary`
`char-desc`
`char-read-hnd <handle>`
`char-write-req <handle> <data>`
`char-write-req 0x000f 0000`

## Ubertooth

### Scan

`ubertooth-scan -s -x`

### Sniff

`mkfifo /tmp/pipe`
`ubertool-btle -f -c /tmp/pipe` -- see packets in wireshark by pointing to named pipe
