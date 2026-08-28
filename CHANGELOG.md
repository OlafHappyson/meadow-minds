# Změny

## v0.1.155 — 2026-08-28

Dvacet kroků od minule. Většina práce šla do toho, aby zvířata vypadala živě, i když se zrovna nic neděje — a do tempa, které tomu dá čas.

### Tempo louky
- **Zvíře u činnosti vydrží.** Předtím měnilo, co dělá, každých devět sekund a „hlídka“ trvala
  v průměru **jedinou vteřinu** — kůň se za šest dní rozhlédl přes tisíckrát. Ostražitost se
  totiž naplnila za sedmnáct sekund a vyprázdnila za tři a půl, takže neustále přebila cokoli
  rozdělaného. Teď má každá činnost svoji nejkratší dobu: průměrný úsek stoupl z 9,7 na
  **45 sekund**, pastva trvá minutu, odpočinek minutu a čtvrt. Strach to nepřebíjí — před vlkem
  zvíře uteče kdykoli.
- **Kořist má konečně čas se najíst.** Ve stejném běhu s vlkem stoupla pastva z 33 na 42 %
  a pití kleslo z 19 na 8 %. Husy předtím střídaly „hlídám“ a „jdu se napít“ po vteřině
  a od vody odcházely s poloviční žízní. Na konci běhu přežilo **deset hus místo šesti**.
- Délka dne a roku se dá nastavit; nejkratší doby činností se řídí jí, takže s delším dnem
  se prodlouží i klid.

### Animace
- **Vlastní animace psané kódem.** Balík má na většinu druhů jen dva tři klipy, tak si zbytek
  doděláváme: dýchání a přenášení váhy, zatřepání hlavou, švihnutí ocasem po mouchách,
  hrabání kopytem, cukání ušima, protažení, prase ryjící rypákem a rytmus žvýkání při pastvě.
- **Zvíře, které stojí, něco dělá.** Klidové pózy se střídají nepravidelně, zvíře se rozhlíží,
  při pastvě okusuje a každých pár vteřin zvedne hlavu. Nejdelší doba úplného bez hnutí klesla
  u prasete z 11 na necelé 4 sekundy.
- **Hlava se dívá po tom, co zvíře zaujalo** — po vlkovi, po vodě, po cíli cesty. Míří na něj
  s odchylkou pod stupeň, zatímco tělo je ještě odkloněné o čtyřicet. Do zatáčky se navíc
  zvíře prohne v páteři.
- **Pomalá chůze koně.** Kůň, kráva a prase mají v balíku i pomalou chůzi, kterou jsme
  nepoužívali — popocházení se hrálo běžnou chůzí natahovanou na strop, takže kůň dělal
  dvoumetrový krok a ujel při něm pětatřicet centimetrů. Krok navíc navazuje tam, kde skončil,
  a přechod do klusu má vůli, aby na prahu neblikal.
- **Kočka** dostala protažení, olizování, švihání ocasem a hlavně natáčení hlavy — do teď
  jí nefungovalo vůbec, protože její model má kosti bez jmen.
- **Námluvy a páření.** Páření bylo dosud jediný okamžik simulace, takže se v deníku objevilo
  mládě jakoby odnikud. Pár teď chvíli zůstane spolu. Hřebec se před klisnou nese s obloukem
  v krku, jelen se blíží s nízkým nataženým krkem, kočka se otírá.
- **Husa mává křídly**, když utíká po zemi, při obraně je roztáhne do stran a při námluvách
  pumpuje hlavou. Zajíc a králík si čistí čumák, panáčkují a cukají ušima; holub a sojka klovou.

### Vzhled
- **Zvířata se bořila do země** po kotníky — model se posazoval podle nejnižší kosti, jenže pod
  ní visí ještě kopyto. Teď stojí na zemi.
- **Barva srsti se konečně používá.** Kůň má v modelu jen dvě plochy a přepočet z nich dělal
  „břicho“, takže všechny čtyři varianty splývaly do jedné bledé. Hnědák, plavák, bělouš
  a vraník jsou teď jasně odlišitelní. Srst navíc má stínování — hřbet tmavší, břicho světlejší.
- **Mrtvé zvíře leží na boku** v kaluži místo hnědé skvrny s kostičkou. Ukládá se i do uložené hry.
- **Prostředí z hotových modelů**: stromy, keře, kameny a trsy trávy. Les už se nepropadá do louky.

### Hra
- **Úvodní obrazovka.** Nová louka, Pokračovat, Nastavení, Konec. Před spuštěním si vybereš
  krajinu, velikost, startovní sadu zvířat a seed — a hned vidíš **živý náhled mapy**, která
  se spustí.
- **Nastavení**: celá obrazovka, svislá synchronizace, strop snímků, hlasitost, štítky, smysly,
  vítr a délka dne i roku. Volby se pamatují.
- **Životopisy.** U vybraného zvířete je záložka Život: kdy se narodilo, kdy dospělo, kolik
  přečkalo zim, koho potkalo, o co přišlo.
- **Louka žije podle toho, kdo po ní chodí.** Stádo vypase dobrou trávu a musí se posunout dál;
  kde dlouho nikdo nebyl, vyroste vysoká.

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
