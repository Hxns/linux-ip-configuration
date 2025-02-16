# Configuración de IP para VM en Debian y Kali

## Debian

### 1. Acceder al fichero correspondiente.

```bash 
sudo nano /etc/netplan/50-cloud-init.yaml
```

### 2. Modificar el fichero.

```yaml
network:
    ethernets:
        enp0s3:
            dhcp4: false
            - 192.168.56.105/24
```

## Kali

### 1. Acceder al fichero correspondiente.

```bash
sudo nano /etc/network/interfaces
```

### 2. Modificar el fichero.

```ini
auto eth0
iface eth0 inet static
address 192.168.56.101
netmask 255.255.255.0
gateway 192.168.56.1
```
