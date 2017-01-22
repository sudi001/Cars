# Autó Navigátor

## **Követelményanalízis**
-----------------------

A beadandó célja egy kis webes alkalmazás elkészítése szerveroldali technológiák segítségével. A feladatnak minimálisan tartalmaznia kell:

- az órai munkától jelentősen el kell térnie
- legalább négy modellt, legyen bennük egy-sok és sok-sok kapcsolatban álló reláció is.
- legalább három tábla adatait szerkeszteni kell tudni: lista, új, módosít, töröl (vagy inaktívvá tesz)
- legyenek benne csak hitelesítés után elérhető funkciók (autentikáció)
- ügyelni kell, hogy csak a megfelelő adatokhoz férjen hozzá a megfelelő felhasználó (autorizáció)


## Funkcionális követelmények
 - Vendégként a főoldalon szeretnék autókat látni kategóriánként.
 - Vendégként szeretnék az autók között szabadon böngészni.
 - Vendégként szeretnék egy autóleírást megtekinteni.
 - Vendégként szeretnék autót keresni.
 - Vendégként szeretnék tudni regisztrálni az oldalra.
 
 - Felhasználóként szeretnék tudni bejelentkezni az oldalra.
 - Felhasználóként szeretném tudni a profiladataimat szerkeszteni.
 - Felhasználóként szeretnék az autók leírásához hozzászólni és értékelni azokat.
 
## Nem funkcionális követelmények 
 - Felhasználóbarát, ergonomikus elrendezés és kinézet.
 - Gyors működés.
 - Biztonságos működés: jelszavak tárolása, funkciókhoz való hozzáférés.  

## Használatieset-modell

Az alkalmazásban a felhasználóknak személygépjárművek adatainak a megtekintésére van lehetőségük. Az oldal használatához registrációra nincs szükség. Azonban regisztráció estén lehetőség van új gépjármű felvételére – márka, típus, évjárat, motor és kategória mezők kötelező megadásával. Az autók kategóriákba sorolhatóak, így meg lehet jeleníteni a csak egy kategóriába tartozó autókat. Csak az adminnank van jogosltsága gépjerművek törlésére.

## Szerepkörök
- vendég: Az a felhasználó, aki azonosítatlanul használja az alkalmazást. A weben a legtöbb látogató ilyen. A vendég felhasználó csak a publikus oldalakat és funkciókat érheti el. Ilyenek a főoldal, a rólunk és az autós listák, a bemutató oldal, valamint a bejelentkezés és regisztráció.
- bejelentkezett, azonosított felhasználó: a bejelentkezett felhasználók a publikus oldalakon kívül az autókhoz véleményt írhatnak és értékelhetik azokat, továbbá.
- adminisztrátor: a felhasználói adatokat módosítani képes felhasználó, új autókat tud hozzáadni, módosítani és meglévőket törölni.

## Tervezés


### Végpontok

 - GET /: főoldal
 - GET /login: bejelentkező oldal
 - POST /login: bejelentkezési adatok felküldése
 - GET /profile: profiladatok
 - GET /autok: autólista
 - GET /autok/id: autó megtekintése
 - GET /autok/create: új autó felvitele, űrlap megjelenítése
 - POST /autok/create: új autók felvitele, adatok küldése
 - GET /films/edit: autók szerkesztése, űrlap megjelenítése
 - POST /films/edit: autók szerkesztése,  adatok küldése
 - POST /films/delete: autók törlése, adatok küldése
 
### Oldalvázlat
#### Főoldal:

![enter image description here](http://kepfeltoltes.hu/161016/Home_www.kepfeltoltes.hu_.jpg)

#### Autentikáció után elért oldal:

![enter image description here](http://kepfeltoltes.hu/161016/Lista_www.kepfeltoltes.hu_.jpg)

![enter image description here](http://kepfeltoltes.hu/161016/_rt_kel_s_www.kepfeltoltes.hu_.jpg)

#### Vendégként megtekintett oldal:

![enter image description here](http://kepfeltoltes.hu/161016/Guest_www.kepfeltoltes.hu_.jpg)


### Szekvencia diagram

![enter image description here](http://kepfeltoltes.hu/161016/Szekvencia_www.kepfeltoltes.hu_.png)

### Adatmodell
![enter image description here](http://kepfeltoltes.hu/161016/Adatmodell_www.kepfeltoltes.hu_.png)

### Szerepkörtől független UseCase diagram
![enter image description here](http://kepfeltoltes.hu/161016/UseCase_www.kepfeltoltes.hu_.png)

**Selenium IDE használata**
 > --Telepítés után a Ctrl+Alt+S kombminációval indíthatjuk el az IDE-t a Firefox böngészőben. Ha elindítottuk az alkalmazást, akkor a zöld nyíllal futtathatjuk a teszteket, ami a képen jelölve van. A tesztek a test alkönyvtárban találhatóak.
 


