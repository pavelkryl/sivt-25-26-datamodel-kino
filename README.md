# úloha: datový model kina

Tvým úkolem je navrhnout datovou strukturu pro systém, který spravuje program kina. k řešení použij **datové třídy** (`dataclasses`) v pythonu.

## zadání entit
namodeluj následující objekty a jejich vlastnosti:

### 1. adresa
- ulice, město, psč.

### 2. sál
- název (např. "velký sál"), kapacita (počet sedadel).

### 3. film
- název, délka v minutách, žánr, popis
- **volitelnost:** popis nemusí být vyplněn (`None`).

### 4. představení (vazební prvek)
- musí vědět, jaký **film** se hraje a v jakém **sále**.
- čas začátku (stačí jako `str`, např. "18:00").
- cena vstupenky.
- **povinnost:** představení nemůže existovat bez filmu a sálu.

### 5. kino
- název kina, **adresa** (objekt).
- seznam všech **filmů**, které mohou být eventuálně promítány
- seznam všech **představení** (kolekce), která kino aktuálně nabízí.

## požadavky na model
- **vnořování (1:1):** každé kino musí mít právě jednu adresu.
- **vazba (1:m):** kino v sobě drží seznam představení.
- **typy:** důsledně používej typové anotace, včetně `list[Trida]` a `Trida | None`.

## technické instrukce
1. kód piš do souboru `kino.py`.
2. pro seznamy v dataclasses použij defaultní hodnotu `field(default_factory=list)`.
3. na konci souboru vytvoř ukázkovou instanci kina, která bude obsahovat:
    - adresu kina,
    - alespoň dva různé filmy,
    - alespoň jeden sál,
    - alespoň čtyři naplánovaná představení (každé v jiný čas nebo na jiný film).

## odevzdání
Jakmile budeš mít model hotový, odevzdej jí jako gitové repo (nezapomeň push).
