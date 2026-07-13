# Duranta OpenAirInterface RAN with free5GC

![alt text](./images/image.png)


## Official Guide by free5GC

Check [here](https://free5gc.org/blog/20260622/20260622/)

### Set static IP addres for free5GC

SSH into free5GC VM and run:
```bash
cat << EOF > /etc/netplan/10-custom.yaml
network:
  version: 2
  ethernets:
    ens4:
      dhcp4: no
      addresses:
        - 192.168.56.101/24
EOF
```

Apply the config:
```bash
sudo netplan apply
```

### Set static IP addres for oai-ran

SSH into oai-ran VM and run:
```bash
cat << EOF > /etc/netplan/10-custom.yaml
network:
  version: 2
  ethernets:
    ens4:
      dhcp4: no
      addresses:
        - 192.168.56.102/24
EOF
```

Apply the config:
```bash
sudo netplan apply
```


## Step by Step Tutorial

Check [here](https://youtu.be/6pgaYMKKGu4)
