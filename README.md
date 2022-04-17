# BannerGrabber

BannerGrabber est un script en python3 vous permettant de capturer les bannières des ports que vous souhaitez. Par défaut le script cherchera des bannières en se connectant sur chaque port dans le rang 1-65535 ce qui peut être assez long. Vous pouvez mettre un rang personalisé avec l'option -p. 
Par ailleurs si vous ne voulez checker que un port , par exemple le port 22 vous pouvez utiliser -p 22-22.
Vous pouvez également personnaliser le timeout ( le temps en seconde au bout duquel une tentative de connexion sur un port est avorté ) en fonction de vos besoins et de la rapidité de votre réseau. 

**Pensez à ne pas mettre un timeout trop bas, auquel cas l'hôte distant n'aura pas le temps de répondre : le script fonctionnera mal voir pas du tout.**


## Installation :
```
git clone https://github.com/PrestaDZ/GrabBanner.git
cd GrabBanner
pip3 install -r requirements.txt
```

## Usage :

```

$ python3 BannerGrabber.py --help
     ____                               ____           _     _
    | __ )  __ _ _ __  _ __   ___ _ __ / ___|_ __ __ _| |__ | |__   ___ _ __
    |  _ \ / _` | '_ \| '_ \ / _ \ '__| |  _| '__/ _` | '_ \| '_ \ / _ \ '__|
    | |_) | (_| | | | | | | |  __/ |  | |_| | | | (_| | |_) | |_) |  __/ |
    |____/ \__,_|_| |_|_| |_|\___|_|   \____|_|  \__,_|_.__/|_.__/ \___|_|

   --< Search for banners
   --< By @Presta


usage: [-h] -i IP [-p PORTS] [-t TIMEOUT]

optional arguments:
  -h, --help            show this help message and exit
  -i IP, --ip IP        The ip address.
  -p PORTS, --ports PORTS
                        Range port to scan (default is 1-65535) | ( python3 BannerGrabber.py -p 1-100 ).
  -t TIMEOUT, --timeout TIMEOUT
                        time before closing the communication in second, minimum is 5

```

## Exemple :

```
$ BannerGrabber.py -i 192.168.0.24 -p 20-22 -t 4
     ____                               ____           _     _
    | __ )  __ _ _ __  _ __   ___ _ __ / ___|_ __ __ _| |__ | |__   ___ _ __
    |  _ \ / _` | '_ \| '_ \ / _ \ '__| |  _| '__/ _` | '_ \| '_ \ / _ \ '__|
    | |_) | (_| | | | | | | |  __/ |  | |_| | | | (_| | |_) | |_) |  __/ |
    |____/ \__,_|_| |_|_| |_|\___|_|   \____|_|  \__,_|_.__/|_.__/ \___|_|

   --< Search for banners
   --< By @Presta


[!] The timeout is set to 4, programm may not work correctly
[i] Starting at : 16:42:53

[+] At port 21 : 220 (vsFTPd 3.0.3)
[+] At port 22 : SSH-2.0-OpenSSH_8.4p1 Debian-5

[i] Ending at 16:42:59, scanned in 6s

``` 

## Informations :

- Written by : Presta
- Language : Python3
