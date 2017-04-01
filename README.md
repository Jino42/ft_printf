FT_PRINTF
===

Presentation
-
Recoder printf de la librairie C avec uniquement :
◦ write
◦ malloc
◦ free
◦ exit
◦ les fonctions du man 3 stdarg (Pour récuperer plusieurs arguments)

Mon printf gères (Consigne obligatoire)
• les conversions suivantes : sSpdDioOuUxXcC
• les flags #0-+ et espace
• la taille minimum du champ (width)
• la précision (.)
• les flags hh h l ll j z

S && C etant l'unicode UTF8 : https://fr.wikipedia.org/wiki/UTF-8

Et que printf est une fonction très très riche : http://manpagesfr.free.fr/man/man3/printf.3.html

![42fc](https://github.com/Jino42/ft_printf/blob/master/pic/42fs.png)

C'est pour cela que le 42FileChecker propose presque 800tests unitaire pour verifier la précision de notre printf.

J'ai décider par soucit de propreté de gérer tout les cas défini et indéfinie de manière logique et ludique, comme printf les gèrent;
ft_printf("%##00##00 33..1..#00d", 42); a donc un sens.

Code
-
Le code est très épurer dans le sens ou, qu'importe la convertion, le chemin reste le meme. Ce qui donne un sens très logique a mon printf
J'utilise un buffer pour rester rapide et propre
Il n'y a aucune condition qui sort de l'ordinaire (Enfaite si, il y en a une, qui m'a couté des points :p)

*Bonus fait :*
La convertion f (Double/Float Peut précis)
Le flag *

*A faire :*
Pouvoir récuperer la string dans un pointeur (sprintf)
Pouvoir afficher la string sur un autre FD (dprintf)
Pouvoir afficher le binaire (%b)
Avoir une meilleur gestion du %f
