# TM Inzetportaal

Zelfstandig Nederlandstalig prototype voor Tourism Management van Hogeschool Inholland, collegejaar 2026–2027. Gebruik uitsluitend fictieve gegevens.

## Openen

Download `TM-Inzetportaal.html` en open het in je browser. Installatie en internet zijn niet nodig; HTML, CSS, JavaScript, het ronde logo en de Excel-generator zitten in dit ene bestand.

Kies een fictieve docent om aanvragen in te dienen en te volgen. Wissel voor de demonstratie naar Teamleider om aanvragen te beoordelen en goedgekeurde wijzigingen naar Excel (.xlsx) te exporteren. Het logo brengt je altijd terug naar het docentoverzicht.

## Gegevens behouden

Aanvragen, reacties en besluiten worden opgeslagen onder de bestaande localStorage-sleutel `tm-inzetportaal.offline-demo.v1` (schema 1). Deze sleutel en het gegevensmodel zijn behouden. Voor bestaande gegevens: vervang het oude HTML-bestand op dezelfde plek en gebruik dezelfde browser en hetzelfde browserprofiel. Bewaar vooraf een kopie van het oude bestand. Browsergedrag bij lokale bestanden kan verschillen; verplaatsen, browsergegevens wissen en privémodus kunnen invloed hebben op de opslag.

Onleesbare bestaande opslag wordt niet automatisch overschreven. Nieuwe wijzigingen blijven in dat geval tijdelijk in het tabblad. Alleen bewust kiezen voor 'Demo opnieuw beginnen' vervangt de opslag door fictieve voorbeelden. Een Excel-export is geen volledige reservekopie: deze bevat alleen geselecteerde goedgekeurde aanvragen en hun historie.

## Statistieken

De locatie van de aanvraag bepaalt de indeling bij Amsterdam, Haarlem of Rotterdam. Elke ingediende aanvraag telt eenmaal, inclusief afgewezen en ingetrokken aanvragen. Aanvullingen en statuswijzigingen verhogen de telling niet. Aangevraagde DBU’s blijven meetellen; bij goedgekeurde DBU’s telt het daadwerkelijk toegekende aantal. Het dashboard toont ook alle locaties samen.

## Controles

De versie is met Chromium via een lokale testserver gecontroleerd op indienen, zichtbaarheid per docent, informatie vragen en aanvullen, gedeeltelijk goedkeuren, afwijzen, intrekken, bewaren na herladen, locatietotalen, logo-navigatie en dashboardkleuren. Op schermbreedtes 320, 375 en 768 pixels is geen horizontale pagina-overloop gemeten; brede tabellen kunnen binnen hun eigen kader scrollen. De Excel-download is gecontroleerd op geldige ZIP/CRC en XML, goedgekeurde aanvragen en het urentotaal. Ook bescherming tegen overschrijven van onleesbare opslag is getest.

De beheerde testbrowser blokkeert `file://`-adressen. Rechtstreeks openen als lokaal bestand kon daardoor hier niet apart worden getest. Er zijn geen externe bronnen of netwerkverzoeken nodig voor de app.

## Grenzen en latere uitbreiding

Er is geen centrale database: gegevens worden niet gedeeld tussen apparaten of collega’s. De rolwisselaar en filtering in de browser bieden geen veilige authenticatie of toegangsbeveiliging. Gebruik het prototype niet met echte personeelsgegevens.

De aanvraaglogica, opslagadapter en schermen zijn binnen het bestand gescheiden. Voor werkelijk gedeeld gebruik zijn centrale opslag, veilige aanmelding en server-side controle van rollen en eigenaarschap nodig. Daarvoor staan aanwijzingen in de broncode. Er zijn geen externe diensten of frameworks toegevoegd.
