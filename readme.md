# Setup

- run 'docker-compose up -d'
- enter container: 'docker-compose exec tinc sh'
- in container generate client: '/usr/local/bin/peer.sh client 10.20.30.2' (arguments: clientname, client address)
- extract tar file to client

# changes to make ssh on rpi work

- use docker-compose w/ services
- add network_mode: host
- make sure ipv4 forwarding is enabled 'sudo sysctl ipv4.forward' should be 1

# useful commands to check everything worked

- ip route (10.20.30.0/24 dev tun0 scope link should be there)
- netstat -a
