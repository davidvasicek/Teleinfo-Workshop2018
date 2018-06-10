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

## Firebase

Firebase je platforma pro vývoj mobilních a webových aplikací vyvinutá firmou Firebase, Inc. v roce 2011 a poté získala společnost Google v roce 2014. [1]

**Firebase Cloud Messaging**

Firebase Cloud Messaging (FCM) je řešení pro zasílání zpráv mezi platformami, které vám umožní spolehlivě doručovat zprávy zdarma.
Pomocí služby FCM můžete upozornit na aplikaci klienta, že jsou k synchronizaci k dispozici nová e-mailová nebo jiná data. Zprávy o oznámení můžete posílat, abyste mohli opětovně zapojit a uchovat uživatele. U aplikací, jako je například instant messaging, může zpráva přenést užitečné zatížení až 4 kB do aplikace klienta.

Používáte službu Google Cloud Messaging již nyní? Další informace o možnostech.

**Realtime Database**

Ukládejte a synchronizujte data s naší databází cloud NoSQL. Data jsou synchronizována ve všech klientech v reálném čase a zůstávají k dispozici, když aplikace zmizí.
Firebase Realtime Database je databáze hostovaná v cloudu. Data jsou uložena jako JSON a synchronizována v reálném čase s každým připojeným klientem. Při vytváření aplikací s více platformami pomocí našich sady iOS, Android a JavaScript SDK sdílí všichni vaši klienti jednu instanci databáze Realtime a automaticky přijímá aktualizace s nejnovějšími daty.

### Založení projektu Firebase

1. **Registrace Google účtu** Abychom mohli plně využívat služeb Firebase, potřebujeme mít platný účet u společnosti Google, Inc. Pokud tento účet nemáme, budeme ho muset v prvé řadě vytvořit. [Registrace zde](https://accounts.google.com/SignUp?continue=https%3A%2F%2Fwww.google.cz%2F%3Fgfe_rd%3Dcr%26ei%3DUXnfWML0IfGv8wfVooPIAg&hl=cs)

2. **Vytvoření nového projektu** na stránkách [https://console.firebase.google.com/](https://console.firebase.google.com/) vytvořte nový projekt kliknutím na tlačítko *Add project*. V dalším kroku vyplňte potřebné údaje a nový projekt vytvořte stisknutím *CREATE PROJEKT*.


**Raspberry Pi** (výslovnost [ˈraːzbəri pai]) je v informatice název malého jednodeskového počítače s deskou plošných spojů o velikosti zhruba platební karty. V roce 2012 byl vyvinut britskou nadací Raspberry Pi Foundantion s cílem podpořit výuku informatiky ve školách a seznámit studenty s tím, jak mohou počítače řídit různá zařízení (např. mikrovlnná trouba, automatická pračka). Primárním operačním systémem je Raspbian. Cena je na konci roku 2016 v rozmezí 150–1 200 Kč (nejlevnější je Raspberry Pi Zero, nejdražší pak Raspberry Pi 3 Model B). Označení „Raspberry Pi“ je registrovanou ochrannou známkou, a proto mají podobně navržené počítače zdánlivě odvozené názvy (např. Banana Pi) [1]

### Instalace OS

**Raspbian** ( anglická výslovnost [raːzbiən] IPA ) je operační systém odvozený od Debianu pro Raspberry Pi i osobní počítače . [2] Je oficiálně poskytován nadací Raspberry Pi Foundation jako primární operační systém pro jednoplášťové počítače z rodiny Raspberry Pi. [1] Raspbian byl vytvořen Mikem Thompsonem a Peterem Greenem jako nezávislý projekt. [5] První sestavení byla dokončena v červnu 2012. [6] Raspbian je vysoce optimalizovaný pro ARM procesory používané v Raspberry Pi. [2]

1. **Stažení operačního systému.** Raspbian je součásti instalačního balíčku zvaného NOOBS, který nalezneme na oficiálních stránkách organizace RaspberryPi [Download zde](https://www.raspberrypi.org/downloads/noobs/). Stáhneme NOOBS ve formátu .zip kliknutím na tlačítko *Download ZIP*.

2. **Příprava Micro SD karty.** Pokud naše karta obsahuje zastaralá data, bude nutné kartu v prvé řadě naformátovat. To provedeme programem zvaným SD Memory Card Formatter [Download zde](https://www.sdcard.org/downloads/formatter_4/).

3. **Kopírování souborů na Micro SD kartu.** Jestliže máme balíček NOOBS stažený a paměťovou kartu naformátovanou, překopírujeme veškeré soubory ze ZIP archívu balíčku NOOBS na paměťovou kartu.

4. **Instalace OS.** Paměťovou kartu vložíme do našeho zařízení Raspberry Pi a připojíme monitor a napájení. Po nabootování paměťové karty se zobrazí nabídka, ve které zaškrtávacím políčkem zvolíme *Raspbian with PIXEL* a stiskem tlačítka *Install* system Raspbian nainstalujeme.

### Prvotní nastavení systému

1. **Připojení k internetu.** 

    - **Kabelové připojení (ETH0):** V případě kabelového ethernetového připojení pouze připojíme datový kabel do zařízení Raspberry Pi. 
    - **Bezdrátové připojení (WLAN0):** Pokud budeme využívat WiFi připojení, nalezneme v grafickém prostředí OS Raspbianu v pravé horní části obrazovky ikonku WiFi, na kterou klikneme, vybereme SSID sítě, ke které se budeme připojovat a vložíme heslo. 
    - **Získáni IP adresy:** Spusťte příkazový řádek a zadejte příkaz `ifconfig`. IP adresu najdeme pod označením *inet*. V případě kabelového připojení v *ETH0*, v případě bezdrátového připojení *WLAN0*.
2. **Povolení protokolu SSH (Secure Shell).** v prostředí OS Raspbianu klikneme v levém horním rohu na ikonu maliny -> Preferences -> Raspberry Pi Configuration -> Interfaces -> SSH: Enable -> OK [Návod zde](https://www.raspberrypi.org/documentation/remote-access/ssh/).
3. **Update a Upgrade systému.** Spusťte příkazový řádek a zadejte příkaz `sudo apt-get -y upgrade`, po dokončení zadejte příkaz `sudo apt-get -y update`
### Instalace repozitářů
Přejděte do příkazového řádku a přihlaste se jako uživatel správce root příkazem `sudo -i`. Pokud nebudete jako správce přihlášeni, budou vám chybět oprávnění k následujícím úkonům.

1. **Instalace FTP**. FTP (File Transfer Protocol) slouží pro přenos souborů mezi Raspberry Pi a jiným počítačem.

    ```
    apt-get install -y vsftpd
    nano /etc/vsftpd.conf 
    	// změťe #write_enable=YES na write_enable=YES
    /etc/init.d/vsftpd restart
    ```
2. **Instalace MariDB.** MariDB je relační databáze, která je komunitou vyvíjenou nástupnickou větví (tzv, „forkem“) MySQL. Hlavním důvodem k vytvoření této větve bylo udržení licence svobodného softwaru GNU GPL. [odkaz10]

    ```
	sudo apt install -y mariadb-server
    ```
	
3. **Instalace Node JS a npm.** Node.js je softwarový systém navržený pro psaní vysoce škálovatelných internetových aplikací, především webových serverů. Programy pro Node.js jsou psané v jazyce JavaScript, hojně využívající model událostí a asynchronní I/O operace pro minimalizaci režie procesoru a maximalizaci výkonu [4]. Npm je správce balíčků pro programovací jazyk JavaScript. [5]
    
    ``` 
	curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
	apt-get install nodejs
	node -v
	npm -v
    ``` 
   
   vytvoření ukázkového skriptu:
    ```
    mkdir /home/pi/nodejs
    cd /home/pi/nodejs
    nano test.js
    	console.log("Hello world");
    node test.js
	``` 
4. **Vytvoření bezdrátového přístupového bodu.** Raspberry Pi může být používán jako bezdrátový přístupový bod, který má samostatnou síť. To lze provést pomocí vestavěných bezdrátových prvků Raspberry Pi 3 nebo Raspberry Pi Zero W nebo pomocí vhodného bezdrátového USB klíče, který podporuje přístupové body. Bezdrátový přístupový bod vytvoříte dle náslodujícího tutoriálu [Tutorial zde](https://www.raspberrypi.org/documentation/configuration/wireless/access-point.md)
	
### Konfigurace projektu
V této fázi máme připravené Raspberry Pi pro samotnou konfiguraci projektu a následující části se proto budeme věnovat postupy konfigurace našeho serveru.

1. **Vytvoření nové databáze a potřebných tabulek.** V příkazovém řádku zadejte příkaz `mysql -u root -p` a zadejte heslo. Pozn.: Heslo jsme volili při instalaci databázového serveru. Při zadávání příkazů nezapomeňte na konci každého příkazu zadat znak středníku.
	``` 
	CREATE DATABASE IoT;  // Vytvoří novou databázi s názvem IoT
	USE IoT;  // Přepneme se do nově vytvořené databáze IoT
	```
	
2.  **Vytvoření nové tabulky ArduinoDevices** - Tato tabulka bude sloužit pro registraci jednotlivých zařízení Arduino, které se na serveru budou registrovat. Obsahuje celkem 4 atributy: 
	
		- **id**: identifikátor záznamů v tabulce
		- **DeviceIP**: IP adresu daného zařízení, abychom jej v síti mohli najít
		- **DeviceID**: jedinečné identifikační číslo daného zařízení (jedná se o MAC adresu zařízení)
		- **Description**: popis zařízení, aby bylo jednodušší zařízení námi identifikovat
         
		```
		CREATE TABLE IF NOT EXISTS ArduinoDevices(
		id INT(20) UNSIGNED PRIMARY KEY NOT NULL AUTO_INCREMENT,
		DeviceIP VARCHAR(100) NOT NULL,
		DeviceID VARCHAR(100) NOT NULL,
		Description VARCHAR(500) NOT NULL
		);
		```
		 
3. **Vytvoření nové tabulky BME280sensors** - Tato tabulka bude slouži pro ukládání záznamů z teplotních a tlakových senzoru BME280, které budou na server odesílat výše registrované zařízení Arduino. Obsahuje celkem 6 atributů:
	
		- id: identifikátor záznamů v tabulce
		- DeviceID: Identifikační číslo zařízení, které data zaslalo
		- Temperature: data o teplotě [°C]
		- Humidity: data o vlhkosti [%]
		- Pressure: data o barometrickém tlaku [hPa]
		- TimeStamp: čas, ve který server data obdržel
	
		```
		CREATE TABLE IF NOT EXISTS BME280sensors(
		id INT(20) UNSIGNED PRIMARY KEY NOT NULL AUTO_INCREMENT,
 		ArduinoID VARCHAR(100) NOT NULL,
 		Temperature FLOAT(3) NOT NULL,
 		Humidity FLOAT(3) NOT NULL,
 		Pressure FLOAT(3) NOT NULL,
 		TimeStamp NUMERIC(20) NOT NULL
		);
		```
	


CREATE TABLE IF NOT EXISTS AndroidDevices(
 id INT(20) UNSIGNED PRIMARY KEY NOT NULL AUTO_INCREMENT,
 Token VARCHAR(200) NOT NULL,
 Device_Name VARCHAR(100) NOT NULL,
 Device_ID VARCHAR(100) NOT NULL
);
	
### Zdroje
- [1] https://cs.wikipedia.org/wiki/Raspberry_Pi
- [2] https://cs.wikipedia.org/wiki/Raspbian
- [3] https://cs.wikipedia.org/wiki/LAMP
- [4] https://cs.wikipedia.org/wiki/Node.js
- [5] https://en.wikipedia.org/wiki/Npm_(software)

odkaz10 - https://cs.wikipedia.org/wiki/MariaDB











https://www.arduino.cc/reference/en/
https://arduino.cz/zaciname-s-arduinem/


