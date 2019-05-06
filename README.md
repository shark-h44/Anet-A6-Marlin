# Anet A6 - Marlin et BL-TOUCH

Il esxiste pas mal de tutos sur la configuration de l'imprimante 3D Anet A8.
Je vous propose içi le fichier de configuration de mon imprimante Anet A6 équipée d'un support d'extrudeur bowden de type Frankenstein et d'un BL-Touch.

## Différence entre ANET A8 et A6 

La broche utilisée pour la commande du servo moteur n'est pas la même que sur Anet A8.
Les schémas que l'on trouve sur le net sont donc faux :

Ci dessous les câblage à effectuer en fonction de l'imprimante :
- Anet A6 : 29 (pin 27 utilisée par l'écran graphique).
- Anet A8 : 27

![bl](https://user-images.githubusercontent.com/38717304/57212033-b024bb00-6fe2-11e9-8bc4-ba66ffe5d8ab.jpg)

Note : Le numéro des pin (27,29) sont ceux du microcontroleur, pas celui des broche du connecteur.

## Compilation / taille du code

Le code est compilé sous Arduino (peut aussi l'être avec PlateformIo) et tourne avec Optiboot (sinon, ça passe difficilement)
Quelques pistes pour réduire la taille du code : 
- Laisser la langue en anglais
- Désactiver le boot screen
- Ne rien n'activer d'autre que le BL-TOUCH et la stratégie de palpation

Si vous souhaitez activer d'autres fonctionnalité, il faudra changer de carte mére, celle de l'ANET A6-A8 (en V1.5 pour moi) est trop juste en espace mémoire
