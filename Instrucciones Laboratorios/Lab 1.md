
# Práctica 1: Instalación y configuración de nginx
  
### Scenario
  
Al final de la práctica se espera que el participante pueda observar en funcionamiento su servidor de nginx. 

Esta práctica está pensada para un sistema operativo CentOS / RedHat

### Objectivos:
  
- Instalar nginx.
- Familiarizarse con los principales comandos de nginx.

### 1. Instalación de nginx.

**1.1** Abrir la terminal de nuestro servidor. 

![1.png](../Imagenes/image001.png)

>***firmate con el usuario y contraseña compartido por el instructor***

**1.2**	Iniciar el super usuario. Consejo: Para cualquier instalación o configuración se recomienda usar el super usuario en nuestro Linux. 

Usar el siguiente comando:
~~~
sudo su
~~~
![2.png](../Imagenes/image003.png)

**1.3**	Actualizar los repositorios usar el comando: yum update
~~~
yum update
~~~ 
![3.png](../Imagenes/image005.png)

**1.4**	Instalar nginx usando el comando:
~~~
yum install nginx
~~~
![4.png](../Imagenes/image007.png) 

**1.5**	Esperar la instalación unos minutos, cuando se termine de instalar usar el comando systemctl status nginx para observar el estado del servidor, la primera vez que se instale el servidor estará en estado inactivo: 

~~~
systemctl status nginx 
~~~

**1.6**	Iniciar el servidor de nginx con el comando: 

~~~
systemctl start nginx
~~~
![5.png](../Imagenes/image011.png)

**1.7** Validar que el servidor este iniciado con el comando: 
~~~
systemctl status nginx
~~~
![6.png](../Imagenes/image013.png)

**1.8**	Obtener la IP pública de tu servidor usando el siguiente comando:
~~~
curl ifconfig.me
~~~
 ![7.png](../Imagenes/image015.png)
 ***Ten en encuenta que la dirección publica puede ser diferente en tu laboratorio***

 **1.9** Abrir un explorador web y pegar la IP pública de tu servidor.

 ### 2. Tarea Opcional

**2.1** Probar los siguientes comandos:

**Iniciar Nginx**
~~~
sudo systemctl start nginx
~~~
 **Detener Nginx**
 ~~~
 sudo systemctl stop nginx
~~~
**Recargar configuración sin interrupciones**
~~~
sudo systemctl reload nginx
~~~
**Reiniciar Nginx**
~~~
sudo systemctl restart nginx
~~~
**Verificar configuración de Nginx**
~~~
sudo nginx -t
~~~
**Mostrar versión de Nginx**
~~~
nginx -v
~~~
**Mostrar información de módulos cargados**
~~~
nginx -V
~~~
**Ver logs de acceso**
~~~
tail -f /var/log/nginx/access.log
~~~
**Ver logs de errores**
~~~
tail -f /var/log/nginx/error.log
~~~
**Abrir nginx.conf**
~~~
sudo nano /etc/nginx/nginx.conf
~~~
**Ver lista de módulos compilados**
~~~
nginx -V
~~~
**Detener Nginx**
~~~
sudo systemctl stop nginx
~~~

 
