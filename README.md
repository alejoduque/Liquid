
```bash

      ___                   ___           ___                       ___                       ___           ___     
     /\__\      ___        /\  \         /\__\          ___        /\  \          ___        /\  \         /\  \    
    /:/  /     /\  \      /::\  \       /:/  /         /\  \      /::\  \        /\  \      /::\  \       /::\  \   
   /:/  /      \:\  \    /:/\:\  \     /:/  /          \:\  \    /:/\:\  \       \:\  \    /:/\:\  \     /:/\:\  \  
  /:/  /       /::\__\   \:\~\:\  \   /:/  /  ___      /::\__\  /:/  \:\__\      /::\__\  /:/  \:\  \   /::\~\:\  \ 
 /:/__/     __/:/\/__/    \:\ \:\__\ /:/__/  /\__\  __/:/\/__/ /:/__/ \:|__|  __/:/\/__/ /:/__/ \:\__\ /:/\:\ \:\__\
 \:\  \    /\/:/  /        \:\/:/  / \:\  \ /:/  / /\/:/  /    \:\  \ /:/  / /\/:/  /    \:\  \  \/__/ \:\~\:\ \/__/
  \:\  \   \::/__/          \::/  /   \:\  /:/  /  \::/__/      \:\  /:/  /  \::/__/      \:\  \        \:\ \:\__\  
   \:\  \   \:\__\          /:/  /     \:\/:/  /    \:\__\       \:\/:/  /    \:\__\       \:\  \        \:\ \/__/  
    \:\__\   \/__/         /:/  /       \::/  /      \/__/        \::/__/      \/__/        \:\__\        \:\__\    
     \/__/                 \/__/         \/__/                     ~~                        \/__/         \/__/    

```



# LiquidIce es un Software que permite crear una transmision de audio a una radio online al tiempo que genera un archivo a partir de todos los aportes de un grupo de chat de la red de mensajeria instantanea y anonima Telegram: https://t.me/radiolibreCC 

LiquidIce permite distribuir contenidos, por ejemplo: 
1. Los archivos de audio enviados al grupo (al undir el icono de microfono de Telegram son transmitidos en tiempo real  a todos los participantes del grupo como tambien por una emisora en Internet (via Icecast) --> https://live.radiolibre.cc/bot.mp3
2. Las imagenes enviadas a traves de Telegram son archivadas en archive.org, por ejemplo: https://archive.org/details/fotoBot


¿Como funciona? Un bot (script) de Telegram captura todo lo que le envias y:

-Alamacena (Text,Docs,Video,Audio) en archive.org https://archive.org/details/@wiki-opdlv <br>
-Los audios son enviados, en orden de llegada a un streaming en Icecast<br> usando LiquidSoap, de ahi el nombre: LiquidIce


### Es un puente que pasa mensajes desde Telegram al software Icecast de una radio online (http://red.radiolibre.cc) dejando un archivo en Archive.org y funcionando desde una RaspberryPi version 3

Código base desarrollado por [Néstor Andrés Peña](http://www.nestorandres.com) para el laboratorio #TodoEsRadio realizado en CKWEB bajo la dirección de [alejoduque](https://github.com/alejoduque) con ayudas en desarrollo de [Juan kalashikov](https://github.com/kalashnikov2). Esta rama usa LiquidSoap, descartando la version 1 que usaba VLC y consumia casi todos los recursos de la raspberryPi.


### Corre desde una raspberryPi:
node-v8.9.0-linux-armv6l en rPi - https://nodejs.org/dist/v8.9.0/node-v8.9.0-linux-armv6l.tar.gz <br>

## Pasos a seguir para correr una instancia en un computador con Node.js instalado

Solicitar un Token para el bot de Telegram usando el botFather oficial de telegram.
Una vez se haya creado el bot, crear un nuevo archivo secret.js en la carpeta raíz con el siguiente contenido:

```bash
TOKEN = "aca-va-el-token-que-genero-el-botfather"
```

Antes de correr la aplicación por primera vez es necesario instalar las dependecias:

```bash
npm install
```

Con las dependencias instaladas ya se puede correr el script con:

```bash
node t2i.js
```

#<img src="#" /> <br>
