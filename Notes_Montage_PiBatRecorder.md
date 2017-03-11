<header>
**PiBatRecorder**  
============
</header> 

Date: 10/03/2017  

---  

Mon "log" du montage d'un PiBatRecorder.  

Le projet PiBatRecorder a pris une forme très aboutie début 2017, ce qui a été signalé sur les différents forums, notamment en pointant vers [ce post](http://pibatrecorder.ardechelibre.org/2017/01/30/2017-nouvelles-pibatrecorder/) qui présente succinctement le résultat, de nombreuses photos à l'appui.  
En parallèle au site officiel <http://pibatrecorder.ardechelibre.org/> il y a une plate-forme *Framagit* sur laquelle se trouvent tous les codes sources avec les documents, schémas et discussions sur le développement du projet: [Framagit](https://framagit.org/PiBatRecorderPojects/PiBatRecorder).  
Un fichier *Markdown* permettant de créer cette page html est [à télécharger ici](http://jeff37.github.io/Notes_Montage_PiBatRecorder.md). S'il y a des ajouts ou commentaires à apporter, il suffit de l'éditer et de me le renvoyer [par mail](mailto:jfgodeau@gmail.com).  

## PiBatRecorder est composé des éléments suivants :
- Une carte processeur Raspberry Pi A+,  
- Une carte audio Cirrus Logic Wolfson à 192kHz de fréquence d'échantillonnage maximum,  
- Une carte horloge temps réel avec batterie pour conserver l'heure à l'arrêt,  
- Une carte afficheur OLED 128x64 pixels avec contrôleur type SH1106 ou SSD1306,  
- Un clavier sensitif 16 touches type TTP229,  
- Une carte SD 16GO avec une image RaspBian spécifique proposée par le constructeur de la carte audio  
- Un micro avec un éventuel pré-ampli connecté sur l'entrée casque ou ligne de la carte audio,  
- En option, un amplificateur audio sur la sortie ligne ou un casque sur la sortie casque,  
- En option, une clé USB pour l'enregistrement des fichiers wav.  

### Hardware (ce que je trouve sur le web)
#### Raspberry Pi A+

#### Carte audio Cirrus Logic Wolfson
##### Chez "Element14": <https://www.element14.com/community/community/raspberry-pi/raspberry-pi-accessories/cirrus_logic_audio_card> --> 34.18 €  
**Features:**   

- Compatible with Raspberry Pi B and A onwards (with 40-pin extended GPIO, and no P5 connector)  
- Capable of rendering HD Audio, at 24-bit, 192kHz  
- 3.5mm 4-pole jack for a headset/boom mic combination for gaming or VoIP applications  
- Two DMIC microphones onboard for stereo recording  
- 3.5mm jack for Stereo Line Input for high quality audio recording or capture  
- 3.5 mm jack Stereo Line Output for connection to devices such as external stereo amplifiers or powered speakers  
- Stereo Digital input and output (SPDIF)  

##### Chez Adafruit: <https://www.adafruit.com/product/1761> --> 49.95$  
**Features:**   

- Based on Cirrus Logic’s WM5102 audio hub, WM8804 S/PDIF transceiver, and a pair of WM7220 digital microphone ICs.  
- Onboard 1.4W per channel class D power amplifier for connection to external speakers (requires separate power supply)  
- On-board class D power amplifier for external speakers, with connection to external power source if needed.  
- Capable of rendering HD Audio at 24-bit, 192kHz  
- 3.5mm 4-pole jack for headphone output, with microphone facility (for headphones w/ boom microphone)  
- Small pin header for additional connections  

##### Chez Amazon: <https://www.amazon.com/Cirrus-Logic-Raspberry-Audio-Card/dp/B00RKSTK2O> --> $46.16 + $6.96 shipping
##### Chez Hi-Fi World?? http://www.hi-fiworld.co.uk/index.php/internet-audio/780.html?showall=1


#### Carte horloge temps réel avec batterie
WittyPi -> est-ce toujours la meilleure solution!? cf Lien dans le tableau en fin de page: `Dear customer, this product is now retired, and we have a newer generation of Witty Pi now`  
=> http://www.uugear.com/product/wittypi2/ ??  

#### Carte afficheur OLED
##### Chez Adafruit Technical Details <https://www.adafruit.com/product/938>

Breakout Board Dimensions:  

- PCB: 35mm x 35mm x 5mm / 1.4" x 1.4" x 0.2"  
- Mounting Holes Distance: 27mm / 1.1" apart  
- Mounting Hole Diameter: 2.5mm / 0.1"  
- Screen: 23mm x 35mm / 0.9" x 1.4"  
- Weight: 8.5g  
- This board/chip uses I2C 7-bit address between 0x3C-0x3D, selectable with jumpers  

OLED Display Details:  

- Diagonal Screen Size：1.30"  
- Number of Pixels：128 × 64  
- Color Depth：Monochrome (White)  
- Module Construction：COG  
- Module Size (mm)：34.50 x 35.00  
- Panel Size (mm)：34.50 x 23.00 x 1.45  
- Active Area (mm)：29.420 x 14.70  
- Pixel Pitch (mm)：0.23 x 0.23  
- Pixel Size (mm)：0.21 x 0.21  
- Weight (g)：2.18  
- Duty：1/64  
- Brightness ( cd/m2)：100 (Typ) @ 12V  
- Display current draw is completely dependent on your usage: each OLED LED draws current when on so the more pixels you have lit, the more current is used. They tend to draw ~25mA or so in practice but for precise numbers you must measure the current in your usage circuit  

#### Clavier 16 touches
##### Chez Aliexpress
<http://www.aliexpress.com/item-img/Raspberry-Pi-Model-B-B-TTP229-LSF-Detector-Controller-Capacitive-Touch-Keypad-Supports-Up-To-16/32244629626.html#> --> 9.99$  

##### Chez Alibaba
<https://www.alibaba.com/product-detail/TTP229-Capacitive-Touch-Keypad-16-Keys_60587894432.html> (par 10 minimum!!)  


#### Carte SD 16GO (avec image RaspBian)
MicroSD!!  
Fabricant conseillé?  

#### Micro
Fabriqués par Knowles, ces capteurs sont identiques à ceux des détecteurs du commerce (modèles electret de la série FG ou modèles MEMS).  

##### Chez Knowles
<http://www.knowles.com/eng/Newsroom/New-product-Ultrasonic-MEMS-Microphone>: SPH0641LU4H-1  
Information: `The new MEMS microphone can receive ultrasonic sound waves above the audible range of humans, up to 80 kHz` mais d'après un post du forum: `[]...micro MEMS (SPU0410LR5H-QB de chez Knowles) spécifié jusqu'à 80kHz et qui reste intéressant au-delà`.  


#### Amplificateur audio sur la sortie ligne ou casque sur la sortie casque
N'importe?  

#### Clé USB
N'importe?  

#### Batterie LiIon
Le dispositif a une autonomie de plusieurs nuits, 2 nuits pour une batterie de 6600mAh.  

#### Case
A bricoler sois-même à partir de boîtiers électroniques classiques. Il faut pouvoir découper des fenêtres pour l'écran OLED, le clavier 16 touches, l'accès vers le connecteur USB, la fiche Jack et tous les trous pour faire passer les vis de fixation.  
Trouvé un boîtier tout fait: <http://www.uugear.com/product/acrylic-case-for-witty-pi-and-raspberry-pi-clear/>, c'est probablement pas l'idéal pour faire tous les trous...  

### Autres éléments matériels (cf. document Platine J2)
Info du forum: La réalisation de cet ensemble est effectuée à partir des éléments ci-dessous (le fournisseur est donné à titre d'exemple):  

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



