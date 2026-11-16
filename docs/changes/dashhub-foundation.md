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
