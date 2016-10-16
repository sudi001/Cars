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
