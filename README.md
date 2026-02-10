# Ringmärkningsdata Sverige

Interaktiv karta över svensk fågelringmärkningsdata från **Naturhistoriska riksmuseet** (Ringmärkningscentralen), publicerad via [GBIF](https://www.gbif.org/dataset/4f70108a-dda7-4e8b-8298-babaee5182c3).

- **Webbplats:** [https://ulfboge.github.io/nrm-ringmarkningsdata/](https://ulfboge.github.io/nrm-ringmarkningsdata/)
- **Källa:** *Bird Ringing Centre in Sweden (NRM)* – DOI [10.15468/cghs8p](https://doi.org/10.15468/cghs8p)

---

## Vad visar kartan?

- Varje **punkt** är en observation från ringmärkningsregistret (ringmärkning eller återfynd) med:
  - **Art** (svenskt + vetenskapligt namn)
  - **Datum** för händelsen
  - **Plats** (lokal och län/landskap)
- Kartan visar i den här versionen ett **urval (~5 000 observationer)** ur ett mycket större dataset (miljontals poster), för att sidan ska vara snabb och responsiv.
- Översiktsrutan under kartan summerar:
  - Antal observationer med koordinater
  - Antal arter
  - Topp 15 arter i urvalet

> Syftet är att ge en snabb, visuell översikt av hur vanligt förekommande ringmärkta och återfunna småfåglar är i Sverige, samt vilka arter som dominerar i ett givet urval.

---

## Begränsningar och tolkning

- **Urval, inte fullständig bild:** Endast ett begränsat antal observationer hämtas via GBIF API, så kartan representerar ett smakprov – inte hela registret.
- **Positionsosäkerhet:** Koordinater kan vara generaliserade eller avrundade beroende på hur datat publicerats.
- **Tidsdimension:** Datumet i popupen hjälper dig se *när* en fågel ringmärkts/observerats, men kartan visar inte tidsanimering (alla år samtidigt).

För mer avancerade analyser (tidsserier, fullständiga dataset, filtrering på art/period) bör du hämta ned data direkt från GBIF och bearbeta den i t.ex. Python eller R.

---

## Tekniskt

- **Format:** GBIF Occurrence API (`/occurrence/search`, dataset key `4f70108a-dda7-4e8b-8298-babaee5182c3`).
- **Frontend:** Ren HTML/JS med [Leaflet](https://leafletjs.com/) och mörk bakgrundskarta från CARTO.
- **Hosting:** GitHub Pages (deploy via GitHub Actions).

Data © Naturhistoriska riksmuseet / publicerad via GBIF. Vid vidareanvändning, citera datasetet med DOI [10.15468/cghs8p](https://doi.org/10.15468/cghs8p).
