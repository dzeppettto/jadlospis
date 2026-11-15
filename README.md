# Jadłospis 5 dni · 2000 / 1600 kcal

Aplikacja HTML z planem żywieniowym dla dwóch osób: te same posiłki, dwie wielkości porcji.
Niski indeks glikemiczny, wysoka podaż białka, śniadania na słodko, drugie śniadanie na słono, obiad z piersi kurczaka, lekka kolacja.

## Funkcje

- przełącznik porcji: obie / 2000 kcal / 1600 kcal
- filtr dni 1–5, rozwijane przepisy na każdy posiłek
- paski realizacji celu kalorii i białka
- lista zakupów z cenami, licznikiem koszyka i odhaczaniem (zapis w `localStorage`)
- **wspólna lista na żywo**: przycisk „Udostępnij listę" tworzy link z kodem — druga osoba widzi odhaczenia i sumę koszyka w czasie rzeczywistym
- wyszukiwarka produktów, zakładki: pizza z airfryera, plan przygotowań, przeliczniki kcal/białko
- wersja do druku / PDF (`jadlospis-5-dni.pdf`)

## Synchronizacja listy

Kanał to publiczny temat w [ntfy.sh](https://ntfy.sh) (`jadlospis-<kod>`), bez konta i bez kluczy API.
Link z kodem (`?l=...`) wystarczy wysłać drugiej osobie. Ostatnie 12 godzin wiadomości jest
przechowywane, więc po ponownym otwarciu linku lista się odtworzy. Kto ma link, ten może edytować —
nie używaj tego do danych wrażliwych. Bez internetu lista działa lokalnie.

## Ceny

Ceny w liście są orientacyjne (Biedronka/Lidl/Kaufland, koniec 2026) i sumują się do **380,50 zł**
za 5 dni dla dwóch osób. Kurczak (2 kg) liczony jako 0 zł, bo jest już w domu.


## Technicznie

Jeden plik `index.html`, zero zależności, działa offline. Wszystkie dane (dni, przepisy, lista zakupów)
są w tablicach `DAYS`, `PIZZA`, `SHOP`, `PREP`, `CONV` na początku skryptu.

Wartości odżywcze są orientacyjne — nie zastępują konsultacji z dietetykiem.
