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

![banngrab](https://user-images.githubusercontent.com/95232318/164916154-7f00139d-486d-4dc4-ae1f-55bfa15b9fbc.png)


## Exemple :

![aaaaaaaa](https://user-images.githubusercontent.com/95232318/164916439-b09f3978-7986-49e2-bbd4-0a90a1b6d710.png)


## Credits :

Credits to:

- https://sourceforge.net/projects/metasploitable/files/Metasploitable2/

## Informations :

- Written by : Presta
- Language : Python3
