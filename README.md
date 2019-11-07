# Motion-Capture

## Système
 
Concrètement, des cartes (nano-ordinateur) font "tourner" un programme Slave pour identifier des point via des caméras.
Ces nano-ordinateur s'occupent de calculer des droites dans un repère 3D et envoie leur calculs au PC Master (là encore un nano-ordinateur).
Tout le système décris utilise linux et ses fonctionnalités :

> Les cartes Slaves sont des orange pi Zero et tournent avec Linux Arm.

> La cate master est une Raspberry et tourne avec raspbian Jessy.

Le système garde une cohésion grace à un réseau cablé RJ45 et un switch pour la communication.

## Programme

J'ai développé deux programmes appelés Slave et Master permettant respectivements de detecter un point dans l'espace et de synthétiser les données recues.

Chaqu'un des deux programmes ont bien entendu un protocole de communication permettant l'échange d'informations.

### Programme Slave

Le programme Slave sera mis en oeuvre sur deux cartes pour le moment.
Ce programme est duplicable dans le sens où on peut rajouter à tout moment une nouvelle carte équipée du meme programme.

Plusieurs fonctionnalités seront implémentées dans le programme :
 * Détéction des points dans l'espace,
 * Interprétation de l'enplacement du point,
 * Envoie d'une droite de l'espace permettant d'identifier le point.

### Programme Master

Le programme Master est sans doutes la partie la plus complexe du projet.
Il fait office de terminal de l'application.

Ce programme est constitués de 3 parties interconnéctées :
 * La récéption des données,
 * L'interprétation des données,
 * La visualisation (qui pourra être réalisée par un autre système).




