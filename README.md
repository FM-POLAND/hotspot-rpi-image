Eksperymentalny obraz FM POLAND Raspberry PI Zero oraz 2/3/4 dla opisu na stronie: http://fm-poland.pl/budowa-hotspota/

Obraz o nazwie fmpoland-rpi.img.xz nagrać na kartę microSD (8 Gb lub większa) przy pomocy: https://etcher.balena.io/

Login do konsoli via ssh:

user: pi

hasło: fmpoland

Dostęp do dashboard:

http://hotspot-fmpl.local

lub

http://ip_adres

Konfiguracja via Dashboard, należy wybrać z menu "Admin" i nastepnie: 

"SQL PTT" - ustawienia sprzetowe SQL i PTT oraz Hidraw dla CM108

"SVXCnf" - konfiguracja konta FM POLAND

"NodeInfo" - Informacje o stacji

"WEBCnf" - konfiguracja Dasboard

oraz inne opcje stosownie do potrzeb

CZYTAJ uważnie informacje umieszczone w każdym oknie z seri administracyjnych
w których są istotne informacje do dostępnych ustawień

![Admin Menu](https://github.com/FM-POLAND/hotspot-rpi-image/blob/main/admin-menu.png)

Obraz ten można używać z produktami SHARI i SHARI PiHat https://kits4hams.com/shari


Domyślnie obraz przygotowany do pracy z modyfikowaną karta dźwiękową CM108 czyli
między innymi dla hotspotów na bazie SHARI, HotspotRadios z modułami SA818

Dostępne konfiguracje:

Konfiguracja dla zmodyfikowanej karty CM108, sterowanie SQL i PTT via gpio CM108
czyli dal hotspotów na bazie SHARI, HotsporRadios z modułami SA818: 

/etc/svxlink/svxlink-cm108-mod.conf   

Konfiguracja dla niezmodyfikowanej karty CM108 i sterowanie via GPIO RPI dla SQL i PTT:

/etc/svxlink/svxlink-gpio.conf        

Należy zalogować się via SSH do RPI i skopiować wybrną konfiguracje na nazwę svxlink.conf i następnie konfigurować via Dashboard
z menu "Admin"

Przykład:

sudo cp /etc/svxlink/svxlink-gpio.conf /etc/svxlink/svxlink.conf

lub

sudo cp /etc/svxlink/svxlink-cm108-mod.conf /etc/svxlink/svxlink.conf

![Raspberry](https://github.com/FM-POLAND/hotspot-rpi-image/blob/main/rpi-login.png)

.


