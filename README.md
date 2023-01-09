# Vaja8-I2C-ADS1115-STM32F0

2.c)V kategorijiConnectivityizberite in omogočite I2C komunikacijo. Kateri pini se aktivirajo? _____ in _____. Koliko različnih I2C komunikacij vaša razvojna plošča omogoča? _____.


d)Glede na dokumentacijo (glejte PDF, stran 17, tabela 5), fizično povežite pin ADDR tako, da bo ADC1115 imel naslov 1001000.

e)Sedaj ADS1115 modul povežite z ustreznimi pini na STM32F0. Ne  pozabite  na  upore  in  kondenzator. Katere pine ste izbrali? Dopolnitetabelo:ADS 1115:SCLSDAADDRALRTVDDSTM32F0:(ni povezan)5 Vali 3.3 VPomagajte si s spodnjo shemo (I2C Master je vaša STM32F0ploščica!):

f)V Parameter  Settings protokola  I2Cspremenite Speed  Mode naFast. Koliko znaša sedaj frekvenca?______________.

g)Sedaj  generirajte  kodo  tako,  da  enostavno  kliknete  ikono Savein po potrebi še enkrat potrdimo generiranje kode. 


3.Programiranje vIDE:
a)V skrajno levem oknu Project Explorer poiščemo main.cdatoteko pod Core→Src→main.c(dvokliknite na datoteko, odpre se tekstovni urejevalnik za main.c). 

b)Pretvorite binarni naslov 1001000v šastnajstiškega: ____ HEX.

c)V User code begin 0deklariramo naslov (slave) ADS1115 pretvornika:#define ADS1115_ADDRESS 0x??Vprašaje v rdečem zamenjajte z ustreznim HEX naslovom, ki ste ga izračunali v b). 

d)Deklariramo še:unsigned char ADSwrite[6];int16_t reading;float voltage[4];

e)ADS    pretvorniku moramoprogramsko    nastavitivhodno ojačanjev    konfiguracijskem    registru(programmable gain amplifier configuration).Ker so naše vrednosti na potenciometru do 3.3V, moramo ustrezno postaviti 16 bitni register tako, da bo lahko meril to vrednost. Bite od 11:9 postavimo na 000, zato je max. napetost ±__.____V.   (glej PDF, str. 19). Deklariramo še ustrezno spremenljivko za pretvorbo:const float voltageConv = ?.???/32768.0;Vprašajezamenjajte s prej dobljeno max.napetostjo iz PDFdokumentacije.

f)V User code begin 3nastavimo registerpretvorbein konfiguracije(Conversionand Configregister, PDF str. 19), spodnjo kodo prepišite in ustrezno zamenjajte ??.
