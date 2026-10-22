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

## Paso 4. Aplicar los cambios del firewall

```bash
sudo firewall-cmd --reload
```

Este comando aplica las reglas guardadas en el firewall.

## Paso 5. Consultar la IP del servidor

```bash
hostname -I
```

Este comando muestra la IP de CentOS, que se utiliza para conectarse al servidor y abrir la página web.

## Paso 6. Consultar el usuario

```bash
whoami
```

Este comando muestra el usuario actual de CentOS.

Con la IP y el usuario se configura la conexión en MobaXterm, seleccionando Session, SSH y el puerto 22.

## Paso 7. Instalar Apache HTTPD y curl

```bash
sudo dnf install -y httpd curl
```

Este comando instala Apache para publicar la página web y curl para comprobarla desde la terminal.

## Paso 8. Activar el servidor web

```bash
sudo systemctl enable --now httpd
```

Este comando inicia Apache y permite que arranque automáticamente al encender CentOS.
