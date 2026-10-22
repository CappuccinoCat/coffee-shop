# Projektbeskrivelse

- Hjemmesiden hedder **MokkaBar**.
- Byg og vedligehold en responsiv hjemmeside, der fungerer som et visuelt online visitkort for en lokal kaffebar.
- Præsentér kaffebarens kaffe, stemning og omgivelser indbydende og professionelt.
- Hjemmesiden er i dag en enkelt side (`index.html`) opdelt i sektioner med intern ankernavigation: Hjem, Om os, Menu, Galleri og Kontakt. Bevar denne ene side.
- Behovet for undersider er [SKAL AFKLARES]. Opret ingen ekstra sider, før brugeren har besluttet det.
- Målgruppe, endelig visuel identitet og konkrete krav til responsiv adfærd er [SKAL AFKLARES]. Den nuværende visuelle retning (varme kaffefarver – espresso, skum, ler, crema og glasur – og en rolig og hyggelig tone) er etableret i `css/styles.css` og skal følges. Ændr den kun, når brugeren udtrykkeligt beder om det.

# Teknologier

- Hjemmesiden bygges med HTML og CSS. Simpel vanilla JavaScript må bruges, når det giver mening; hold det enkelt.
- Mobilnavigationen er bygget med en CSS-only checkbox (`navigation-toggle`); bevar dette mønster.
- Udviklingsserver, buildproces og deployment er [SKAL AFKLARES].
- `.idea/` er lokal IDE-metadata (den indeholder bl.a. PHP-indstillinger) og dokumenterer ikke et teknologivalg for hjemmesiden.
- Introducér ikke frameworks eller tredjepartsbiblioteker, medmindre brugeren senere udtrykkeligt ændrer denne begrænsning.
- Implementér ikke backend-programmering, medmindre brugeren senere udtrykkeligt ændrer denne begrænsning.

# Projektstruktur

- Anvend den eksisterende projektstruktur:

  ```text
  coffee-shop/
  ├── index.html
  ├── css/
  │   └── styles.css
  ├── fonts/
  └── images/
  ```

- `fonts/` indeholder den lokalt hostede Instrument Serif (kursiv, `.woff2`) og dens licens (`OFL.txt`). Fonten indlæses via `@font-face` i `css/styles.css` og preloades i `index.html`; hent ikke fonte fra Google Fonts eller andre eksterne domæner.

- `index.html` er hele hjemmesiden for MokkaBar (sprog: dansk, `lang="da"`).
- `css/styles.css` indeholder al styling. Farver og andre fælles værdier ligger som CSS-variabler i `:root`; genbrug dem frem for at indføre nye hardcodede værdier.
- Responsiv adfærd styres med breakpoints i `css/styles.css` (mobil til og med 767 px, `min-width: 768px` og `min-width: 1024px`) samt `prefers-reduced-motion`. Følg dem.
- `images/` indeholder de billeder, brugeren selv har indsat (filnavne følger mønstret `mokkabar-*.jpg|png`). Hjemmesiden skal bruge billeder fra denne mappe, og nye billeder navngives efter samme mønster.
- Sektioner i `index.html` bruger `id`-ankre (`hjem`, `om-os`, `menu`, `galleri`, `kontakt`), som både header- og footernavigation peger på. Bevar ankrene, eller opdatér alle links, hvis et anker ændres.
- `.idea/` indeholder editorens lokale projektindstillinger; redigér ikke disse filer som del af hjemmesidearbejdet.
- Opret ikke ekstra sider, heller ikke midlertidige demo-, test- eller fejlsider, medmindre brugeren udtrykkeligt beder om det.

# Arbejdsform

## Før ændringer

- Undersøg relevante eksisterende filer og kode, før noget ændres.
- Forstå den eksisterende implementering, før ny kode foreslås eller skrives.
- Identificér eksisterende mønstre, navngivning (fx BEM-lignende klasser som `menu-item__heading` og `button--light`) og mappestruktur, og følg dem.
- Gæt ikke på væsentlige beslutninger. Bed om afklaring, eller markér den manglende information tydeligt, hvis den kan ændre løsningen væsentligt.

## Under arbejdet

- Følg projektets eksisterende struktur og konventioner.
- Genbrug eksisterende kode, komponenter, styles og mønstre, når de dækker behovet.
- Lav kun de ændringer, der er nødvendige for den aktuelle opgave.
- Undgå refaktorering og ændringer uden for opgavens scope.
- Bevar eksisterende funktionalitet, medmindre opgaven specifikt kræver andet.
- Bevar tilgængeligheden: semantisk HTML, meningsfulde `alt`-tekster, `aria`-attributter, "Spring til indhold"-linket og synlig fokus.
- Kontrollér relaterede sektioner, navigation (header og footer) og alle berørte områder for konsekvenser, før arbejdet afsluttes.

# Andre vigtige ting ift. projekt

- Prioritér tydelig visuel præsentation af kaffen og stemningen i kaffebaren; tilføj ikke andre forretningsområder (fx webshop, bestilling eller booking) uden krav.
- Bevar en sammenhængende oplevelse på tværs af alle sektioner.
- Kontrollér layout og navigation på små og store skærme ved alle visuelle ændringer.
- Brug kun tekster, priser, produktnavne, kontaktoplysninger, åbningstider, adresser, billeder og branding, som brugeren har leveret eller godkendt; ellers markér dem som [SKAL AFKLARES].
- Priser, adresse (Kaffestræde 7, 2200 København N), åbningstider, telefonnummer, e-mail (`hej@mokkabar.example`) og links til sociale medier i `index.html` er [SKAL AFKLARES] og må ikke ændres eller udvides uden brugerens godkendelse. Mailadressen og de sociale links ser ud til at være pladsholdere.

# Begrænsninger

- Hjemmesiden skal indtil videre bestå af den ene side `index.html`.
- Brug HTML og CSS samt evt. simpel vanilla JavaScript.
- Introducér ikke frameworks.
- Installér eller anvend ikke nye tredjepartsbiblioteker.
- Implementér ikke backend, database, serverlogik eller API-endpoints.
- Tilføj ikke funktionalitet, indhold eller projektkrav, som ikke kan udledes af opgaven eller eksisterende filer.
- Ændr ikke IDE-metadata, genererede filer eller uvedkommende filer.

# Test og kvalitet

- Brug kun test-, build- og valideringskommandoer, der allerede findes og kan dokumenteres i projektet.
- Opfind ikke scripts, kommandoer eller værktøjer; der er aktuelt ingen dokumenteret test- eller buildkommando.
- Test især den funktionalitet og de sektioner, som en ændring berører.
- Kontrollér ved UI-ændringer mindst navigation (inkl. mobilmenuen og ankerlinks), indholdsoverløb, læsbarhed og layout ved små og store viewportbredder.
- Kontrollér, at der fortsat kun findes de aftalte brugerrettede sider.
- Hvis relevante tests eller kontroller ikke kan køres, forklar kort hvorfor.
- Rapportér relevante fejl, risici, manglende validering og mulige sideeffekter. Skeln tydeligt mellem problemer skabt af ændringen og allerede eksisterende problemer.

# Svar fra CODEX

- Hold afsluttende svar korte og fokuserede på resultatet.
- Brug dette format, og udelad kun punkter, der ikke er relevante:
  - **Ændret:** Kort beskrivelse af resultatet.
  - **Filer/områder:** Centrale berørte filer eller sektioner.
  - **Kontrol:** Udførte tests, builds eller manuelle kontroller; angiv hvorfor noget ikke kunne køres.
  - **Bemærkninger:** Relevante fejl, risici, begrænsninger og manglende information, som ikke kunne afgøres sikkert.
