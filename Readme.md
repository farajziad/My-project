# Mon Projet du Micro-controlleur "Air Controller"
Créer un microcontroleur avec une technologie avancée du BT ou du WI-FI
le microcontrolleur va etre programmer avec le WI-FI ou le BT sans la souffrance des cables de programmation et avec un processeur tres simple qui est l'ATmega 328p et une ecran OLED avec "4 digits" pour afficher l'etat du micro-controlleur et plus une LED connecté au pin 13 du ATmega pour quelle indique l'alimentation du micro-controlleur et en plus des petits ventilateurs en bas du micro controlleur pour le refroidissement du regulateur 5V qui va alimenter tous les composants ayant besoin de 5V pour fonctionner et en plus deux piles de battrie qui ont comme durée de vie qui est presque 17 heure ou plus et la fonction la plus impressionante du projet est le control du BT , tu peux programmer avec C++ juste avec le BT selon une application qui s'applle Air controller , sans la souffrance des cables.
Ce projet et une grande solution et un moyen pour que les debutents en robtiques puissent la utiliser et la programmer avec C++ selon le BT soit avec pc , soit avec telephone et sonprix n'est pas chére car elle est fabriqué avec un micro processeur "ATmega 328p" ce qui rend la fabriquation du microcontrolleur un peu plus compliqué et qui prend un peu du temps.
et en plus L'application qui va etre créer par moi avec l'HTML ou un logiciel tres simple pour fabriqué les applications (ex : MIT app inventor) est cette application va etre capable sans aucun probléme de televerser le code C++ avec le mode BT est cette methode pour moi est une bonne methode car avec la progrommation cablé les roboticiens rencontre parfois des problémes lors du port .
# La partie Hardware du Micro-controlleur "Air Controller"
Pour la partie Hardware le Micro-controlleur sera avec une carte d'impression PCB ou il va être le materiel collé avec l'appareil à souder .
+Les composants qui seront utilisés sont : 
1-ATmega 328p
2-OLED diplay (la petite ecran)
3-LED
4-Un petit vontilateur
5-Regulateur 5V
6-BT module
7-Batterie
+Le rôle de chacun de c'est composants : 
1-ATmega 328p : le cerveau du micro-controlleur qui va pouvoir programmer les projets electroniques et les robots.
2-OLED display : Dans cette petite écran permet de visualiser l'etat du micro-controlleur (ex : le televersement , le fonctionnement , etc).
3-LED : cette LED va etre connecté à l'ATmega 328 p pour savoir si le micro-controlleur est allumé.
4-Un petit vontilateur : Ce vontilateur va être utilisée pour refroidîre le Regulateur 5V.
5-Regulateur 5V : Ce regulateur va etre utilisée pour alimenté les appareils ayant besoin de 5V (ex : BT module , écran OLED , ATmega 328p , petit vontilateur ).
6-BT module : C'est l'option avancée du projet entier , il va être utilisée pour la programmation (C++ ou les Blocs).
7-Batterie : elle va être composée de deux piles rechargeables qui ont 17 heure et plus pour durée de chaque racharge.
# La partie Software du Micro-controlleur "Air controller"
Pour la partie du software je vais utiliser Arduino IDE come programmateur avec le C++ , et même pour configurer le bootloader la programmation va être avec une autre arduino ("Arduino as ISP") la progrommation va-t-être sous un programme C++ , et aprés ce programme le projet va-t-être prêt.
# Et pour les composants , quelque composants ont étè prises d'un ancien materiel
##  Grand Questionnaire d'Ingénierie : Air Controller 

###  SECTION A : PHILOSOPHIE ET DESIGN DU SYSTÈME
#### Question  : Quel est le scénario d'utilisation idéal de ton Air Controller dans la vie réelle ?
*(Détaille s'il s'agit d'un boîtier de bureau, d'un système embarqué dans un placard, ou d'un prototype de laboratoire).*
Réponse : pour le prototype j'ai fabriqué une boitier en carton et cette boitier ou se trouve les composants a l'interieur



#### Question  : Quelle sera la taille approximative de ton boîtier physique et quels matériaux aimerais-tu utiliser pour le fabriquer (impression 3D, plastique, bois) ?
Réponse :presque 15x15x15 et j'aimerais imprimer une PCB ou le materiel va etre coller sans aucun danger.

#### Question  : Comment visualises-tu l'ergonomie ? Est-ce que l'écran et les boutons seront sur le dessus, à l'avant, et pourquoi ce choix est-il le plus pratique ?
Réponse : 
le micro-controlleur va etre avec un bouton (On,OFF) , il est pratique car il est tres faciles a allumer et meme a l'arrêter.
---

###  SECTION B : ÉLECTRONIQUE ET CIRCUITS (HARDWARE)
#### Question  : L'ATmega328p fonctionne généralement en 5V. Si tu utilises des capteurs modernes qui fonctionnent en 3.3V, comment vas-tu adapter les tensions pour ne pas brûler tes composants ?
Réponse : j'utilise pas des capteurs et pour les autres composants j'ai utilisée un regulateur 5V connectée avec la batterie de 8V . 

#### Question  : Pourquoi est-il important de placer des condensateurs de découplage près des broches d'alimentation de ton microcontrôleur ?
Réponse : C'est important juste lorsque j'utilise le quartz mais maintenant j'utilise l'oscillateur interne de l'ATmega .

#### Question  : Quel type de connecteur physique veux-tu installer sur ton boîtier pour l'alimenter (un port USB-C, une prise Jack DC, ou des borniers à vis) ?
Réponse : J'ai utilisée une batterie de 8V chargeable et qui a comme dur+ée de vie pour chaque charge 17 heures

#### Question  : Pour concevoir ton circuit imprimé (PCB) sur KiCad, vas-tu choisir une carte à 2 couches (simple) ou à 4 couches, et quel est l'avantage pour la gestion de la chaleur ?
Réponse : Il y a pas un probléme dans le choix de type du PCB car mon Micro-controlleur posséde d'un vontilateur capable de refroidire tout le materiel.

#### Question  : Comment vas-tu connecter ton écran OLED à l'ATmega328p ? Vas-tu utiliser le protocole I2C (qui utilise seulement 2 fils de données) ou le SPI (plus rapide mais utilise plus de fils) ?
Réponse : je n'ai qu'une petite écran OLED à 4 fils de couleur d'affichege bleu .

#### Question  : Le ventilateur peut générer des parasites électriques (bruit inductif) lorsqu'il tourne. Quel composant de protection (comme une diode de roue libre) vas-tu ajouter pour protéger la puce ATmega328p ?
Réponse :
Non il ne fait aucun bruit car ce n'est qu'un petit vontilateur a moteur DC pour refroidir le regulateur 5V
---

###  SECTION C : PROGRAMMATION ET ALGORITHMES (SOFTWARE)
#### Question 21 : Décris l'algorithme de démarrage (la fonction `setup()`). Quelles sont les vérifications de sécurité que le code doit faire avant de lancer le ventilateur ?
Réponse : le ventilateur n'a aucune relation avec le code a televerser avec le BT

#### Question 22 : Comment vas-tu coder la gestion de la vitesse du ventilateur ? Vas-tu utiliser le signal PWM (Pulse Width Modulation) pour faire varier la vitesse proprement ? Explique le principe.
Réponse : Non, il fonctionne avec le DC 5V a travers le regulateur

#### Question 23 : Si l'utilisateur appuie sur un bouton physique, il y a un risque de "rebond" électrique (la puce croit qu'on a appuyé 10 fois au lieu d'une). Comment vas-tu régler ce problème (anti-rebond logiciel ou matériel) ?
Réponse :Non, Mon micro-controlleur est bien programmer et pour le bouton il y a un seul bouton "RESET" pour redemarer le miro-controlleur

#### Question 24 : Imagine la structure de ton code. Vas-tu utiliser une machine à états (State Machine) pour gérer les différents menus de l'écran OLED (Menu Principal, Menu Réglages, Écran d'Alerte) ?
Réponse :L'ecran OLED ne va pas avoir plusieurs utilités le role de cette ecran et juste indiqué le niveau de chargement du televersement et l'etat "allumé ou eteint"

#### Question 25 : Si tu devais ajouter un capteur de température (comme un DHT11 ou un TMP36), comment modifierais-tu le code pour que le ventilateur tourne plus vite quand il fait plus chaud ?
Réponse : je vais faire une condition ( if(E>30 & E==30){Analog.write (200);})

---
