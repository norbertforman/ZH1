# Python Feladat: Állatkert Kezelő Rendszer

## Cél:
Hozz létre egy egyszerű állatkert kezelő rendszert, amely lehetővé teszi különböző állatok nyilvántartását. Az állatkertben különböző típusú állatok vannak, és minden állatnak vannak alapvető adatai és képességei.

## Követelmények:

## 1. Allat Osztály:

Attribútumok:
• nev (string): Az állat neve.
• faj (string): Az állat faja.

Metódusok:
• __init__(self, nev, faj): Konstruktor metódus.
• hangot_ad(self): Egy metódus, ami visszaadja, hogy az állat milyen hangot ad ki. Az alapértelmezett hang "Ismeretlen hang".

## 2. Ragadozo és Novenyevo Osztályok (Öröklődnek az Allat osztályból):

Ragadozo specifikus metódusok:
• vadaszik(self): Visszaadja, hogy "A [állat neve] vadászik."

Novenyevo specifikus metódusok:
• eszik(self): Visszaadja, hogy "A [állat neve] növényeket eszik."

## 3. Allatkert Osztály:

Attribútumok:
• allatok (lista): Az állatkertben lévő állatok listája.

Metódusok:
• allat_hozzaadasa(self, allat): Hozzáad egy állatot az állatkert listájához. Ha az állat már létezik (név alapján), akkor dobj egy AllatMarLetezikKivetel kivételt.
• allatok_listazasa(self): Listázza az összes állatot az állatkertben.

## 4. Egyedi Kivételek:
• AllatMarLetezikKivetel: Akkor dobható, ha olyan állatot próbálunk hozzáadni, ami már létezik az állatkertben.

## Feladatok:
• Implementáld az Allat, Ragadozo, és Novenyevo osztályokat.
• Implementáld az Allatkert osztályt.
• Implementáld az egyedi kivételt.
• A programod fő részében hozz létre egy Allatkert osztály példányt, és próbálj meg különböző állatokat hozzáadni és listázni.

```python
allatkert = Allatkert()
oroszlan = Ragadozo("Simba", "oroszlán")
zebra = Novenyevo("Zara", "zebra")

allatkert.allat_hozzaadasa(oroszlan)
allatkert.allat_hozzaadasa(zebra)

print(oroszlan.vadaszik())  # Kimenet: "A Simba vadászik."
print(zebra.eszik())        # Kimenet: "A Zara növényeket eszik."

allatkert.allatok_listazasa()
