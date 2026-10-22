# Servidor web con HTTPD en CentOS

Autor: Franklin Andres Luna Arias

En esta práctica se configura un servidor web en CentOS usando Apache HTTPD y MobaXterm.

## Paso 1. Instalar SSH y el firewall

```bash
sudo dnf install -y openssh-server firewalld
```

Este comando instala SSH para conectarse desde MobaXterm y el firewall para controlar las conexiones.
