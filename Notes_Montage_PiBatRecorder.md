<header>
**PiBatRecorder**  
============
</header> 

Date: 16/05/2017  
Author: JF Godeau et JL Leclef  

---  

# "log" du montage d'un PiBatRecorder.  

Le projet PiBatRecorder a pris une forme très aboutie début 2017, ce qui a été signalé sur les différents forums, notamment en pointant vers [ce post](http://pibatrecorder.ardechelibre.org/2017/01/30/2017-nouvelles-pibatrecorder/) qui présente succinctement le résultat, de nombreuses photos à l'appui.  
En parallèle au site officiel <http://pibatrecorder.ardechelibre.org/> il y a une plate-forme *Framagit* sur laquelle se trouvent tous les codes sources avec les documents, schémas et discussions sur le développement du projet: [Framagit](https://framagit.org/PiBatRecorderPojects/PiBatRecorder).  
Un fichier *Markdown* permettant de créer cette page html est [à télécharger ici](http://jeff37.github.io/Notes_Montage_PiBatRecorder.md). S'il y a des ajouts ou commentaires à apporter, il suffit de l'éditer et de me le renvoyer [par mail](mailto:jfgodeau@gmail.com).  

## Etapes  
- 11/03/2017: création de cette page  
- 18/04/2017: Jean-Louis a reçu le Raspberry Pi A+ et la carte audio Wolfson de chez Element14  
- 16/05/2017: commande par JL de la micro SD, de plusieurs types de micro (Knowles et MEMS) et commande par moi de l'afficheur, du keypad, des batteries (+ chargeur), d'un case et de la carte horloge (penser à acheter les piles!)  

## PiBatRecorder est composé des éléments suivants :
- ~~Une carte processeur Raspberry Pi A+,~~  
- ~~Une carte audio Cirrus Logic Wolfson à 192kHz de fréquence d'échantillonnage maximum,~~  
- ~~Une carte horloge temps réel avec batterie pour conserver l'heure à l'arrêt,~~  
- ~~Une carte afficheur OLED 128x64 pixels avec contrôleur type SH1106 ou SSD1306,~~  
- ~~Un clavier sensitif 16 touches type TTP229,~~  
- ~~Une carte SD 16GO avec une image RaspBian spécifique proposée par le constructeur de la carte audio~~  
- ~~Un micro avec un éventuel pré-ampli connecté sur l'entrée casque ou ligne de la carte audio,~~  
- En option, un amplificateur audio sur la sortie ligne ou un casque sur la sortie casque,  
- En option, une clé USB pour l'enregistrement des fichiers wav.  

### Hardware (ce que je trouve sur le web)
#### Raspberry Pi A+
cf. JL  

#### Carte audio Cirrus Logic Wolfson
cf. JL  

#### Carte horloge temps réel avec batterie
##### Chez UUGear  
Livraison en Belgique de la [Witty Pi 2: Realtime Clock and Power Management for Raspberry Pi (#WITTY_PI_2)](http://www.uugear.com/product/wittypi2/). Prix: 18.24 €  

##### Chez McHobby  
Livraison en Belgique de la ADF-RTC-DS1307-v2 Horloge temps réel DS1307 (RTC) (10,94 €) ... ??? on verra si c'est bon!?  

#### Carte afficheur OLED  
##### Chez McHobby  
Livraison en Belgique de l'afficheur OLED-128x64-MON Aff. Graphique OLED 128x64 Monochrome (29,38 €)

##### Chez Aliexpress  
Livraison en Pologne d'un autre afficheur plus petit, aussi en 128x64, `Nouveau 1 Pcs 128X64 Bleu OLED LCD LED Module D'affichage Pour Arduino 0.96 "I2C IIC SPI Série new original` à $2.52 + $1.78 shipping  

**NB. Drivers!!**  
cf. plus bas, les bibliothèques utilisées: https://github.com/hallard/ArduiPi_OLED   
?: Python library for 0.96'' OLED display: https://github.com/BLavery/lib_oled96  
?: Python module to drive a SSD1306 / SSD1322 / SSD1325 / SSD1331 / SH1106 OLED: https://github.com/rm-hull/luma.oled   


#### Clavier 16 touches: Raspberry Pi Model Capacitive Touch Keypad Module Kit 16 Touch Key I2C Port  
##### Chez Aliexpress  
Livraison en Pologne: <http://www.aliexpress.com/item-img/Raspberry-Pi-Model-B-B-TTP229-LSF-Detector-Controller-Capacitive-Touch-Keypad-Supports-Up-To-16/32244629626.html#> --> 9.99$  

##### e-Bay
Livraison en Belgique: $9.95 + free shipping  

#### Carte SD 16GO (pour importer l'image RaspBian)
##### Chez Richelt  
cf. JL. Réf: LSDMI32GCBEU1000	microSDHC-Card 32GB - Lexar - UHS-II (€22,36 net)  


#### Micro
##### Tenté chez Reichelt
MCE 101 Electret capacitor microphone capsule (€0,84), mais serait limité à 12 kHz!  

##### Chez Mouser
1 MEMS à 2€ et un Knowles FG-23329-P07 à 26.84€ ... + 20€ de shipping (F***ing bastards!).  


#### Amplificateur audio sur la sortie ligne ou casque sur la sortie casque  
-> Casque ou mini haut-parleur portable  

#### Clé USB  
Ce que j'ai...  

#### Batterie LiIon

Commandé avec chargeur (USB) chez McHobby:  
- ADV-LIPO-USBCHAR  	Chargeur LiIon/LiPo (18,04 €)  
- ACC-LIPO-6.6Ah 	Accu Lipo - 3.7v 6600mAh (28,07 €)  


#### Case

A bricoler sois-même mais j'ai quand même tenté d'en acheter un tout fait chez UUgear (République Tchèque): [Acrylic Case for Witty Pi (1 or 2), 7-Port USB Hub and Raspberry Pi (Clear)](http://www.uugear.com/product/acrylic-case-for-7-port-usb-hub-wittypi-and-raspberry-pi-clear/) pour le truander à la foreuse!  

### Autres éléments matériels (cf. document Platine J2)

Câble USB-série, cf. <https://www.adafruit.com/product/954> mais JL a des solutions!  


## Info du forum
La réalisation de cet ensemble est effectuée à partir des éléments ci-dessous (le fournisseur est donné à titre d'exemple):  

- Nappe 10 fils 1m (suffisant pour 4 exemplaires minimum) <http://www.gotronic.fr/art-cable-en-nappe-cnm10-30.htm>,  
- Plaque à pastilles 50x100mm (suffisant pour 4 exemplaires minimum) <http://www.gotronic.fr/art-plaque-d-essais-bcs050-6931.htm>,  
- Connecteur 2x10 femelle à souder pour le connecteur J2 de la carte audio <http://www.gotronic.fr/art-connecteur-fh210-4477.htm>,  
- Connecteur 1x4 femelle à souder pour le connecteur écran <http://www.gotronic.fr/art-connecteur-fh1x4-22730.htm>,  
- Connecteur 1x36 droit mâle à souder pour le connecteur clavier (2x5 utilisé, suffisant pour 3 exemplaires) <http://www.gotronic.fr/art-connecteur-he14-mh100-4457.htm>,  
- Connecteur 1x36 coudé mâle à souder pour le connecteur horloge (1x5 utilisé, suffisant pour 7 exemplaires !) <http://www.gotronic.fr/art-connecteur-he14-mh190-4458.htm>,  
- Connecteur JST3 coudé mâle 3 contacts + cordon femelle pour les alimentations. 1 exemplaire nécessaire pour l'alimentation du pré-ampli et un autre en option pour l'alimentation de l'amplificateur audio si vous voulez une sortie sur haut-parleur (il est possible d'utiliser l'amplificateur interne de la carte audio). Avec un casque, un amplificateur n'est pas nécessaire <http://www.gotronic.fr/art-cordon-jst-male-femelle-3-cts-jst3-22570.htm>,  
- Connecteur JST4 coudé mâle 4 contacts + cordon femelle pour l'encodeur de la molette hétérodyne <http://www.gotronic.fr/art-cordon-jst-male-femelle-4-cts-jst4-22571.htm>,  
- Le connecteur J8 pour la console n'est nécessaire que pour travailler sur le système Linux en l'absence d'une clé USB Wifi <http://www.gotronic.fr/art-connecteur-fh1x3-22729.htm>.  

### Software
Tous les codes sources se trouvent sur [le dépôt framagit](https://framagit.org/PiBatRecorderPojects/PiBatRecorder/tree/master) qui contient les sous-répertoires suivants (voir à quoi chacun sert dans le tableau en bas de page):  
- Construction  
- PiBatRecorder  
- PiBatScheduler  
- PiBatUpdater  

#### OS Raspbian
Une image du système d'exploitation Linux (RaspBian) est à télécharger sur <http://pibatrecorder.ardechelibre.org/os-image/>.  
On y trouve les explications pour créer la carte SD avec l'image.  
Téléchargé la version courante le 14/05/2016.  

#### Le logiciel utilise les bibliothèques externes suivantes :
- GPU_FFT pour le calcul des FFT en utilisant le GPU de la carte Raspberry. Cette bibliothèque est embarquée directement dans l'exécutable. Site internet: http://www.aholme.co.uk/GPU_FFT/Main.htm  
- PortAudio pour la gestion des entrées/sorties audio standard. Site internet : http://www.portaudio.com/  
- Adafruit GFX pour la gestion de l'écran OLED avec contrôleur de type SSD1327 ou SH1106. Site internet : https://github.com/hallard/ArduiPi_OLED  
- WiringPi pour la gestion du GPIO et des timer. Site internet : http://wiringpi.com/  


## Tableau de synthèse du projet (liens pas à jour car ça date du 08/12/2015!)
Se trouve sur <https://framacalc.org/BrqdyTwc4v>  

|Nom                                                                    |X                                                     |PiBatManualRecorder                                                                                                           |PiBatAutomaticRecorder                                                                                                                                                              |PiBatFixedRecorder                                                                                     |PiBatLogger                                                                                                                                                                                                       |Prix.approximatif |Lien.internet                                                                                                                                                        |
|:----------------------------------------------------------------------|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|Fonctions globales                                                     |                                                      |Utilisation manuelle avec écoute hétérodyne et enregistrement wav. Permet un fonctionnement automatique type SM2 sur une nuit |Utilisation automatique de type SM2 pour enregistrement de wav sur une ou plusieurs nuits Modification des paramètres via un PC+Navigateur, liaison câble (Écran/Clavier en option) |Utilisation automatique en point fixe sur de nombreux jours. Lien internet avec le serveur Vigie-Chiro |Surveillance automatique sur plusieurs semaines de l'activité d'une espèce facile à détecter (Grand Rhino par exemple). Modification des paramètres via un PC+Navigateur, liaison câble (Écran/Clavier en option) |                  |                                                                                                                                                                     |
|Matériel                                                               |Fonction                                              |                                                                                                                              |                                                                                                                                                                                    |                                                                                                       |                                                                                                                                                                                                                  |                  |                                                                                                                                                                     |
|Carte Pi Zero (ou A+ pour ceux qui ne veulent pas souder sur la carte) |Carte processeur et mémoire                           |Oui                                                                                                                           |Oui                                                                                                                                                                                 |Oui sauf si les traitements nécessitent une carte plus puissance (PI 2)                                |Oui                                                                                                                                                                                                               |9 à 30            |<http://www.kubii.fr/nano-ordinateurs-raspberry-pi/1401-raspberry-pi-zero--3272496003408.html>                                                                       |
|Carte audio Wolfson                                                    |Carte acquisition audio Fe 192kHz                     |Oui                                                                                                                           |Oui                                                                                                                                                                                 |Oui                                                                                                    |Oui                                                                                                                                                                                                               |40                |Non fonctionnel: <http://www.kubii.fr/cartes-extension-cameras-raspberry-pi/482-carte-wolfson-audio-raspberry-pi-b-640522710478.html>                                |
|Carte horloge                                                          |Sauvegarde date/heure sur coupure alimentation        |Oui (Non mais mise à jour manuelle à chaque mise en route)                                                                    |Non                                                                                                                                                                                 |Non (via Internet)                                                                                     |Non                                                                                                                                                                                                               |12                |Non fonctionnel: <http://www.kubii.fr/composants-raspberry-pi/436-shim-rtc-horloge-temps-reel-640522710348.html>                                                     |
|Carte WittyPi                                                          |Horloge plus gestion énergie avec mode veille         |Non                                                                                                                           |Oui                                                                                                                                                                                 |Non                                                                                                    |Oui                                                                                                                                                                                                               |15                |<http://www.uugear.com/product/witty-pi-realtime-clock-and-power-management-for-raspberry-pi/>                                                                       |
|Pré-ampli micro                                                        |Ajustement niveau et correction courbe de réponse     |Oui (un seul sur entrée Headset)                                                                                              |Oui (un seul sur entrée Headset ou deux pour la stéréo sur entrées lignes)                                                                                                          |Oui (un seul sur entrée Headset)                                                                       |Oui (un seul sur entrée Headset)                                                                                                                                                                                  |10                |                                                                                                                                                                     |
|Micro                                                                  |MEMS ou électret                                      |Un                                                                                                                            |Un ou deux                                                                                                                                                                          |Un ou deux                                                                                             |Un                                                                                                                                                                                                                |2                 |                                                                                                                                                                     |
|Alimentation                                                           |                                                      |Batterie Li-Ion type chargeur de secours de téléphone                                                                         |Batterie de plusieurs dizaines d'ampères/heure                                                                                                                                      |Secteur                                                                                                |Batterie de plusieurs dizaines d'ampères/heure                                                                                                                                                                    |30                |                                                                                                                                                                     |
|Écran OLED 21x6 caractères                                             |                                                      |Oui                                                                                                                           |Non (Oui en option pour le paramètrage)                                                                                                                                             |Non (Oui en option pour le paramètrage)                                                                |Non (Oui en option)                                                                                                                                                                                               |10                |Plus disponible: <http://fr.aliexpress.com/item/1-3-Inch-white-I2C-IIC-OLED-LCD-Module-Serial-128X64-LED-Display-Modules-for-Arduino/32445305003.html>               |
|Clavier sensitif 16 touches                                            |                                                      |Oui                                                                                                                           |Non (Oui en option pour le paramètrage)                                                                                                                                             |Non (Oui en option pour le paramètrage)                                                                |Non (Oui en option)                                                                                                                                                                                               |10                |Non fonctionnel: <http://fr.aliexpress.com/item/Raspberry-Pi-Model-B-B-TTP229-LSF-Detector-Controller-Capacitive-Touch-Keypad-Supports-Up-To-16/32244765970.html>    |
|Boîtier                                                                |                                                      |Oui, tout en un                                                                                                               |Oui, si possible étanche (dans le cas sans clavier/écran). Éventuellement avec batterie et micros séparées                                                                          |Oui tout en un, étanche avec entrée secteur                                                            |Oui, si possible étanche (dans le cas sans clavier/écran) et probablement avec batterie séparée                                                                                                                   |30                |                                                                                                                                                                     |
|Clé USB mémoire                                                        |Mémorisation des résultats                            |Oui                                                                                                                           |En option (en absence de clavier/écran, utilisation de la carte SD système et récupération en Ftp avec un PC)                                                                       |Non                                                                                                    |En option (en absence de clavier/écran, utilisation de la carte SD système et récupération en Ftp avec un PC)                                                                                                     |15                |                                                                                                                                                                     |
|Clé USB WiFi                                                           |Assure le lien Internet                               |Non                                                                                                                           |Non                                                                                                                                                                                 |Oui (Non si liaison câble)                                                                             |Non                                                                                                                                                                                                               |10                |                                                                                                                                                                     |

---  
**Description logiciels**   

|Nom                    |X                                                                                                                                                                                                                                                                      |PiBatManualRecorder        |PiBatAutomaticRecorder             |PiBatFixedRecorder    |PiBatLogger                      |
|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------|:----------------------------------|:---------------------|:--------------------------------|
|Logiciel               |                                                                                                                                                                                                                                                                       |                           |                                   |                      |                                 |
|PiBatRecorder          |Logiciel en C++ permettant enregistrement, hétérodyne, lecture et pilotage clavier écran. Utilisable sans clavier/écran pour le mode automatique (enregistrement seul). Des contraintes temps réel fortes font que ce logiciel n'est pas découpé en plusieurs modules. |Oui                        |Oui                                |Oui                   |Oui                              |
|PiBatManager           |Logiciel en Python permettant la gestion d'un écran/clavier et la modification des paramètres pour lancer PiBatRecorder en automatique                                                                                                                                 |Non                        |Oui si présence clavier/écran      |Non                   |Oui si présence clavier/écran    |
|PiBatScheduler         |Logiciel en python permettant le lancement de PiBatRecorder (et d'autres tâches éventuelles) aux heures programmées                                                                                                                                                    |Non                        |Oui                                |Oui                   |Oui                              |
|PiBatWebServer         |Serveur Web en Python pour la modification des paramètres de fonctionnement                                                                                                                                                                                            |Non                        |Oui si clavier/écran absent        |Oui                   |Oui si clavier/écran absent      |
|PostTraitement         |Traitement(s) en différé sur les fichiers wav                                                                                                                                                                                                                          |Non                        |Probablement non                   |Probablement oui      |Oui                              |
|Transfert données      |Transfert des données vers le serveur Vigie-Chiro                                                                                                                                                                                                                      |Non                        |Non (Oui en option)                |Oui                   |Non                              |



