# Jadłospis 5 dni · 2000 / 1600 kcal

Aplikacja HTML z planem żywieniowym dla dwóch osób: te same posiłki, dwie wielkości porcji.
Niski indeks glikemiczny, wysoka podaż białka, śniadania na słodko, drugie śniadanie na słono, obiad z piersi kurczaka, lekka kolacja.

## Funkcje

- przełącznik porcji: obie / 2000 kcal / 1600 kcal
- filtr dni 1–5, rozwijane przepisy na każdy posiłek
- paski realizacji celu kalorii i białka
- lista zakupów z odhaczaniem (zapis w `localStorage`), wyszukiwarka produktów
- zakładki: pizza z airfryera, plan przygotowań, przeliczniki kcal/białko
- wersja do druku / PDF (`jadlospis-5-dni.pdf`)

## Technicznie

Jeden plik `index.html`, zero zależności, działa offline. Wszystkie dane (dni, przepisy, lista zakupów)
są w tablicach `DAYS`, `PIZZA`, `SHOP`, `PREP`, `CONV` na początku skryptu.

Wartości odżywcze są orientacyjne — nie zastępują konsultacji z dietetykiem.
