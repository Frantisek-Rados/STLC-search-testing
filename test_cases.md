# Test Cases – DuckDuckGo Search

## Testovacie prostredie
- Web: https://duckduckgo.com
- Prehliadač: Chrome
- Dátum: 2026-05-30

## Požiadavka
Vyhľadávanie musí akceptovať dopyty v dĺžke 1–50 znakov. Prázdny dopyt (0 znakov) nezobrazí žiadne výsledky alebo zobrazí chybu. Dopyt nad 50 znakov zobrazí varovanie.

| TC ID | Test Case | Vstup (search query) | Expected Result | Actual Result | Status (PASS/FAIL) |
|-------|-----------|---------------------|-----------------|---------------|-------------------|
| TC_01 | Prázdne vyhľadávanie (hranica 0) | (prázdne pole) | Žiadne výsledky alebo chybová správa | | |
| TC_02 | Jeden znak (dolná hranica – funguje) | "a" | Zobrazia sa výsledky vyhľadávania | | |
| TC_03 | Bežný dopyt (v strede rozsahu) | "qa testing" | Zobrazia sa relevantné výsledky | | |
| TC_04 | Presne 50 znakov (horná hranica) | (vytvor reťazec s 50 znakmi – napr. "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa") | Zobrazia sa výsledky | | |
| TC_05 | 51 znakov (nad hornou hranicou) | (vytvor reťazec s 51 znakmi) | Systém zobrazí varovanie alebo orezá dopyt | | |
| TC_06 | Špeciálne znaky | "@#$%^&*()" | Žiadna chyba, systém vyhľadá (alebo zobrazí 0 výsledkov) | | |
| TC_07 | Veľmi dlhý dopyt (100+ znakov) | (100 znakov) | Systém nezamrzne, zobrazí varovanie alebo orezanie | | |
