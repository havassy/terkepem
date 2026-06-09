# Térképem

A Térképem egy böngészőben futó, térképes földrajzi kvíz. A felhasználó saját helylistát tölthet be, majd a program a térképen kattintva kérdezi vissza az egyes helyek pozícióját.[file:2]

## Mit tud a program?

- Saját helylista betöltése CSV-fájlból vagy beillesztett szövegből.[file:2]
- KML/XML alapú helyadatok beolvasása.[file:2][file:1]
- Demóadat gyors kipróbáláshoz.[file:2][file:1]
- Kvíz véletlen sorrendben vagy betöltési sorrendben.[file:2][file:1]
- Állítható találati küszöb kilométerben.[file:2]
- Több alaptérkép közötti váltás.[file:2][file:1]
- A helyes válasz megjelenítése.[file:2]
- Újrakezdés, amely törli a betöltött adatokat és visszaállítja a kezdő állapotot.[file:2]
- Témaszűrés típus szerint: ország, város, folyó, tó, hegység, hegy, sziget, régió, megye, egyéb.[file:1]
- Névcímkék ki- és bekapcsolása, minimum zoomszinthez kötve.[file:1]
- Beépített súgó a használathoz és az adatelőkészítéshez.[file:1]

## Támogatott adatforma

A program a legbiztosabban a következő CSV-formátumot kezeli:[file:2][file:1]

```text
name,latitude,longitude,type
Magyarország,47.1625,19.5033,ország
Budapest,47.4979,19.0402,város
Balaton,46.8300,17.7200,tó
Duna,45.2700,28.9700,folyó
Kékes,47.8720,20.0080,hegy
Mátra,47.8700,20.0000,hegység
```

Kötelező oszlopok:[file:2]

- `name` – a hely neve.[file:2]
- `latitude` – földrajzi szélesség decimális fokban.[file:2]
- `longitude` – földrajzi hosszúság decimális fokban.[file:2]
- `type` – a hely típusa, például ország, város, folyó, tó, hegység, hegy, sziget, régió, megye vagy egyéb.[file:2][file:1]

## Használat

1. Tölts fel egy `.csv`, `.kml` vagy `.xml` fájlt, vagy illeszd be a CSV tartalmát.[file:2]
2. Szöveges bemenet esetén kattints a „Beillesztett adat betöltése” gombra.[file:2]
3. Szükség esetén válassz témaszűrést és egyéb beállításokat.[file:1]
4. Indítsd el a kvízt a „Kvíz indítása” gombbal.[file:2]
5. Kattints a térképre ott, ahol szerinted a keresett hely található.[file:2]
6. A program megmutatja a távolságot, a pontosságot és a helyes választ.[file:2]

## Adatelőkészítés

A legegyszerűbb megoldás, ha a gyakorolni kívánt helynevekhez egy MI segítségével készítesz egységes CSV-listát a fenti oszlopokkal.[file:2][file:1] A részletes mintaprompt a program beépített súgójában található, ezért itt nem szerepel külön.[file:1]

## Megjegyzések

- A program a hibás vagy hiányzó koordinátás sorokat kihagyhatja.[file:2][file:1]
- Az MI által adott koordináták nem mindig pontosak, ezért érdemes ellenőrizni őket térképen.[file:2][file:1]
- Folyók, hegységek, régiók és más nagy kiterjedésű objektumok esetén különösen fontos az ellenőrzés.[file:2]
- Első próbához érdemes 5–15 helyből álló listát használni.[file:2]
- Gyors teszthez használható a beépített „Demóadat” gomb.[file:2][file:1]
