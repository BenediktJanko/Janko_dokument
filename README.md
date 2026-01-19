# Counter-Strike 1.6 a Half-Life Dokumentace 

V této dokumentaci se budu převážně zaobírat původem hry Counter-Strike 1.6 a jak tahle legendární hra vznikla  

## Úvod do Counter-Strike 1.6 

Counter-Strike je taktická first-person střílečka (FPS), ve které proti sobě bojují dva týmy -- teroristé a protiteroristé.  

Hra se zaměřuje na týmovou strategii, ekonomii a realistické zbraně.  

Verze 1.6 je nejznámější a nejoblíbenější historická verze, která se stala standardem pro kompetitivní hraní a esport po mnoho let. 

## Historie a vývoj hry 

### Původní koncept: 

Counter-Strike vznikl jako modifikace (mód) pro hru Half-Life. Tento mód vytvořili Minh „Gooseman“ Le a Jess Cliffe v roce 1999. První veřejná beta verze byla vydána 19. června 1999. 

Verze 1.6 byla finální opravou a balíčkem všech předchozích úprav, který obsahoval stabilní síťový kód, mapy a herní mechaniky, které hráči znali desetiletí. 

 

##Technologie a programování 

Herní engine: 

Counter-Strike 1.6 běží na herním enginu GoldSrc, což je silně upravený engine původně založený na Quake engine od id Software. 

Engine GoldSrc byl použit původně pro Half-Life a následně i pro CS a další tituly Valve. 

Programovací jazyky: 

GoldSrc engine a samotná hra jsou napsány především v jazycích C++ a C. 

Vývojáři a SDK: 

Modifikace CS využívá Half-Life Software Development Kit (SDK), který poskytuje nástroje pro úpravy kódu i mapování. 

 

Herní mechanismy a systémy 

Ekonomický systém: 

Hráči získávají peníze za zabití, dokončení úkolů a výhru kola. Peníze se používají k nákupu zbraní a vybavení na začátku kol. Tento systém zvyšuje hloubku strategie hry.  

Multiplayer a netcode: 

Síťový kód GoldSrc byl optimalizován tak, aby fungoval při různých pingech(PING = Rychlost Odezvy Serveru), což umožnilo plynulé online hraní i na starších připojeních.  

 

Mapy a design 

Mapy ve CS jsou navrženy tak, aby: 

-měly výchozí body týmů, 

-obsahovaly strategické body boje, 

-podporovaly taktické postupy. 

Mapy se vytvářejí pomocí Valve Hammer Editor a dalších nástrojů ze SDK.  

 

Komunitní modifikace: 

Existuje mnoho fanouškovských módů a projektů, které si hru přizpůsobily. Jedním z nich je např. CSPromod / Counter-Strike Professional Mod (založený na Source enginu, s mechanic podobnými 1.6). 

Quake Engine → GoldSrc 

Half-Life byl postaven na silně upraveném Quake Engine (Quake Engine byl technický základ moderních 3D FPS her). 

Valve tento engine licencovalo a postupně zcela přepsalo velké části kódu. Výsledkem byl engine zvaný GoldSrc. 

Důležité změny oproti původnímu Quake enginu: 

-podpora skeletových animací (ne jen vertex animací) 

-komplexnější fyzika objektů 

-skriptované události (cutscény bez přerušení hry) 

-vylepšený síťového kódu 

GoldSrc nebyl jen „upravený Quake“, ale prakticky nový engine, který s Quakem sdílel jen základní architekturu. 

 

Programovací jazyky a nástroje 

Použité jazyky: 

Vývoj Half-Life i Counter-Strike probíhal hlavně v: 

-C++ – hlavní herní logika, engine, AI, zbraně 

-C – nízkoúrovňové části enginu 

-Assembler – výkonově kritické části (síť, rendering) 

-Skriptovací jazyk enginu – pro mapové události 

Žádný moderní engine, žádný Blueprint, žádný Unity. 
Vše bylo ručně psané. 

 

Half-Life SDK 

Valve vydalo Half-Life SDK, které umožňovalo psát vlastní herní logiku, uprovovat chvoání zbraní, vytvářet nové entity, měnit multiplayerová pravidla. 

SDK obsahovalo: Zdrojové kódy herních DLL, hlavičkové soubory, dokumentaci k enginu. 

Counter-Strike vznikl výhradně pomocí tohoto SDK. 

 

Jak se programoval Half-Life 

Architektura hry 

Half-Life byl rozdělen do několika vrstev: 

Engine (core): 

-Renderování, fyzika, síťová komunikace, správa paměti. 

Game DLL: 

-Nepřátelé, zbraně, hráč, herní pravidla. 

 

To znamená, že engine zůstal stejný, ale hra samotná byla samostatná knihovna. 

 

AI nepřátel (revoluce v době vydání) 

Half-Life měl pokročilou AI, která: 

-Komunikovala mezi NPC, reagovala na zvuk kryla se, obcházela hráče. 

 

Každý nepřítel měl: 

-Paměť poslední pozice hráče, rozhodovací logiku, skripty chování. 

 

 

 

Skriptované sekvence 

Valve vytvořilo systém skriptovaných událostí, aby hra působila filmově: 

-NPC se pohybují,  mluví, aktivují objekty. 

To byl obrovský technický problém, protože: 

-Hráč mohl událost přerušit, engine musel reagovat dynamicky. 

 

Valve strávilo roky laděním chyb, kdy se NPC „zasekli“ nebo rozbili skript. 

 

 

Programování multiplayeru a síťového kódu 

Klient–server model: 

Counter-Strike používal: 

-Dedikovaný server a klienty jako „hloupé terminály“ 

Server rozhodoval: 

-Kdo byl zasažen, kdo zemřel, kdy kolo skončí. 

To bylo zásadní pro omezení cheatů. 

 

Problémy se sítí 

V roce 1999–2003: 

-dial-up připojení, vysoký ping, packet loss. 

 

Valve řešilo: 

-Client-side prediction, lag compensation, interpolaci pohybu, CS 1.6 byl vrchol optimalizace GoldSrc netcode. 

 

 

Programování zbraní 

Každá zbraň měla: 

-Vlastní třídu v C++ 

-Parametry: Damage, recoil pattern, přesnost, kadenci, pohybovou penalizaci. 

Recoil nebyl náhodný: 

-Byl deterministický, založený na předem definovaných hodnotách 

Díky tomu vznikl skill-based gameplay. 

 

Vývojové problémy a chyby 

Technická omezení: 

-Max. 32 hráčů, limit polygonů, limit paměti (32bit). 

Bugy: 

-Hitboxy neseděly s animací, exploity map, desynchronizace klient/server. 

Valve opravovali chyby roky. Některé bugy se staly „feature“ (např. bunny hop) 

 

 

 

Přechod od modu ke komerční hře 

Valve: 

-Odkoupilo práva, aměstnalo Minh Le a Jess Cliffe, přepsalo části kódu, přidalo anti-cheat, zaměstnalo Minh Le a Jess Cliffe. 

CS 1.6 byl: 

-Finální stabilní verze GoldSrc, technologický vrchol enginu 

 

Závěr 

Counter-Strike 1.6 není jen hra — je to fenomén, který změnil online multiplayer ságy, inspiroval esport i mnoho dalších her. Jeho jednoduchá, ale hluboká mechanika, spolu s podporou komunity, zajistila dlouhověkost, která trvá více než dvě dekády.  

 

Projekt ještě není dodělaný!  

Zdroje: ChatGPT, Wikipedie, Google 

Tvůrce: Benedikt Janko 

 
