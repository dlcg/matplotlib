**Ceci est une prise de note sur ma compréhension de Matplotlib et surtout des besoins que j'en ai.**

Je m'inspire assez de la documentation officielle que j'ai grossièrement traduit et adapté à mon approche. 
Je vois un nombre de choses fausses sur le net qui est assez déconcertante, le pire étant sur Stack Overflow où l'on balance des réponses sans même comprendre son fonctionnement. Le problème est ce que la réponse peut donner le résutat escompté mais de manière détourné.

Les bases
=========

Matplotlib est une bibliothèque en Python servant à produire des graphiques et à les visualiser. 

Elle trace vos données dans ce que l'on appelle une "Figure" qui va contenir un ou plusieurs axes graphiques.


Tout commence par l'import de la bibliothèque 

```
import matplotlib.pyplot as plt 
```

Par cette ligne de code nous disons à Python que l'on va exploiter des fonctions se trouvant dans le fichier pyplot.py se situant le répertoire matplotlib.
Ce fichier est important car les fonctions servant à créer les graphiques sont de dedans
Mon poste personnel est sous arch-linux et les bibliothèques sont stockées à cet endroit:

**/usr/lib/python3.9/site-packages**

```
/usr/lib/python3.9/site-packages/matplotlib 
 $  ls py*
pylab.py  pyplot.py
```

Nous parlions d'axes graphiques dans une Figure. Concrétisons visuellement ce propos.

```
import matplotlib.pyplot as plt 
#Crée la "Figure" en question. Sur un même rendu, peut afficher 1 à n graphique.
plt.subplots()
#Affiche visuellement un graphique vide avec les axes abscisses et ordonnées.
plt.show()
```


Faire subplots(1,1) ou subplots(1) équivaut à faire subplots()
![](graph1.png)

Maintenant si nous faisons subplots(2)? puis subplots(1,2)?
![](graph2.png)
![](graph3.png)

Nous voyons bien sur les deux dernières images que les graphiques ont été doublés verticalement et horizontalement.
On peut en ajouter autant que l'on souhaite en afficher.

Terminologie Matplotlib:
Figure: est l'objet qui va contenir votre ou vos graphiques. Il faut voir cela comme un conteneur.
Axe: C'est le graphique en lui même avec tout ce qu'il va contenir ( le titre l'axe des abscisses et des ordonnées, le tracé visuelle de vos données)
Axis: ce sont les axes des abscisses et des ordonnées. 
Tick: ce sont les graduations sur vos axes des axes des abscisss et des ordonnées.

Il y a deux façons de créer vos graphiques avec matplotlib:
- où l'on dit explicitement ce que l'on va créer ( et donc avoir une meilleure maîtrise de ce que l'on fait), Figure, Axes etc... 
- L'autre méthode où l'on passe par pyplot pour qu'il produise lui-même les  Figure, Axes etc... On s'occupe uniquement du tracé de nos données.

Il y a une troisième manière de créer qui serait d'intégrer Matplotlib dans une application, mais je n'aborderai pas ce dernier.

Quand utiliser l'une ou l'autre méthode?
Il est conseillé d'utiliser la première méthode lorsque l'on veut intégrer son code dans un programme, que le code doit pouvoir être réutilisable.
La seconde approche se ferait plutôt lorsque l'on voudrait un rendu à chaud, voir ce que cela donnerait comme dans le mode interactif de Python ou bien jupyter le but étant de visualiser la donnée rapidement.


