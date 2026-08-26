# Změny

## v0.1.127 — 2026-08-26

Verze je nově číslo kroků vývoje (`0.1.<počet commitů>`) a vidíš ji v rohu horní lišty.

### Opravy z hraní
- **Zvířata se prolínala** — hlava jednoho koně končila v těle druhého. Každý druh má teď
  osobní prostor podle délky těla. Kdo jde stejným směrem, tomu stačí jemné uhnutí, takže
  smečka na cestě kolem sebe proklouzne místo nárazu do neviditelné zdi.
- **Mládě se hýbalo, ale nešlapalo** — rychlost pro volbu animace se počítala špatně, takže
  hříbě „chodilo“ pod prahem chůze a stálo v klidové póze. Modely mláďat se navíc zmenšovaly dvakrát.
- **Kočka se hýbala bez kroku** — balík pro ni nemá cval, a při rychlosti nad prahem se sáhlo
  po prázdné animaci. Do rychlejšího chodu se navíc přechází dřív, aby krok odpovídal rychlosti.
- **Vlci po nezdařeném lovu trčeli v hloučku** půl minuty tam, kde jim kořist utekla.
  Teď se odklidí do krytu. Hloučkování kleslo z 33 % na 11 % času.
- **Sledovací kamera se klepala** — mířila na pozici zvířete v simulaci, která se mění jen
  desetkrát za sekundu.
- **Kláda přes potok** ležela jednou nad hladinou, jindy pod ní.
- **Žízeň** — stádo u rybníka končilo na maximu. Voda je teď cítit na dálku, stádo se učí
  jeden od druhého, napajedlo si pamatuje dlouho a zvíře se napije dosyta.

### Druhy a vzhled
- **Zubr je nově kráva** (samec býk) a **prase je domácí** — model i barvy tomu odpovídají víc.
- **Ze srnky je jelen lesní**: měl rozměry srnce, ale model jelena, takže vedle koně působil malý.
- **Varianty srsti**: kůň má hnědáka, plaváka, bělouše a vraníka, kráva čtyři, prase tři, vlk tři.
  V katalogu se dají vybrat.
- **Barvení po částech** — hříva, ocas, kopyta, rohy a břicho místo jedné barvy na celé zvíře.
- **Kůň se lišce postaví**, místo aby před ní utíkal. Před vlkem utíkají oba.
- Nové ikony druhů v hranatém rámu.

## v0.1.0 — 2026-08-26

První veřejný vývojový build.

### Zvířata a modely
- **Dvanáct druhů**: jelen, kůň divoký, kráva, prase, husa, zajíc, králík, holub, sojka
  a predátoři vlk, liška, kočka.
- Sedm druhů má **hotový low-poly model** s kostrou a animacemi (vlk, liška, jelen/laň, kůň,
  kráva/býk, prase, kočka), zbytek staví parametrická stavebnice.
- **Varianty srsti**: kůň má hnědáka, plaváka, bělouše a vraníka, kráva čtyři, prase tři,
  vlk tři. Vybírají se v katalogu, nebo si každý kus vezme svoji.
- Mládě není jen zmenšené zvíře — má proti tělu větší hlavu a parohy mu narostou až s dospělostí.

### Animace
- Chůze, klus a cval se přepínají podle skutečné rychlosti a **tempo odpovídá délce kroku**,
  takže nohy neklouzají po zemi a malá zvířata našlapují častěji než velká.
- Zvíře otáčí **nejdřív hlavu, pak krk a nakonec tělo** — otočit se celý stojí energii.
- Pastva, útok při ulovení, pád po zásahu, obrana stáda trknutím, střídání klidových póz.
- Ve svahu zvířata stojí po spádnici, ne svisle.

### Chování
- Utility AI: každé zvíře si boduje, co teď dává největší smysl, a v pravém panelu je vidět proč.
- Smysly: zrak se zorným kuželem, čich podle větru, sluch podle hlučnosti. **Vodu je cítit**
  na dálku, stádo se učí jeden od druhého a napajedlo si pamatuje dlouho.
- Rozmnožování: páry, hnízda s vejci, krmení a učení mláďat, sirotci, vdovství, příbuznost.
- Roční období (rok trvá 16 dnů), sníh, zamrzlý rybník, déšť a vítr.

### Prostředí
- Nástroje: kopec se srázem, rybník, mělčina, potok s brody, lávka přes vodu, les, vysoká tráva,
  kámen, bláto, holá zem, krmítko, hluk. Náhled ukazuje přesně, co vznikne.
- Minimapa, filtry, fotorežim, okno sledování jednoho zvířete, průřezy norou a hnízdem.

### Známá omezení
- macOS a Linux buildy nebyly na cílovém systému otestované (vývoj běží na Windows).
- Uložené hry nemusí přežít další verzi.
