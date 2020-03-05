<h1 align="center" style="box-shadow: 10px 5px 5px red">Compte rendu TP3</h1>                                   
<p>RIOUAL Matthieu :computer:</p>
<p>MORNEAU Hugo :computer:</P>

## Exercice 1

1) Les 5 derniers paquets installés sont "open-vm-tools.list", "ubuntu-server.list", "unattended-upgrade.list", "cloud-init.list" et "m-locate.list". On les trouve avec la commande: ```ls -ltr /var/lib/dpkg/info/*.list |tail -5```

2) On trouve 544 paquets installés avec: ```dpkg --get-selections | wc -l```, et 545 avec ```apt list --installed | wc -l```.

3) On trouve qu'il y a 88252 paquets disponibes au téléchargement avc la commande: ```apt-cache dup | grep -oP 'Package:' | wc -l```

4) On créé un alias ```maj``` mettant à jour le sytème en utilisant la commande: ```alias maj='sudo apt update'```. Pour rendre cet alias permanent, on place cette commande dans le fichier _.bashrc_.

5) Le paquet fortunes permet de tirer aléatoirement un pictogramme de biscuit de fortune chinois. On l'installe avec ```apt install fortune```.

6) Le paquet "sudoku" permet de jouer au suduku.

7) On utilise la commande ```grep "apt install" /var/log/apt/history/log``` pour afficher les derniers paquets installés par cette ligne de commande.
 
## Exercice 2

On peut utiliser la commande ```dpkg -S commande``` pour trouver quel paquet a installé une commande. ```ls``` par exemple vient de __linux-headers-5.3.0-29__.

On utilise le script __origine-commande.sh__ suivant pour obtenir le paquet ayant installé une commande:

```
#!/bin/bash
dpkg -S $1 | grep usr/ | head -1 | cut -d ":" -f 1
```

## Exercice 3:


## Exercice 4:

La commande ```dpkg -L coreutils``` nous donne les programmes livrés avec coreutils. La commande ```[``` sert à indiquer un test booléen.

## Exercice 5:

On installe __aptitude__ avec __apt__, on fait une recherche avec ```/```, choisit le bon paquet avec ```n```, appuie sur ```+``` pour installer, puis 2 fois ```g``` pour confirmer l'installation.

## Exercice 6:

## Exercice 7:
