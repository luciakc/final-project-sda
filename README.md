# final-project-sda
Software Tester Course SDA - Final Project

TESTOVACÍ PLÁN PRE WEBOVÚ APLIKÁCIU
PETSTORE.OCTOPERF.COM
https://petstore.octoperf.com/actions/Catalog.action

1. ÚVOD

1.1. Účel

Účelom tohto dokumentu je plán komplexného testovania demo webstránky JPetStore (https://petstore.octoperf.com/actions/Catalog.action) v rámci finálneho projektu kurzu Software Tester poskytovaného spoločnosťou Software Development Academy (https://sdacademy.cz/).
	
Na testovaní sa podieľal tím testerov: Alica Tothová, Lucia Čurma, Marek Kovaľ, Oľga Matoušková, Yeldana Sadyková

Testovaná webstránka predstavuje demo verziu e-shopu so zvieratami s napohľad jednoduchou navigáciou, kde v záhlaví stránky môže užívateľ nájsť odkaz na nákupný košík a prihlásenie, rovnako ako aj možnosť vyhľadávania. V tele stránky sa nachádza hlavný navigačný panel s odkazmi na jednotlivé podkategórie (akvaristika, psy, teraristika, mačky a vtáky). V záhlaví stránky možno nájsť len odkaz na komunitnú webstránku.

V rámci inicializačnej fázy si testeri vymädzili predmet testovania  a identifikovali jeho priority. Vytvorili si cloudový dokument pre mapovanie postupu testovania všetkých členov tímu, taktiež komunikačný kanál na platforme Slack, projekt vo webovej aplikácii Jira na sledovanie pokroku plnenia úloh, TestRail na zaznamenávanie testovacích prípadov a Trello board na dokumentáciu nájdených defektov. 

2. Osnova

Pri koncipovaní osnovy pre postup testovania bola testovaná webstránka rozdelená na jednotlivé časti podľa dôležitosti z pohľadu koncového užívateľa, ktoré boli v tomto ohľade zoradené nasledovne:

Obr. 1 Jednoduchá osnova

Následne boli jednotlivé celky rozpísané na konkrétne testovacie scenáre, ktoré budú ďalej spracované v podobe testovacích prípadov.
	
2.1. Registrácia
Ako celok s najvyššou prioritou si testeri zvolili registráciu užívateľa, ktorá predstavuje prvý krok pre úspešné vykonanie objednávky a bez nej nie je možné na testovanej webstránke, okrem prezerania dostupných položiek, nič robiť.

Hlavným cieľom testovania registračného formuláru je analýza spracovávania a vyhodnotenie validácie vstupných dát a ich archivácia v databáze webstránky. V rámci tejto časti bude využité manuálne testovanie, ako aj automatické testovanie registračného formuláru pomocou nástroja Selenium.

Obr. 2 Rozvetvená osnova
	
2.2. Nákup 
Druhú prioritu dostal obsiahly celok nákupu v jeho kompletnej podobe od vloženia prvej položky do nákupného košíka až po kompletizáciu objednávky a zaplatenie. Predmetom testovania budú okrem iného aj bežné úkony koncového užívateľa v podobe stornovania či reklamovania objednávky. V rámci tejto časti bude využité manuálne testovanie. Z možných techník testovania budú využívané najmä techniky testovania založené na skúsenostiach, a to odhadovanie chýb, prieskumné testovanie a revízia založená na kontrolných zoznamoch.

2.3. Responzivita
Tretiu prioritu dostalo testovanie responzivity webovej stránky, dôležitého faktora pri zlepšovaní používateľskej skúsenosti. Je nesporným faktom, že návštevnosť webových stránok, pokiaľ ide o použité zariadenie, sa za posledné desaťročie výrazne zmenila.

Ako možno vidieť na nižšie uvedenom grafe (https://www.broadbandsearch.net/blog/mobile-desktop-internet-usage-statistics), na konci roka 2021 dosiahla návštevnosť webových stránok z mobilných zariadení až 56%, a preto bude webová stránka JPetStore testovaná aj z hľadiska prístupu z rôznych zariadení, operačných systémov či internetových prehliadačov.

V rámci testovania responzivity budú vykonané taktiež testy a analýza výkonnosti a optimalizácie webstránky.	

2.4. Obsah

Ako už napovedá názov tejto časti, v rámci tohto celku sa bude testovať samotný obsah webovej stránky, jej konzistentnosť a zjednotenosť prevedenia, tzv ‘look and feel’, a správne prepojenie jednotlivých stránok odkazmi.

Testovaná webová stránka má napohľad jednoduchú navigáciu, z pohľadu koncového užívateľa však možno pri prezeraní si jednotlivých kategórií na stránke naraziť hneď na niekoľko problémov.

Ako v prípade mnohých webových stránok, testovanú stránku možno rozdeliť na hlavičku, telo a pätu. Pokiaľ ide o hlavičku, jediný otáznik vyvstáva pri umiestnení menu pozostávajúceho z ikon pre nákupný košík, prihlásenie a informácie do stredu, čo môže pôsobiť rušivo a odvádzať pozornosť od zobrazovaných položiek nižšie v tele stránky.

V tele stránky sa nachádza hlavný navigačný panel s odkazmi na kategórie ponúkaných zvierat. Tieto odkazy sa nachádzajú tak na ľavej strane, v strede a rovnako aj v hornej časti tela stránky. Výraznejší stredný panel s obrázkami zvierat a ľavý panel po kliknutí na jeden z odkazov miznú a zostáva len ten najmenší a najnevýraznejší. Pri preklikávaní na jednotlivé položky sa možno ľahko stratiť v neprehľadnosti na seba nadväzujúcich odkazov. Jednoduchým riešením tohto problému by mohlo byť ‘breadcrumbs’ menu, ktoré by užívateľovi umožnilo vrátiť sa na požadovanú úroveň a pokračovať v prezeraní.

2.5. Vyhľadávanie 

V tomto bode bude testovaniu podliehať funkcia interného vyhľadávania v rámci testovanej stránky. Podľa Econsultancy (https://econsultancy.com/) vyhľadávanie na stránkach prináša až 14% celkového obratu, čo znamená, že zlá skúsenosť s touto funkcionalitou ovplyvní konečný výsledok. Vyhľadávanie na webe by preto nemalo predstavovať len ‘zadné dvierka’. Optimalizované a plne funkčné interné vyhľadávanie môže spoločnosti poskytnúť významné výhody a ovplyvniť výnosy.

3. NÁSTROJE

Ako už bolo spomenuté v úvode tohto dokumentu, v priebehu projektu boli využité rôzne nástroje.

3.1. Excel

Jadro projektu bolo vytvorené pomocou Excel tabuľky v cloudovom úložisku, kde bola zapísaná osnova, simulované testovacie dáta, kompletný zoznam testovacích prípadov a ich vypracovanie, zistené defekty a zoznam a kontaktné údaje testerov.

3.2. Jira

S cieľom simulácie reálnej situácie bol vytvorený projekt v Jire pod názvom PetStore. K projektu bola pripojená súkromná skupina na Slacku. Na základe pripravenej osnovy bol vytvorený zoznam ‘user stories’. Nasledovalo vytvorenie siedmich hlavných epicov, počínajúc prípravou až po vytvorenie dokumentácie k projektu. K jednotlivým epicom boli priradené ‘story pointy’ podľa odhadovanej náročnosti jednotlivých tém a testovacích prípadov. Po rozvrhnutí obsahu do jednotlivých epicov boli nasimulované sprinty, každý s trvaním jedného týždňa a náplňou jedného epicu. Záverečný sprint je venovaný vyhodnoteniu, nápadom, featurám a doplneniu dokumentácie.
	
3.3. Trello

Trello bolo využité na vizualizáciu ďalšieho spôsobu zaznamenávania testovacích prípadov a reportovanie zistených defektov na testovanej stránke. 

3.4. TestRail

Niektoré testovacie prípady boli napísané na platforme TestRail pre znázornenie ďalšej alternatívy v rámci manažmentu testov. 

3.5. Selenium

Pomocou nástroja Selenium IDE bol testovaný registračný formulár stránky.  Selenium WebDriver bol použitý na otestovanie prihlásenia registrovaného užívateľa. Obidva testy prebehli úspešne.

3.6. Performance testy

Vykonaných bolo niekoľko analýz rýchlosti načítania a výkonnosti testovanej stránky vrátane prístupu z mobilných zariadení. Okrem nižšie uvedenej analýzy Lighthouse report bol vykonaný test cez GTmetrix a PageSpeed Insights.
