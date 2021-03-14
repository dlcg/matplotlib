**Ceci est une prise de note sur ma compréhension de Matplotlib et surtout des besoins que j'en ai.**

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
/usr/lib/python3.9/site-packages/matplotlib   
 $  ls py*
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



Faire subplots(1) ou subplots(1,1) équivaut à ne rien mettre.
