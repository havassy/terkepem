# Térképem

A Térképem egy böngészőben futó, térképes földrajzi kvíz. A felhasználó saját helylistát tölthet be, majd a program a térképen kattintva kérdezi vissza az egyes helyek pozícióját.

## Mit tud a program?

- Saját helylista betöltése CSV-fájlból vagy beillesztett szövegből
- KML/XML alapú helyadatok beolvasása
- Demóadat gyors kipróbáláshoz
- Kvíz véletlen sorrendben vagy betöltési sorrendben
- Állítható találati küszöb kilométerben
- Több alaptérkép közötti váltás
- A helyes válasz megjelenítése
- Újrakezdés funkció, amely törli a betöltött adatokat és visszaállítja a kezdő állapotot

## Támogatott adatforma

A program a legbiztosabban a következő CSV-formátumot kezeli:

```text
name,latitude,longitude,type
Magyarország,47.1625,19.5033,ország
Budapest,47.4979,19.0402,város
Balaton,46.8300,17.7200,tó
Duna,45.2700,28.9700,folyó
Kékes,47.8720,20.0080,hegy
Mátra,47.8700,20.0000,hegység
```

### Kötelező oszlopok

- `name` – a hely neve
- `latitude` – földrajzi szélesség decimális fokban
- `longitude` – földrajzi hosszúság decimális fokban
- `type` – a hely típusa, például ország, város, folyó, tó, hegység, hegy, sziget, régió, megye vagy egyéb

## Használat

1. Tölts fel egy `.csv`, `.kml` vagy `.xml` fájlt, vagy illeszd be a CSV tartalmát.
2. Kattints a **Beillesztett adat betöltése** gombra, ha szöveget használsz.
3. Indítsd el a kvízt a **Kvíz indítása** gombbal.
4. Kattints a térképre ott, ahol szerinted a keresett hely található.
5. A program megmutatja a távolságot, a pontosságot és a helyes választ.
6. Az **Újrakezdés** gombbal minden adat törölhető, és a program visszaáll a kezdő állapotra.

## Adat-előkészítés

A legegyszerűbb megoldás, ha a gyakorolni kívánt helynevekből egy MI segítségével készítesz egységes CSV-listát a fenti oszlopokkal. A bemásolt szöveg legyen pontos, mert egy hibás fejléc vagy elcsúszott mező miatt a program rekordokat hagyhat ki. [cite:1]

### Rövid mintaprompt

```text
Készíts földrajzi kvízhez használható CSV-t az alábbi oszlopokkal:
name,latitude,longitude,type

Szabályok:
- csak megbízható koordinátás rekord maradjon
- a koordináták decimális fokban legyenek
- a `type` mező mindig legyen kitöltve
- a válasz kizárólag valódi CSV legyen

A feldolgozandó helyek:
IDE ÍRD A HELYLISTÁT
```

## Fontos megjegyzések

- A program a hibás vagy hiányzó koordinátás sorokat kihagyhatja.
- Az MI által adott koordináták nem mindig pontosak.
- Folyók, hegységek, régiók és más nagy kiterjedésű objektumok esetén különösen érdemes ellenőrizni az adatokat.
- Első próbához érdemes 5–15 helyből álló listát használni.

## Gyors teszt

Ha csak kipróbálnád az alkalmazást, használd a beépített **Demóadat** gombot.
