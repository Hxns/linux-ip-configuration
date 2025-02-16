# Configuración de IP para maquinas virtuales Debian y Kali

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

