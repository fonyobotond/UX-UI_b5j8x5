---
week: 08
neptun: b5j8x5
---

# Nyolcadik házi feladat

https://www.figma.com/proto/zwSHGYI5rLHZtQqPhMpsZ9/UX-projekt---7-8-User-flow--st%C3%ADlus?node-id=2-2&p=f&t=TctNu67Xnrpo6xzF-0&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=2%3A2

## Mit készítettem a héten

Ezen a héten a projekt használhatósági tesztelését végeztem el. Összeállítottam egy teszttervet, majd három releváns felhasználó bevonásával vizsgáltam meg, mennyire ésszerű a kivilágított pályák keresése és a meglévő meccsekhez való csatlakozás. A tesztek során megfigyelési jegyzeteket készítettem, rögzítettem a felhasználók elakadásait és észrevételeit, majd ezekből súlyossági sorrendbe állított hibákat fogalmaztam meg, és elkészítettem a kutatás részletes szöveges dokumentációját.

### Megoldás összefoglalása

A tesztelés során feltárt leletek alapján frissítettem a prototípust, hogy orvosoljam a felmerült érthetőségi és hozzáférhetőségi problémákat. A "Csatlakozás" és "Véglegesítés" gombokat élénk narancssárga színűre cseréltem a megfelelő kontraszt és láthatóság érdekében. Vizuálisan egyértelműen elkülönítettem az aktív meccseket és az üres pályákat jelző térképtűket, a nehezen észrevehető szűrőt pedig egy kiemelt gombba helyeztem át.

---
## 1) Tesztterv
**Tanulási célok**
- Kideríteni, hogy a felhasználók maguktól megtalálják-e a térképen a szűrőket
- Tesztelni, mennyire egyértelmű a csatlakozás egy már meglévő csapathoz/meccshez a "csapattárskereső" funkción keresztül.

**Résztvevők leírása**
- 18–35 év közötti fiatalok, akik legalább alkalmanként kosárlabdáznak, és használnak okostelefonos térképes alkalmazásokat. Feltétel, hogy a prototípust még sosem látták korábban.

**Feladatok forgatókönyvvel**
- Pályakeresés: „Képzeld el, hogy este 8 óra van, és szeretnél dobálni egyet a közeledben. Keress a térképen egy olyan utcai kosárpályát, ahol van világítás, és nyisd meg az adatlapját!”
- Csatlakozás: „Egyedül vagy, de szívesen játszanál egy 3v3 meccset másokkal. Keress egy olyan aktív eseményt a térképen vagy a listában, ahol még hiányzik játékos, és jelezd a csatlakozási szándékodat!”

**Sikerkritérium, mérőszámok**
- A felhasználó külső segítség nélkül eljut a pálya adatlapjáig, illetve a sikeres csatlakozást visszaigazoló képernyőig.
- Sikeresen befejezett feladatok aránya, valamint az elakadások és téves kattintások száma feladatonként.

## 2) Hozzájáruló nyilatkozat

„Szia! Nagyon köszi, hogy rászánod az időt a projektemre. Egy elég korai verziót fogsz látni, úgyhogy messze nem tökéletes még. Fontos, hogy itt magát a felületet teszteljük, szóval nyugodtan mondd, ha valami nem egyértelmű. Arra kérnélek, hogy közben gondolkodj hangosan: mondd el, mit próbálsz épp megcsinálni, és miért oda kattintasz, ahova. A tapasztalatokat a beadandómhoz használom majd fel, természetesen név nélkül. Kezdhetjük?"

## 3) Megfigyelési jegyzetek

|Feladat|Megfigyelés|Idézet|Értelmezés|
|---|---|---|---|
|Pályakeresés - Világítás|A főképernyőn rögtön a térképen kezdett kattintgatni a szűrő ikon helyett. Több téves kattintás után vette észre az világítás ikont.|"Azt hittem, ha rányomok egy pályára, ott írja ki rögtön, hogy van-e lámpa. A szűrő ikon kicsit beleolvad a fejlécbe."|Az ikon feltűnősége gyenge, a felhasználó figyelme a térkép közepére fókuszál.|
|Csatlakozás|Sikeresen megtalálta a meccs adatlapját, görgetett lefelé, de másodpercekig megakadt, mielőtt rányomott a "Csatlakozom" gombra.|"Hol tudok belépni? Ja, itt ez a szürke gomb lent. Azt hittem, ez inaktív, mert annyira halvány a színe."|A fő gombok színkontrasztja nem megfelelő.|
|Csatlakozás|Az alsó navigációs sávban a "Profil" ikonra kattintott, hogy ott keressen meccseket, majd visszalépett a Térkép nézetre. Végül a "Lista" nézetre váltva találta meg a nyitott meccseket.|"Logikusabbnak tűnt a térképen keresni, de a sok ikon miatt átláthatatlan volt, hogy hol van épp meccs és mi csak egy üres pálya."|A térképen lévő pinek nem különböztetik meg egyértelműen az üres pályákat és az aktív, játékost kereső eseményeket.|

## 4) Leletek súlyossági sorrendben, javítások indoklással

**Súlyos lelet**
- Csatlakozás gomb láthatósága és kontrasztja
- A tesztelő nem vette észre azonnal a gombot, és inaktívnak hitte a a halvány színe miatt
- A felhasználó nem tudja végrehajtani a fő funkciót
- A "Csatlakozom" gomb hátterét élénk színűre, a szöveget pedig fehérre állítom

**Közepes lelet**
- Térkép pinek megkülönböztetése
- A tesztelő nem tudta megkülönböztetni a térképen az üres pályákat az aktívaktól
- Túl sok időt vesz igénybe a keresgélés, sok hibás kattintáshoz vezet
- Az aktív meccseket jelző pineket vizuálisan kiemelem, az üres pályáké pedig egyszerű, kisebb pöttyök maradnak

**Kisebb lelet**
- Szűrő ikon vizuális hierarchiája
- Az szűrő ikon túlságosan beleolvadt a háttérbe
- Plusz kattintások, nehezített és lassabb navigáció a térképen
- A szűrő ikont egy különálló gombba helyezem át a képernyő alsóbb vagy jobban látható részére, így az elem kiemelkedik a felületből
