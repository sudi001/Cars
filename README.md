# cars

## **Követelményanalízis**
-----------------------

A beadandó célja egy kis webes alkalmazás elkészítése szerveroldali technológiák segítségével. A feladatnak minimálisan tartalmaznia kell:

- az órai munkától jelentősen el kell térnie
- legalább négy modellt, legyen bennük egy-sok és sok-sok kapcsolatban álló reláció is.
- legalább három tábla adatait szerkeszteni kell tudni: lista, új, módosít, töröl (vagy inaktívvá tesz)
- legyenek benne csak hitelesítés után elérhető funkciók (autentikáció)
- ügyelni kell, hogy csak a megfelelő adatokhoz férjen hozzá a megfelelő felhasználó (autorizáció)
   
   

## Használatieset-modell

Az alkalmazásban a felhasználóknak személygépjárművek adatainak a megtekintésére van lehetőségük. Az oldal használatához registrációra nincs szükség. Azonban regisztráció estén lehetőség van új gépjármű felvételére – márka, típus, évjárat, motor és kategória mezők kötelező megadásával. Az autók kategóriákba sorolhatóak, így meg lehet jeleníteni a csak egy kategóriába tartozó autókat. Csak az adminnank van jogosltsága gépjerművek törlésére.

## Szerepkörök
- vendég: Az a felhasználó, aki azonosítatlanul használja az alkalmazást. A weben a legtöbb látogató ilyen. A vendég felhasználó csak a publikus oldalakat és funkciókat érheti el. Ilyenek a főoldal, a címke és felhasználó szerinti listák, a bemutató oldal, valamint a bejelentkezés és regisztráció.
- bejelentkezett, azonosított felhasználó: a bejelentkezett felhasználók a publikus oldalakon kívül a saját bemutató lista és a szerkesztési oldalakat is használhatja.
- adminisztrátor: a felhasználói adatokat módosítani képes felhasználó.

## Tervezés

### Végpontok

Az oldal az alábbi végpont-szerkezet alapján épül fel:
- contacts/
  - list A névjegyek megtekintésenew Új névjegy felvételedelete{id} Kiválasztott névjegy törlésemodificate{id} Kiválasztott névjegy módosításaauth/ login Bejelentkezéssignup Regisztrációlogout Kijelentkezésabout Az alkalmazásról szóló információk megtekintése

![enter image description here](http://static1.creately.com/blog/wp-content/uploads/2012/02/UML-Class-Diagram-Example.png)
