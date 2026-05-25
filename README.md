# Felhasználói útmutató

A program földrajzi helyekből készít térképes kvízt. Használatához egy egyszerű CSV-adatlista kell, amelyben minden hely külön sorban szerepel.

## Milyen adat kell?

A program a legbiztosabban ezt a formátumot kezeli:

```text
name,latitude,longitude,type
Magyarország,47.1625,19.5033,ország
Budapest,47.4979,19.0402,város
Balaton,46.8300,17.7200,tó
Duna,45.2700,28.9700,folyó
Kékes,47.8720,20.0080,hegy
Mátra,47.8700,20.0000,hegység
```

## Mit jelentenek az oszlopok?

- `name`: a hely neve
- `latitude`: földrajzi szélesség decimális fokban
- `longitude`: földrajzi hosszúság decimális fokban
- `type`: a hely típusa, például ország, város, folyó, tó, hegység, hegy, sziget, régió, megye, egyéb

## Hogyan készíthetek ilyen adatot?

A legegyszerűbb megoldás, ha a gyakorolni kívánt földrajzi neveket bemásolod egy MI-nek, és kéred, hogy készítsen belőlük többsoros CSV-t a szükséges oszlopokkal. Ezután a kapott CSV-t bemásolhatod közvetlenül a programba, vagy elmentheted `.csv` fájlként. Ha a CSV-formátumú szöveget bemásolással használod, nagyon fontos, hogy karakterre pontosan másold be, mert egy hiányzó, plusz vagy megváltozott karakter is hibát okozhat, és a program hibát jelezhet.

## Mintaprompt MI-hez

Az alábbi promptot másold be az MI-nek, és a végére írd oda a saját helylistádat:

```text
Készíts egy földrajzi/helyismereti kvízhez használható, tiszta és egységes adatállományt CSV formátumban.

A kimenet kötelező oszlopai:
name,latitude,longitude,type

Szabályok:
- A `name` mezőbe az objektum rövid, egyértelmű magyar neve kerüljön.
- A `latitude` és `longitude` mezőbe decimális fokban add meg a koordinátákat.
- Csak olyan rekord maradjon benne, amelyhez megbízható koordináta tartozik.
- Ha nincs biztos koordináta, inkább hagyd ki a rekordot.
- A `type` mezőt minden rekordnál kötelező kitölteni.
- A `type` mező csak az alábbi értékek egyikét kaphatja:
  ország, város, folyó, tó, hegység, hegy, sziget, régió, megye, egyéb
- Ha az objektum típusa egyértelműen megállapítható, a fenti listából a legjobban illő kategóriát használd.
- Ha nincs megfelelő kategória, vagy a besorolás bizonytalan, akkor a `type` értéke legyen: egyéb
- Ne használj eltérő írásmódokat vagy szinonimákat, például ne írj ilyet: település, varos, nagyváros, county, settlement. Ezek helyett mindig a megadott fix kategóriák egyikét használd.
- Folyók esetén a koordináta a torkolat környékére essen, de ne közvetlenül a tengerparti vagy nyílt vízi találkozási pontra; a pont legyen kissé a folyón felfelé, még egyértelműen a folyó medrében vagy közvetlen folyószakaszán.
- A válasz több soros, valódi CSV legyen, minden rekord külön új sorban szerepeljen.
- Ne szerepeljen magyarázó szöveg, csak a kész CSV.

A válasz kizárólag a kész CSV legyen.

A feldolgozandó helyek:
IDE ÍRD A SAJÁT HELYLISTÁDAT
```

## Példa helylistára

A prompt végére például ezt írhatod:

```text
A feldolgozandó helyek:
Magyarország
Budapest
Balaton
Duna
Kékes
Mátra
Szeged
Tisza
```

## Hogyan töltsd be?

A kapott CSV-t bemásolhatod a program szövegmezőjébe, majd kattints a „Beillesztett adat betöltése” gombra. Ugyanezt `.csv` fájlként is feltöltheted a „Fájl kiválasztása” gombbal.

## Fontos figyelmeztetés

Az MI által megadott koordináták nem mindig pontosak. Különösen folyók, hegységek, régiók vagy nagy kiterjedésű földrajzi objektumok esetén érdemes az adatokat ellenőrizni térképen, mielőtt élesben használod a kvízt.

## Használati tanács

Kezdésnek érdemes 5–15 helyből álló listával próbálkozni. Ha a program nem tud egy sort használni, annak oka általában hiányzó vagy hibás koordináta, vagy rossz CSV-formátum.
