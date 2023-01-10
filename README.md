# Vaja8-I2C-ADS1115-STM32F0

2.ODGOVORI NA VPRAŠANJA --> 

--> c)V kategorijiConnectivityizberite in omogočite I2C komunikacijo. Kateri pini se aktivirajo? __PB6___ in __PB7___. Koliko različnih I2C komunikacij vaša razvojna plošča omogoča? __2___.

--> f)V Parameter  Settings protokola  I2Cspremenite Speed  Mode naFast. Koliko znaša sedaj frekvenca?______400kHz________.

3.ODGOVORI NA VPRAŠANJA -->

--> b)Pretvorite binarni naslov 1001000v šastnajstiškega: __48__ HEX.

--> e)ADS    pretvorniku moramoprogramsko    nastavitivhodno ojačanjev    konfiguracijskem    registru(programmable gain amplifier configuration).Ker so naše vrednosti na potenciometru do 3.3V, moramo ustrezno postaviti 16 bitni register tako, da bo lahko meril to vrednost. Bite od 11:9 postavimo na 000, zato je max. napetost ±_6.144_V.

KOMENTAR NA DELOVANJE --> 
Naloga nama ni predstavljala večjih težav. Edina napaka, ki sva jo naredila je bila pri "live expressions" ker sva namesto "voltage" napisala "Voltage". 

--> Slika vezja
![Slika vezja](https://raw.githubusercontent.com/bozoslapy/Vaja8-I2C-ADS1115-STM32F0/main/IMG_0555.jpg)

--> Slika mikroprocesorja
![Slika mikroprocesorja]()

--> I2C okno
![I2C okno]()

--> Posntek delovanja
![Posntek delovanja](https://github.com/bozoslapy/Vaja8-I2C-ADS1115-STM32F0/blob/main/IMG_0553.MOV)
