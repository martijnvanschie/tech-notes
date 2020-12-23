# Setup Docker

## Get Repo

## Install Docker Engine

https://docs.docker.com/engine/install/ubuntu/

## Install Docker Compose

Just get it from the repo

```bash
sudo apt install docker-compose
```

https://github.com/docker/compose/issues/6831#issuecomment-634866527

# Setup Pi-hole

## Disable DNS Resolve

I used WinSCP to set the value for `DNSStubListener` to `No` and then uncomment it.  
Then i ran the commands from the page below

```bash
sudo sh -c 'rm /etc/resolv.conf && ln -s /run/systemd/resolve/resolv.conf /etc/resolv.conf'
systemctl restart systemd-resolved
```

https://github.com/pi-hole/docker-pi-hole#installing-on-ubuntu
