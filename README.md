# XTB – kalkulačka zisku a straty

Jednostránková aplikácia (len `index.html`, bez servera). Nahráš výkaz z XTB v Exceli,
vyberieš akciu a posuvníkom meníš jej cenu. Aplikácia prepočíta zisk/stratu v mene
tvojho účtu (EUR alebo USD), nakreslí graf a rozpíše jednotlivé nákupy.

Súbor sa nikam neodosiela, všetko beží v prehliadači.

## Nasadenie na GitHub Pages
1. Na GitHube vytvor nový repozitár (napr. `xtb-kalkulacka`).
2. Nahraj doň `index.html` a `README.md`.
3. Settings → Pages → Source: *Deploy from a branch* → vetva `main`, priečinok `/ (root)` → Save.
4. Po minúte bude stránka na `https://<tvoje-meno>.github.io/xtb-kalkulacka/`.

Dôležité: výkaz z XTB (xlsx) **nenahrávaj do repozitára**, obsahuje číslo účtu a tvoje obchody.
Nahrávaš ho iba cez stránku v prehliadači.

## Ako sa používa
1. Exportuj z XTB výkaz (xStation → História → Export → Excel).
2. Pretiahni súbor na stránku. Mena účtu sa zistí z výkazu a dá sa prepnúť EUR/USD.
3. Vyber ticker (predvolene NVDA.US), posuvníkom zmeň cenu, prípadne aj kurz.

## Čo sa používa z výkazu
Hárok `Open Positions`: počet akcií, nákupné ceny a dátumy, hodnota a čistý zisk v mene účtu.
Investovaná suma v mene účtu = hodnota − čistý zisk (obsahuje skutočný kurz v čase nákupu).
Zahrnuté sú len otvorené nákupy (BUY). Dividendy sa nezapočítavajú.

## Knižnice (načítavajú sa z cdnjs)
SheetJS 0.18.5 (čítanie xlsx), Chart.js 4.4.1 (graf).
