
Naviguer dans le shell linux est extremement facile, les trois principales commandes à retenir sont les suivantes:
- cd
- ls
- pwd

# cd : navigation entre dossier

Pour illustrer nos propos, nous allons imaginer un ensemble de dossier composer de l'arborescence suivante:
/home/
		name/
				folder
		othername

La navigation entre les différents dossier (ie de /home/name vers /home par exemple) se fait via la commande cd.
Pour comprendre l'usage, il faut comprendre les bases de la nomination de chemin (Relatifs et absolus)


## notation relative

cd s'utilise soit en relatif, il suffit alors d'éxécuter la commande sans / au début du chemin
exemple, pour aller de /home vers /home/name, il suffit de faire un simple:
"cd name"

La notation relative permet également de revenir en amont de l'arborescence.
pour passer du dossier /home/name/folder a /home/name, il suffit d'exécuter :
"cd .."

Il est également possible de passer directement de /home/name a /home/othername en chemin relatif, pour cela il faut faire:
"cd ../othername"

## notation absolue

Le chemin absolu est plus simple a utiliser, mais nécessite de bien savoir où l'on veut aller.
En effet il suffit d'un simple cd /home/name/folder, depuis n'importe quel dossier pour se retrouver dans le sous dossier folder.

l'autocompletion permettra de s'y retrouver plus facilement, si tant est qu'on a une idée de ce qu'on cherche et des premières lettres (on peut très vite se retrouver avec des cinquantaines de sous dossiers dans certains dossier system linux)

# ls lister le contenu

## affichage simple

L'utilisation la plus simple et rapide de #ls et de taper simplement la commande, cela offre un affichage simple et brouillon, mais peu parfois suffir, tant que la masse d'élément a lister n'est pas trop importante

## affichage avancé

L'usage le plus courant reste la commande "ls -l" qui permet d'afficher bien plus de détail sur les éléments du dossier actif.

En effet, vous aurez ici les attribue de droits des fichiers et dossier (les fameux 640 ou 777, cf #chmod), ainsi que la possession (cd #chown). D'autres attribues comme le type d'éléments (fichier, dossier, volume) ainsi que les redirections possibles.

## affichage combiné

Le principal avantage de l'affichage avancé est de l'utiliser combiné avec un #pipe, en effet, le pipe permet de filtrer la sortie et de trouver un élément plus précis dans une longue liste.
Exemple: 
ls l- | grep rwxr-xr-x
permettre de trouver tous les fichiers ou dossier comprenant l'attribue de droit 