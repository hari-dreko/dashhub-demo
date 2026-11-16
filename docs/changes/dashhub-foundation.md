# Dashhub Business: første fundament

Status 16/11/2026: klar til designreview. Branch: haris/dashhub-foundation.
Kilde: https://github.com/hari-dreko/dashhub-demo/tree/haris/dashhub-foundation
Relateret senere arbejde: AI-332. Dette er Haris' egen dashboardskabelon.

Problem: Haris mangler en konkret skabelon, som kan vise kunder et enkelt dashboard, mens SOYA- og demo-repo-adgang afventes.

Løsning: En selvstændig HTML-demo med SOYA-inspireret venstremenu, velkomstfelt, kort og genveje. Light er standard efter Haris' ønske; dark bruger OS-guidens mørke grundfarver. Fiktive nøgletal, periodevalg, nye demotal, projektsøgning og detaljer, CSV-download, illustrerede automatiseringer og temaindstillinger. Binær detalje viser sætningen Haris er den bedste samt 526 gentagelser i 10.000 bytes (19 bytes pr. sætning, ingen separator).

Metode: Buildless HTML/CSS/JS valgt til en hurtig lokal designprototype uden pakkeinstallation. Dette er ikke den færdige Next.js/React/Tailwind OS-app og genbruger endnu ikke appChrome-komponenterne. Systemfont bruges som lokal fallback. Teknisk migrering aftales separat. Ingen backend eller ægte AI-funktioner.

Filer: index.html, README.md og dette dokument. Ingen kundedata, adgangskoder eller eksterne netværkskald i demoen. Repoet er offentligt efter Haris' godkendelse. Ingen deploymentopsætning medfølger.

Kontrol: Browserkontrol gennemført af mobil- og desktoplayout, projektnavigation, filtrering til Nye produktbilleder, detaljedialog, light/dark-skift, ugevalg med opdaterede tal og binær beregning (19 bytes, 526 gentagelser). CSV-downloadtesten blev afbrudt af browserforbindelsen og er ikke bekræftet. Tilfældige tal er begrænset i koden; tilfredshed højst 100. Ingen merge eller deployment. Ingen workflows eller hostingfiler findes i repoet. GitHub Pages var deaktiveret ved repoaflæsning; eksterne hostingkoblinger er ikke fuldt verificeret. Afleveres lokalt og på branch.

## Opdatering 16/11/2026: personligt overblik og Ret gitter

Problem: Overblikket havde for meget tekst og et for afdæmpet lyst tema. Haris ønskede at prioritere kortene selv.

Løsning i index.html: Lyst tema med lavendel, mint, fersken og rosa. Mindre skrift og forklaringer i detaljevisninger. Ret gitter til venstre for navnet aktiverer let rystende kort, træk og slip, håndtag og flyttepile. Færdig gemmer rækkefølgen i den aktuelle browser. Tastaturets pile kan også flytte et fokuseret kort. Reduceret bevægelse respekteres. Ingen ekstra pakker.

Kontrol: Flytning med pil, gemt rækkefølge efter genindlæsning og detaljedialog verificeret i browseren. Lyst og mørkt tema kontrolleret. Berøringsbetjening på fysisk telefon er ikke testet. Træk via håndtaget og opdatering af demotal er også verificeret. Mobilvisning kontrolleret efter genindlæsning; ingen JavaScript-fejl i browserloggen. git diff --check bestået. Status: klar til review på opgavens branch, ikke deployet.

## Opdatering 16/11/2026: resultatfarver

Problem: De store tal viste ikke tydeligt, om resultatet var godt eller lavt.
Løsning i index.html: Nøgletal og kort bruger rød, orange, gul og grøn i både lyst og mørkt tema. Kortene får også en tekststatus. Farven beregnes ud fra andel af demomålet: under 40 %, under 65 %, under 90 % og fra 90 %. Månedens mål er 10.000 aktiviteter, 2.500 sparede minutter og 80 opgaver. Ugens mål er 2.500, 600 og 20. Tilfredshed måles mod 100 %. Højere er bedre i denne demo; grænserne er illustrative, ikke kundens aftalte KPI'er. Detaljen forklarer mål og grænser.
Kontrol: Browseren viser korrekte statusser for starttal, periodevalg opdaterer mål og farver, og mørkt tema viser gul, grøn og rød med læsbare tal. Detaljeforklaringen er verificeret. git diff --check bestået.
Status: klar til review på haris/dashhub-foundation. Ingen merge eller deployment.

## Opdatering 16/11/2026: hvid baggrund og tydeligere knapper

Problem: Baggrunden og kanterne var for afdæmpede, og knapperne for små.
Løsning i index.html: Hvid baggrund i lyst tema, tydeligere kantfarver i begge temaer og 1 px kanter på kort. Handlingsknapper, periodevalg og navigation får 0,5 em ekstra indvendig afstand. Gitterknapper er 40 × 40 px med ekstra plads over kortindholdet. Resultatfarver bevares.
Kontrol: Mobilvisning kontrolleret i browseren i normal og Ret gitter-tilstand; større knapper og korttekst overlapper ikke. git diff --check bestået.
Status: klar til review på haris/dashhub-foundation. Ikke merged eller deployet.

## Opdatering 16/11/2026: detaljer og næste skridt

Problem: Lange detaljer skal kunne læses uden at miste luk-knappen eller næste skridt.
Løsning i index.html: Detaljedialog med intern scroll og fast overskrift og bund. En deaktiveret knap viser næste skridt, fx Arbejd videre med projektet. Teksten Kun demo forklarer, at ingen destination er tilsluttet. Dashboardet bagved låses under visningen. Indholdet kan også scrolles med tastaturet og starter øverst ved genåbning.
Kontrol: Browserkontrol på mobil og ved 500 px skærmhøjde. Indholdshøjde 421 px i et område på 237 px; scroll til bunden verificeret. Luk-knap og demoknap forbliver synlige. git diff --check bestået.
Status: klar til review på haris/dashhub-foundation. Ingen merge eller deployment.

## Opdatering 16/11/2026: nulstil gitter

Problem: Efter flytning af kort manglede en vej tilbage til standardrækkefølgen.
Løsning i index.html: Nulstil gitter vises ved siden af Færdig under redigering. Knappen gendanner den oprindelige rækkefølge; Færdig gemmer den. Tema og demotal ændres ikke. Headeren ombrydes på mobil.
Kontrol: Flyttet kort, nulstillet, gemt og genindlæst i browseren. Alle 11 kort står i standardrækkefølge, og nulstil-knappen er skjult uden for redigering. Mobilvisning og git diff --check kontrolleret.
Status: klar til review på haris/dashhub-foundation. Ikke merged eller deployet.
