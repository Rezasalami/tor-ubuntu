# tor-ubuntu
```sh
sudo apt-get install tor 
sudo apt-get install obfs4proxy
```
 ```sh
sudo systemctl enable tor.service
```
 ```sh
vim /etc/tor/torrc
```
 ```sh
UseBridges 1  
ClientTransportPlugin obfs4 exec /usr/bin/obfs4proxy 
```

 ```sh
bridges.torproject.org
```

 ```sh
bridges@torproject.org
```

 ```sh
UseBridges 1   
ClientTransportPlugin obfs4 exec /usr/bin/obfs4proxy

Bridge scramblesuit 94.242.249.2:51385 6DA5550F16BA8E6ED180299C6E2C1F352FCA2C61 password=MRFIF5OX43AQ6MZ3TNLXOXKQUQK7LKIS

Bridge fte  192.40.56.94:443 0BCF64A49F111414EA1CE6D7938019E0198A41D5


Bridge obfs4 49.176.248.3:8081 1ABFF076E7C78D965D54A32B00FCA6C28E8DF0C9 cert=dw3mJqKOA3HUH85i7cEUOev9TpjWHdrsApyXwflgvQSU7MyZt782FAs4//C7CACKyI0rIA iat-mode=0

HTTPTunnelPort 6524
```

 ```sh
sudo systemctl start tor@default.service 
sudo systemctl restart tor@default.service
```

 ```sh
systemctl status tor@default.service
journalctl -exft Tor|grep -i done
```

 ```sh
torsocks
source torsocks on
source torsocks off
```
 ```sh
wget -qO - https://api.ipify.org; echo
```
