# Servidor web con HTTPD en CentOS

Autor: Franklin Andres Luna Arias

En esta práctica se configura un servidor web en CentOS usando Apache HTTPD y MobaXterm.

## Paso 1. Instalar SSH y el firewall

```bash
sudo dnf install -y openssh-server firewalld
```

Este comando instala SSH para conectarse desde MobaXterm y el firewall para controlar las conexiones.

## Paso 2. Activar SSH y el firewall

```bash
sudo systemctl enable --now firewalld sshd
```

Este comando inicia SSH y el firewall. También permite que arranquen automáticamente al encender CentOS.

## Paso 3. Permitir conexiones SSH

```bash
sudo firewall-cmd --permanent --add-service=ssh
```

Este comando permite las conexiones SSH en el firewall para acceder desde MobaXterm.
