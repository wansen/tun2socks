# README

## How to use it?

```
# install golang 1.9+, becase of sync.Map
cp config.example.ini config.ini
# edit it for free
sudo go run cmd/main.go --config=config.ini
```

## Support operating system.

* [x] macOS
* [x] linux
* [x] windows 10 support with [tap-windows6](https://github.com/OpenVPN/tap-windows6)
* [x] Raspberry Pi support
* [x] android support with root

## Hot reload config with `USR2` signal. Not support windows.

Support `route`, `udp.proxy`, `proxy`, `pattern` and `rule`, see [config.example.ini](https://github.com/FlowerWrong/tun2socks/blob/master/config.example.ini).

```bash
sudo kill -s USR2 $PID
```

NOTE: `go run` not support kill command signal.

## TODO

* [ ] ipv6 support
* [ ] set and reset dns server to `127.0.0.1` automatically on windows, Raspberry Pi and android with shell

## Thanks

* thanks [xjdrew/kone](https://github.com/xjdrew/kone) for dns fake mode
* thanks [yinghuocho/gotun2socks](https://github.com/yinghuocho/gotun2socks) for udp <-> socks5 tunnel
* thanks [songgao/water](https://github.com/songgao/water) for tun io on many platform
* thanks [google/netstack](https://github.com/google/netstack) for tcp/ip stack
* thanks [google/gopacket](https://github.com/google/gopacket) for pack/unpack ip package
* thanks [miekg/dns](https://github.com/miekg/dns) for dns parser and server
