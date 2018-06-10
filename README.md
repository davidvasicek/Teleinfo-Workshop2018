# Teleinfo-Workshop2018

## Arduino

Arduino [čti Arduíno] je v informatice název malého jednodeskového počítače založeného na mikrokontrolerech ATmega od firmy Atmel. Svým návrhem se snaží podpořit výuku informatiky ve školách a seznámit studenty s tím, jak jsou pomocí počítačů řízena různá zařízení (např. mikrovlnná trouba, automatická pračka a jiné stroje). Nejedná se tedy o počítač ve smyslu stolního počítače nebo chytrého telefonu. Nelze proto k němu snadno přímo připojit monitor ani klávesnici či myš, ale je připraven na připojení LED diod, displeje z tekutých krystalů, servomotorů, senzorů, osvětlení atd. [1]

### Hardware

- **ESP32 Development Board** - ESP32 Development board vývojová deska pro Arduino [e-shop](https://arduino-shop.cz/arduino/1581-esp-32s-esp32-development-board-2-4ghz-dual-mode-wifi-bluetooth-antenna-module-1493028819.html)
- **DHT11 - digitální teploměr a vlhkoměr** - Modul pro měření teploty a vlhkosti. [e-shop](https://arduino-shop.cz/arduino/829-arduino-teplomer-a-vlhkomer-digitalni-1500635986.html) | [návod](http://navody.arduino-shop.cz/navody-k-produktum/teplotni-senzor-dht11.html   ) | [datasheet](https://arduino-shop.cz/docs/produkty/0/133/1500635986.pdf)
- **BH1750** - Modul pro měření měření intenzity světla. [e-shop](https://arduino-shop.cz/arduino/902-arduino-mereni-intenzity-svetla-1420672425.html) | [návod](http://navody.arduino-shop.cz/navody-k-produktum/arduino-mereni-intenzity-svetla.html) | [datasheet](https://arduino-shop.cz/docs/produkty/0/465/1420672425.pdf)
- **Půdní Vlhkoměr** - Modul pro detekci vlhkosti půdy. [e-shop](https://arduino-shop.cz/arduino/1399-pudni-vlhkomer-modul-pro-arduino-1474354607.html) | [návod](http://navody.arduino-shop.cz/navody-k-produktum/pudni-vlhkomer.html) | [datasheet](https://arduino-shop.cz/docs/produkty/0/102/1474354607.pdf )
- **Zvukový senzor** - Modul pro měření hladiny zvuku ve svém okolí. [e-shop](https://arduino-shop.cz/arduino/1358-modul-mikrofonu-s-analogovym-vystupem-pro-arduino-vysoka-citlivost-1467272055.html?gclid=EAIaIQobChMIn8D-sN652wIVCYjVCh0TIwfXEAQYAyABEgLXYfD_BwE) | [návod](http://navody.arduino-shop.cz/navody-k-produktum/modul-mikrofonu-s-analogovym-vystupem.html) | [datasheet](https://arduino-shop.cz/docs/produkty/0/89/1467272055.pdf)
- **LED pásek** - [e-shop](https://www.gme.cz/led-pasek-60led-m-cool-white-4-8w-m-ip20-3m)
- **MOSFET TIP120** - [e-shop](https://www.gme.cz/darlingtonuv-tranzistor-tip120-to220)
- **Síťový napájecí adaptér 12V** - Wattáž volena dle délky LED pásku. např. 1,5A .. [e-shop](https://www.gme.cz/napajeci-adapter-sitovy-12v-1500ma-5-5-2-1mm-b-vigan)
- **Vodiče, jumpers** - [e-shop F-F + F-M + M-M](https://arduino-shop.cz/arduino/1314-sada-dupont-vodicu-120-kusu-mm-ff-mf-3-druhy-1464646471.html) | [e-shop F-F](https://arduino-shop.cz/arduino-kabelaz-propoje-rozsireni/835-arduino-vodice-samice-samice-40-kusu-1500635965.html) | [e-shop F-M](https://arduino-shop.cz/arduino-kabelaz-propoje-rozsireni/1214-arduino-vodice-samice-samice-40-kusu-1457705007.html) | [e-shop M-M](https://arduino-shop.cz/arduino-kabelaz-propoje-rozsireni/1063-arduino-vodice-samec-samec-40-kusu-1500635966.html) 
- **Kontaktní nepájivé pole** - [e-shop](https://www.gme.cz/nepajive-kontaktni-pole-zy-204) 

### Software

Open-source software Arduino IDE umožňuje snadné psaní kódu a jeho nahrávání na desku. Spouští se na systémech Windows, Mac OS X a Linux a jeho prostředí je napsáno v jazyce Java a je také založeno na zpracování a jiném open-source softwaru.
Tento software lze použít s libovolnou deskou Arduino.

1. **Stažení a instalace softwaru Arduino IDE** - Software Arduino IDE je dostupný na oficiálních stráchkách společnosti Arduino [Download zde](https://www.arduino.cc/en/main/software). 

2. **Instalace čipu ESP32** - Samotný software Arduino IDE neobsahuje podporu desek s čipy ESP32, proto je nutné tuto podporu doinstalovat. Využijeme návodu vytvořeného společností Arduino-shop [Návod zde](http://navody.arduino-shop.cz/navody-k-produktum/vyvojova-deska-esp32.html).

3. **Připojení desky s PC** - Desku ESP32 Development Board připojte s PC. V sotwaru Arduino IDE zvolte Nástroje -> Port a zvolte port, ke kterému jste vaší desku připojili. Následně v Nástroje -> Vývojová deska zvolte desku, pro kterou budete vyvíjet. V našem případě se jedná o desku *ESP32 Dev Module*.

4. **Instalace knihoven** - Návod, jak knihovny do prostředí Arduino IDE implementovat nalezneme [zde](http://navody.arduino-shop.cz/zaciname-s-arduinem/arduino-knihovny.html). Pořebné knihovny: **DHT** [Download](https://github.com/adafruit/DHT-sensor-library), **BH1750** [Download](https://github.com/claws/BH1750), **ArduinoJson** [Download](https://github.com/bblanchon/ArduinoJson)

### Zapojení

![zapojeni](https://github.com/davidvasicek/Elektronicke-zabezpecovaci-systemy---EZS/blob/master/img/Zapojeni1.png)

Schéma zapojení bylo vytvořeno v open-source software Fritzing. Tento software můžeme stáhnout ze stránek [http://fritzing.org/download/](http://fritzing.org/download/). Všechny použité komponenty hardwaru, které musely být do tohoto programu importovány naleznete [zde TODO]()

### Kód

Kód projektu pro ESP32 stáhneme z následujícího odkazu. [Arduino.ino TODO]()

Základní struktura kódu se zkládá ze dvou hlavních funkcí. Z funkce *Setup* a funkce *Loop*, které se spouští automaticky po inicializaci knihoven a globalních proměnných. Funkce Setup se spouští po každém zapnutí nebo resetování desky Arduino pouze jednou a slouží k inicializaci proměnných, definování režimů pinů, volání knihoven apod. Funkce Loop, jak už její název napovídá bude prováděna automaticky, což umožňuje arduinu reágovat na změny a provádět požadované úkony. 

Kromě základních funkci Setup a Loop, obsahuje kód také funkce jako jsou connectToWiFi a WiFiEvent které jsou určeny pro čipy ESP32 a jsou součásti ukázkových kódu pro WiFi s čipy ESP32. 

Pokud bychom si měli popsat funkčnost samotného celého programu, funkčnost bude následující. Po spuštění kódu program prvně načte veškeré poptřebné knihovny, definuje čísla pinů jednotlivých připojených senzorů, ale především definuje heslo a SSID WiFi sítě, ke které se bude zařízení připojovat. Tyto údaje jsou důležité pro inicializaci WiFi spojení s AP naší domácí sítě a získání IP adresy DHCP serverem. Tato inicializace se spouší ve funkci Setup voláním funkce connectToWiFi s předáním parametrů SSID sítě a hesla. Tato funkce prvně odstraní veškeré staré konfigurace, registruje nového posluchače na události ve změně stavu sítě, inicializuje spojení a po sériové lince vypíše zprávu *"Waiting for WIFI connection..."*. V této chvíli se již čeká na námi registrovaného posluchače WiFiEvent, který naslouchá změnám stavu WiFi sítě, dokud mu není přidělena IP adresa. Po přidělení adresy se inicializuje přenost paketů pomocí protokolu UDP, změní se stav proměnné *connected* z false na true a zavolá se funkce sendBroadcastMessage. Tato funkce slouží k vytvoření broadcastu z naši získané lokální adresy, na který je následně odeslán UDP packet se zprávou "Hello server", kterou se snaží najít server v síti, kterému může zasílat veškerá svá data. 

Ve chvíli, kdy máme změněný status u coonected na true, může začít probíhat samotná smyčka. Ta v cyklu v prvé řadě kontroluje příchozí paket na svém otevřeném portu, který jsme definovali v globalních proměnných a následně vykoná zbytek svého kódu v cyklu. V tomto zbytku kódu docházi ke čtení dat z připojených senzů a nasldným odesíláním těchto získánych dat serveru. Nicméně, tento zbytek kódu se neprovede do chvíle, dokud nedostaneme UDP packet od hledaného serveru, který jsme zprávou "Hello server" žádali o zaslání jeho adresy. Ve chvíli, kdy nám server odpověděl, získá se jeho adresa, na kterou je opětovně zaslaná zpráva s registračními údaji a informacemi o našem zařízení v podobě JSON objektu. Ve chvíli, kdy známe adresu našeho serveru a zařízení mám u serveru registrováno, můžeme začít zasílat jednotlivé údaje ze senzorů. Ty se odesílají každých 3000 ms v podobě JSON objektu. Tyto objekty již zpracovává samotný server, který si popíšeme v další části tutoriálu. 

















https://www.arduino.cc/reference/en/
https://arduino.cz/zaciname-s-arduinem/


