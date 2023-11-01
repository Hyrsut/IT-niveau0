Appliquer le modèle OSI dans la vie réelle n'est pas aisé de prime abord, mais peu se comprendre assez rapidement.

Ainsi, il faut savoir a quelle couche peuvent correspondre chaque type d'équipement réseau, et connaître les "protocoles" qui se cachent dérrière.

## Couche 1 | physique : les cables les prises et les cartes réseau

Un moyen simple de comprendre les couches étant de visualiser les équipements, il suffit de se dire que la couche 1 est tout simplement l'infrastructure qui permet au réseau d'exister. Aujourd'hui, cela comprend les cables réseau cuivre (ethernet) la fibre optique, et tout les connecteurs qui y sont liés.

Sur un équipement, cela va aussi comprendre l'existence même d'une interface, avec a la limite un nom d'interface (GI 1/0/1 sur un switch Cisco par exemple), mais pas plus.

L'adresse MAC se retrouve uniquement à la partie suivante.

A l'échelle de la couche physique, seuls comptes les bit de données, rien d'autre. Pour le moment, l'information n'est que 1 et 0 qui sont envoyés par un signal électrique entre deux interface.

## Couche 2 | Liaison : le switching

Le sujet comment a devenir plus complet à la couche 2, car il s'agit ici de savoir adresser correctement les informations.

Ainsi la notion d'adressage commence ici, avec notamment la fameuse table des adresses MAC, ainsi que la table ARP.

Nul besoin de switch pour parler de couche 2, une connexion entre deux ordinateurs windows suffira, car tout ordinateur a déjà une table ARP pour savoir à qui envoyer l'information. La problématique venant plus souvent du fait que les ordinateurs n'ayant qu'une interface, la table mac renvoi toujours par le même canal.

Un switch permet de faire l'intermédiaire. En se référant à sa table d'adresse MAC, il sera capable de faire la transmission à la bonne machine.



## Couche 3 | Réseau : routeur et parefeu, passerelle et routage

## Couche 4 | Transport : Parefeu et ordinateur, TCP et UDP