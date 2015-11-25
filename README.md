# Analiza podatkov s programom R, 2015/16

Repozitorij z gradivi pri predmetu APPR v študijskem letu 2015/16.

## Tematika

Za temo projekta sem si izbrala Pesem Evrovizije. Analizirala bom tekmovanje od začetka v letu 1956 do leta 2014. Pri tem bom uporabila dve tabeli: Prva tabela, ki sem jo napisala v excelu (CSV), obravnava spremeljivke: država (imenska spremenljivka), mesto prve udeležbe države na tekmovanju Pesmi Evrovizije (imenska spremenljivka), leto prve udeležbe države na tekmovanju (številska spremenljivka), število udeležb (številska spremenljivka), število zmag (številska spremenljivka) ter urejenostno spremeljivko - razsežnost držav glede na število udeležb. Če se je država udeležila tekmovanja manj kot dvajsetkrat, je razsežnost majhna, srednja, če se je udeležila manj kot štiridesetkrat in visoka sicer. Druga tabela v HTML obliki pa vsebuje podatke: leto (številska), gostiteljica Evrovizije (imenska), mesto (imenska), država zmagovalka (imenska), zmagovalni izvajalec (imenska) in zmagovalna pesem (imenska). 

Tabelo sem dobila na strani:http://sl.wikipedia.org/wiki/Pesem_Evrovizije .

Cilj: Cilj projektne naloge je, da analiziram katere države so se največkrat udeležile tekmovanja, katere zmagale, katere države (mesta) so bile največkrat gostiteljice dogodka ter katerega leta je največ držav prvič nastopilo.
Podatke sem dobila iz spletnih naslovov:

•	Wikipedija: http://sl.wikipedia.org/wiki/Pesem_Evrovizije

•	http://www.eurovision.tv/page/history/year


Podatke,ki jih potrebujem, bom v R uvozila iz CSV in HTML oblike.


## Program

Glavni program in poročilo se nahajata v datoteki `projekt.Rmd`. Ko ga prevedemo,
se izvedejo programi, ki ustrezajo drugi, tretji in četrti fazi projekta:

* obdelava, uvoz in čiščenje podatkov: `uvoz/uvoz.r`
* analiza in vizualizacija podatkov: `vizualizacija/vizualizacija.r`
* napredna analiza podatkov: `analiza/analiza.r`

Vnaprej pripravljene funkcije se nahajajo v datotekah v mapi `lib/`. Podatkovni
viri so v mapi `podatki/`. Zemljevidi v obliki SHP, ki jih program pobere, se
shranijo v mapo `../zemljevidi/` (torej izven mape projekta).

## Spletni vmesnik

Spletni vmesnik se nahaja v datotekah v mapi `shiny/`. Poženemo ga tako, da v
RStudiu odpremo datoteko `server.R` ali `ui.R` ter kliknemo na gumb *Run App*.
Alternativno ga lahko poženemo tudi tako, da poženemo program `shiny.r`.

## Potrebni paketi za R

Za zagon tega vzorca je potrebno namestiti sledeče pakete za R:

* `knitr` - za izdelovanje poročila
* `rmarkdown` - za prevajanje poročila v obliki RMarkdown
* `shiny` - za prikaz spletnega vmesnika
* `DT` - za prikaz interaktivne tabele
* `maptools` - za uvoz zemljevidov
* `sp` - za delo z zemljevidi
* `digest` - za zgoščevalne funkcije (uporabljajo se za shranjevanje zemljevidov)
* `httr` - za pobiranje spletnih strani
* `XML` - za branje spletnih strani
* `extrafont` - za pravilen prikaz šumnikov (neobvezno)
