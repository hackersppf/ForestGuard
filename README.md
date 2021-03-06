# ForestGuard

Το σύστημα που προτείνουμε έχει ως βασικό σκοπό την άμεση αντιμετώπιση των δασικών πυρκαγιών πριν πάρουν μεγάλες διαστάσεις και γίνουν απειλητικές για ανθρώπους και περιουσίες. Η καταστροφή που έγινε στο Μάτι της Αττικής το 2018 αποτέλεσε το έναυσμα για την ιδέα μας.

Το σύστημα μας αποτελείται από τρία μέρη:

-   Κέντρο ελέγχου
-   Drone επιτήρησης
-   Αυτόνομο όχημα αντιμετώπισης φωτιάς
## Κέντρο ελέγχου

Το κέντρο ελέγχου θα είναι ένας υπολογιστής ο οποίος θα μπορεί να συνδεθεί τόσο με το όχημα αντιμετώπισης της φωτιάς (μέσω bluetooth) όσο και με το Drone επιτήρησης (μέσω wifi και Python).

## Drone επιτήρησης

Θα αξιοποιήσουμε ένα Drone DJI tello που διαθέτουμε στο εργαστήριο μας και το οποίο μπορεί να προγραμματιστεί με την γλώσσα Python και την βιβλιοθήκη OpenCV για να αξιοποιήσει την κάμερα του με τεχνητή νοημοσύνη. Το Drone κάνει επιτήρηση στο δάσος από ψηλά και όταν αντιληφθεί φωτιά ειδοποιεί το κέντρο ελέγχου. Η ανίχνευση της φωτιάς γίνεται από την κάμερα του drone χρησιμοποιώντας τη γλώσσα python και την βιβλιοθήκη OpenCV. Το κέντρο ελέγχου στέλνει σήμα στο όχημα αντιμετώπισης της φωτιάς, μαζί με το σημείο στο οποίο βρίσκεται (αν βρίσκεται βόρεια, νότια, δυτικά ή ανατολικά από τον σταθμό του οχήματος).

## Όχημα αντιμετώπισης φωτιάς

Το όχημα μας αποτελείται από ένα Microbit μαζί με την πλατφόρμα Maqueen Plus, την κάμερα ΤΝ HuskyLens και μια δεξαμενή νερού με αντλία. Επίσης περιλαμβάνει στο μπροστά μέρος εξάρτημα απομάκρυνσης εμποδίων με την χρήση ενός κινητήρα servo. Όταν λάβει το σήμα από  
το κέντρο ελέγχου ξεκινάει να κατευθυνθεί προς την φωτιά αξιοποιώντας την πυξίδα του Microbit και τις πληροφορίες από το drone για την θέση της φωτιάς. Για τον ακριβή εντοπισμό της χρησιμοποιεί την κάμερα ΤΝ που διαθέτει. Αν συναντήσει εμπόδια τα απομακρύνει με τον μηχανισμό που έχει στο μπροστά μέρος. Μόλις φτάσει κοντά στην φωτιά ενεργοποιεί την αντλία νερού μέχρι να σβήσει η φωτιά (κάμερα ΤΝ).

## Λίστα υλικών που θα χρειαστούμε

-   [Funduino](https://grobotronics.com/funduino-uno-rev3-arduino-uno-compatible.html) - κόστος 12 ευρώ
-   [HuskyLens](https://www.hellasdigital.gr/electronics/sensors/gravity-huskylens-an-easy-to-use-ai-machine-vision-sensor/) – κόστος 56 ευρώ
-   [Αισθητήρας Φωτιάς 5 Channels](https://grobotronics.com/flame-sensor-5-ch.html) - κόστος 7 ευρώ
-   [Robot Smart Car 4WD](https://grobotronics.com/robot-smart-car-4wd-chassis-26cm.html) - κόστος 17 ευρώ
-   [Dual Motor Driver Module L298N](https://grobotronics.com/dual-motor-driver-module-l298n.html) - κόστος 5 ευρώ
-   [Relay Module](https://grobotronics.com/relay-module-1-channel-5v-high-level-trigger-screw-terminals.html) - κόστος 2 ευρώ
-   [Mini Brushless Water Pump](https://grobotronics.com/mini-brushless-water-pump-12v-dc-240l-h-ad20p-1230a.html)  – κόστος 7 ευρώ
-   [Bluetooth Module for Arduino](https://grobotronics.com/bluetooth-module-for-arduino-hc05.html) - κόστος 7 ευρώ
-   [Servo Micro](https://grobotronics.com/servo-micro-1.5kg.cm-plastic-gears-feetech-fs90.html) - κόστος 4 ευρώ
-   [800mAh 11.1V 45C 3S1P Lipo Battery Pack](https://www.hellasdigital.gr/electronics/batteries/lipo/gens-ace-800mah-11.1v-40c-3s1p-lipo-battery-pack/) - κόστος 13 ευρώ
-   [12v 2-3S Basic Balance Charger](https://www.hellasdigital.gr/electronics/batteries/chargers/turnigy-12v-2-3s-basic-balance-charger/) - κόστος 12 ευρώ
-   [Πλακέτα Δοκιμών 400 Οπές](https://grobotronics.com/breadboard-400-tie-point-white-half-size.html) - κόστος 3 ευρώ
-   DJI Tello Drone (το έχουμε ήδη στο εργαστήριο μας)
-   [PLA Fillament 1KG](https://grobotronics.com/3d-printer-filament-devil-pla-1.75mm-pink-1kg.html)  – κόστος 22 ευρώ

**Συνολικό κόστος: 167 ευρώ**
![enter image description here](https://ppf.edu.gr/hackers/wp-content/uploads/2021/03/forest-guard.png)
