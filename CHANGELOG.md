# Změny

## v0.1.192 — 2026-09-12

Na louce přibyly ovce a kozy, velká zvířata se přestala nechat bez odporu lovit a rozhraní
dostalo kreslenou grafiku. A hlavně: louka se přestala zasekávat.

### Nové druhy
- **Ovce.** Stádo drží pohromadě jako jeden kus: nikdo nechodí sám k vodě, na nocleh ani na
  toulky a před vlkem prchají všichni **stejným směrem** místo na všechny strany (poloměr
  rozprchnutého stáda klesl ze 14 na 4 metry). Zatoulaná ovce se ozve **bečením** a podle
  odpovědi si stádo najde i přes celou louku — dřív se stádo rozpadlo na čtyři až šest
  hloučků, teď zůstává jeden. Jehně, které nevidí matku, jde za jejím hlasem.
- **Koza.** Drží se volněji než ovce a umí dvě věci, které ostatní neumí: **okusuje keře**,
  takže se nají i tam, kde tráva nestačí, a před vlkem **vyleze na sráz** a zůstane stát
  nahoře — vlk za ní nevyleze. V dešti jde do úkrytu dřív a rozhodněji, kůzlata první dny
  leží schovaná.
- **Nová startovní sada Salaš**: osm ovcí, čtyři kozy a vlk. Šelma ze startovní sady se
  nově objeví na okraji louky, ne uprostřed stáda.
- Každý nový druh má **vlastní model pro samici, samce i mládě** — bahnice a beran se
  zatočenými rohy, koza s kratšími rohy a kozel s bradkou. Rohy jehněti a kůzleti
  dorůstají s věkem.

### Stádo a lov
- **Stádo má vůdkyni.** Přesun vede nejstarší klisna nebo laň, hřebec a býk jistí zezadu.
  Každý druh má navíc osobní rozestup podle toho, jestli se pase nebo odpočívá — tlačenice
  při pastvě klesla z 45–56 % času na 5–14 %. Matka s mládětem a zesláblý kus se při pastvě
  posouvají blíž ke středu, kde je bezpečněji.
- **Velká zvířata se brání.** Krávy se při spatření vlka stáhnou k sobě, postaví se čelem
  a vyrazí, když jde vlk blízko; telata utíkají za matku. Proti vlkovi jde **hřebec**
  (nebo odvážná klisna bez hříběte), klisny s hříbaty ustupují na odvrácenou stranu stáda.
  Laň brání kolouška proti lišce a kočce. Vlk stádo napřed **otestuje** — vyrazí do něj, a když
  se nikdo neoddělí nebo ho obránci zaženou, ustoupí a ten druh na půl dne nechá být.
  Za rok na louce klesla úspěšnost vlka u krav z 88 na 62 %, u koní z jednoho úlovku na
  žádný a celkově ze 48 na 35 %. Krav na konci roku zbylo 30 místo 25.
- **Vlk se konečně nasytí.** Dřív od úlovku odešel v půlce, mršina zmizela a on šel lovit
  znovu — za osm dní udělal dvaatřicet úlovků a z deseti krav nezbylo skoro nic. Teď úlovek
  dojídá do sytosti a **vrací se k němu**, i když je sto metrů daleko: úlovků je devět,
  krav padne 1,7 místo 7,3. Kořist si taky vybírá podle chuti, ne jen podle vzdálenosti.
- **Mršina se rozkládá.** Prochází stádii čerstvá → rozežraná → kosti a teprve pak zmizí.
  Maso ubývá žraním i hnitím podle počasí — v létě zhruba za dva dny, v hluboké zimě až
  za dvacet. Liška a kočka chodí ožírat, když vlk není nablízku. Býložravci se čerstvé
  mršině vyhýbají na dvanáct metrů, kosti je už neděsí.

### Rozhraní
- **Škáluje se s oknem.** V malém okně se rozhraní zmenší celé a nic se nepřekrývá, na velké
  obrazovce zůstane čitelné. V nastavení je navíc posuvník **Velikost UI**.
- **Volba rozlišení okna** (1280×720 až 2560×1440). Okno se vycentruje a nikdy nepřeroste
  plochu obrazovky.
- **Kreslená grafika**: tlačítka, záložky a ikony horní lišty v bronzovém stylu ikon druhů.
- Spodní lišta už nezačíná pod levým panelem (z nadpisu „Časová osa“ zbývalo „osa“)
  a prázdný černý obdélník náhledu druhu je schovaný, dokud si druh nevybereš.

### Vzhled
- **Skály a balvany**: srázy mají šest nepravidelných vrstev a společný zvětralý kámen,
  balvanům zmizely díry v povrchu.
- **Zvíře stojí ve svahu správně** — naklání se podle terénu pod všemi čtyřma, kůň si navíc
  dorovnává kopyta. Zvíře ve vzduchu se už k zemi nenaklání.
- **Potoky nejsou řetěz kaluží**, šířka se plynule mění a brod je dost široký na to, aby ho
  sousední hluboká místa nepřekryla. Rybníky mají mírně nepravidelný břeh.
- **Jehličnany z vlastních modelů** místo tří kuželů. Přes podzim zůstávají zelené.
- **Všech dvanáct druhů má vlastní podobu mláděte** — větší hlava proti tělu, kratší uši,
  menší křídla, kolouch má skvrny, tele nemá vemeno a rohy dorůstají až s dospělostí.

### Výkon
- **Louka se nezasekává ani s deseti zvířaty.** Ukázalo se, že za to nemohlo přemýšlení
  zvířat, ale přebarvování trávy — každou půlvteřinu se přepočítávalo dvanáct tisíc bodů
  louky (28,6 ms, v nejhorším 44,9 ms). Teď to dělá grafická karta za 0,37 ms a louka
  vypadá stejně.
- **Simulace je o třetinu až polovinu rychlejší**: krok se 125 zvířaty spadl z 31 na 18 ms.
  Ve hře to dělá 144 snímků za sekundu s deseti zvířaty a 72 se šedesáti. Chování zvířat
  se přitom nezměnilo ani o kousek.

### Opravy z hraní
- **Vymyšlená voda.** Stádo si navzájem „potvrzovalo“ vodu uprostřed louky — stačilo, aby
  soused vyrazil směrem k rybníku. Zvíře se teď učí jen od toho, kdo opravdu stojí u hladiny,
  a když na zapamatovaném místě žádná voda není, vzpomínku zahodí. Ovce stávaly se žízní
  na maximu devadesát metrů od nejbližší vody.
- **Matka odlétala od hladového mláděte.** Čerstvě vylíhlé mládě bylo tak malé, že se svým
  hladem nedosáhlo na práh krmení. Teď rozhoduje hlad, ne velikost.
- **Uložená hra se rozcházela hned prvním krokem** — neukládala se síla poplachu a seznam
  predátorů, takže po načtení rostl strach pomaleji. Dál se ztrácelo popolétnutí husy,
  hrabání, cesta na lávku, směr pohledu při hlídce, počet přečkaných zim a zeslábnutí hladem
  (a v deníku se podruhé objevilo „Dospěla“).

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
