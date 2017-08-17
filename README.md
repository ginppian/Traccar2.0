Traccar 2
==========

## Objetivo

<p align="justify">
	Instalar la versión nueva de Traccar.
</p>


## Técnico

<p align="justify">
	En nuestro caso usamos <a href="https://m.do.co/c/ccd8a4dcf484">Digital Ocean</a>
</p>

1. Creamos un VPS(Virtual Personal Server) en <a href="https://m.do.co/c/ccd8a4dcf484">Digital Ocean</a>

2. Instalamos Java 8

```
$ sudo add-apt-repository ppa:webupd8team/java
$ sudo apt-get update
$ sudo apt-get install oracle-java8-installer
$ sudo apt-get install oracle-java8-set-default
```

3. Modificamos la hora

- List available timezones

```
timedatectl list-timezones

```

- Set the desired timezone

```
sudo timedatectl set-timezone America/Mexico_City
```

 Verify that the timezone has been set properly

```
timedatectl
```


4. Instalamos la última versión de Traccar, en nuestro caso la v3.13.

Para ver todas las versiónes <a href="https://github.com/tananaev/traccar/releases">aquí</a>.

```
$ cd /opt
$ wget https://github.com/tananaev/traccar/releases/download/v3.13/traccar-linux-3.13.zip
$ sudo apt-get install unzip
$ unzip traccar-linux-3.13.zip
$ chmod +x traccar.run
$ sudo ./traccar.run
$ sudo /opt/traccar/bin/startDaemon.sh
```

para versiones más recientes por favor seguir este <a href="https://github.com/ginppian/Traccar">tutorial</a>.

5. Puertos

Recordemos que el Sistema Web funciona bajo el puerto *8082* y la <a href="https://github.com/tananaev/traccar-client-android">Aplicación Móvil</a> bajo el puerto *5505*.


## Conclusión

Práctico, muy útil para una implementación rápida. Para consultas sobre la Aplicación Móvil o instalaciones más recientes clic <a href="https://github.com/ginppian/Traccer">aquí</a>. 


## Fuente

* <a href="https://www.traccar.org/linux/">Install Traccar in Linux</a>
* <a href="https://www.digitalocean.com/community/tutorials/how-to-set-up-timezone-and-ntp-synchronization-on-ubuntu-14-04-quickstart">How To Set Up Timezone and NTP Synchronization on Ubuntu 14.04</a>