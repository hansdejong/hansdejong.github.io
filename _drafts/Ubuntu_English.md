---
layout: post
title: Ubuntu_English
categories : [Programming, _OS, _draft]
tags : [installation, switch]
comments: true
---

This is an account of all what happened during my intended switch to Linux. This switch wasn't flawless. I'll mark in <font color="green">green</font> some remarks that maybe could help other users, and in <font color="red">red</font> some points where possibly Linux developers could pay some attention.

At home I mostly work on a rather old Vista-PC. I'm content about Vista in general, but it gets more and more sluggish over time. CCleaner is not enough of a remedy, the registry gets polluted by the installations and updates. So I foresaw that I would have to switch to a new computer, and a new Windows-version in short term.<br>
I don't envy that: Windows keeps getting more and more congested, it's expensive, you have to deal with licencechecks en -restrictions, and everything moves toward the cloud and privacy-constraints. Of course Linux is not free from that, but is seems to be a good alternative, and it is free of charge.

Vroeger heb ik me al wel eens verdiept in Unix, en er op m'n werk mee gewerkt. Ik heb Red-Hat Linux, en ook Ubuntu wel eens ge&iuml;nstalleerd en het een tijdje uitgeprobeerd. Mijn computer was al een dual boot. Ik besloot de Linux-draad weer eens op te pakken.

<hr>

**Ubuntu 14.04**

Op de installatie een maand of wat geleden van Ubuntu&nbsp;14.04&nbsp;LTS wil ik niet te diep ingaan. (LTS staat voor "long term support", de hoofdversies met een vijf-jarige ondersteuning. Er zijn ook tussenversies, overeenkomend met het jaar van uitkomen.) Dat ging redelijk voorspoedig. Ook had ik geen data van belang onder Linux, dus konden de betreffende partities gewoon worden geformatteerd.<br>
Linux (en dus Ubuntu) vergt meer kennis dan windows, dus was ik bereid daarin te investeren. Ik heb verschillende Linux boeken, en ik heb de <font color="green">(zeer aan te bevelen)</font> MOOC
<a href ="https://www.edx.org/course/introduction-linux-linuxfoundationx-lfs101x-0" target="_blank">Introduction to Linux</a> gedaan om mijn kennis op te frissen.

Het idee was langzamerhand de belangrijkste activiteiten naar Ubuntu te verhuizen. Mijn experimenten met Scala (Scala-Ide in Eclipse) deed ik nu onder Ubuntu, zaken als Git (met Git-gui en gitk) werkten prima. Bestanden onder Windows waren vanuit Linux gewoon te benaderen <font color="green">(en te wissen. Kijk dus erg uit met het <b>rm</b>-commando. Er is een optie, <b>--one-file-system</b>, om het effect tot &eacute;&eacute;n systeem te beperken)</font>. Sommige konden worden gesynchroniseerd (KeePass2). Ook bleek LibreOffice prima te voldoen: het leest MS-Word bestanden, en schrijft ze eventueel ook in dat formaat weg. GemistDownloader deed het. 

Alleen mijn vele macro's in VBA miste ik (Word2000-VBA gebruik ik als algemene scripttaal voor allerlei klusjes).
Mijn mail deed ik nog via Windows, Jekyll (dit blog) was nog niet aan de praat vanwege een vernachelde installatie van Ruby.

Maar de bottomline was dat ik zeer tevreden was over Ubuntu, alles draaide als een tierelier en binnenkort zou ik grotendeels "over" zijn. Ik was gelukkig.

<hr>

**Ubuntu 16.04.1 via update-manager**

Dit jaar was ook Ubuntu&nbsp;16.04&nbsp;LTS uitgekomen. Er werd aangeraden te wachten tot de offici&euml;le installer van Ubuntu er zou zijn, via de "update-manager". Daar gaat altijd enige tijd overheen, maar deze zou meer zekerheid bieden dan een .iso-imagebestand. Sommigen op internet waarschuwden dat het wel eens mis ging, volgens de meesten bleven de applicaties, data en instellingen gewoon behouden. 

Eind juli was het zover. Ik had intussen het volste vertrouwen in Ubuntu... en het ging mis. De downloadfase ging prima, maar de installatie strandde op zo'n 80%, na zo'n twee uur (vanaf de DVD ging het later veel sneller). Netjes Ubuntu afsluiten ging niet meer. Gelukkig was Vista nog te starten. <font color="green">Het is dus zeer aan te raden die Backup w&egrave;l te maken voor je aan dit soort avonturen begint.</font>

<hr>

**Recuperatie 1**

De eerste recuperatiepoging was via een opstart-USB met het intussen gedownloade imagebestand er op. Hoe ik de opstartvolgorde in de BIOS ook veranderde, opstarten lukte niet. Ik ben een tijdje aan het klooien geweest met een "plop boot-manager", maar die had vreselijk veel opties om een eigen versie te brouwen, dat heb ik opgegeven. Vervolgens een opstart Ubuntu live-DVD gemaakt. Daar kon ik wel van starten.

<hr>

**Recuperatie 2**

De eerste live-DVD poging ging niet goed. Met alle opties aangevinkt, mogelijke Ubuntu-upgrades binnenhalen, en meteen alle multimediabestanden etc., bleef het installatiescherm gewoon staan, zonder enige indicatie of er iets gebeurde. Aan het kiezen van de partities kwam ik niet eens toe. Op internet, via een tablet, bleken er mensen na een uur of negen toch succes te hebben, dus ik wachten (nou ja, slapen). Ook werd daar gesuggereerd dat er bij niet-hangende installaties reclamevideootjes worden getoond waar de hangende kennelijk niet tegen kunnen. Bij mij na elf uur nog steeds niets. <font color="red">Zou een voortgangsindicator en/of een scherm met wat er staat te gebeuren en hoeveel tijd er ongeveer voor staat een idee zijn?</font> Als gebruiker heb je geen idee wat normaal gedrag is, en ben je bang voor een corrupt systeem. 

<font color="green">Daarna heb ik alleen "kale" installaties gedaan, die je later moet aanvullen.</font> Nu lukte dat, en best snel. In de orde van ruim een kwartier, i.t.t. de eerdere uren.
Het systeem stond nu keurig op de partities waar eerder Ubuntu 14.04 had gestaan. In plaats van unity had ik nu de GNOME desktop. Het was even wennen, maar het zag er chique uit.

<font color="red">(Klein minpuntje: onder GNOME is het nog lastiger dan onder Unity icons (launchers) op je desktop te zetten: er is een listig verstopte boolean instelling waardoor ze standaard niet worden getoond. En dan heb je op Internetfora wijsneuzen die vinden dat je dat niet mag willen, want zo is het willens en wetens ontworpen. Daar heb je trouwens toch frequent reacties in de sfeer van zelfverklaarde guru's onder elkaar, die het alleen maar mooi vinden als iets moeilijk te vinden is.)</font><br>
Heel even wennen. Ineens begon Ubuntu bij het opstarten te zeuren over een verplichte fsck (een niet te omzeilen soort ChkDisk). Je krijgt een hoop onduidelijke opties voorgeschoteld over INodes die part zijn van een Orphan Linked List, en ander ongerief. Na enige tijd bleven de vragen uit en hing het systeem.<br>
<font color="red">Dat kun je gebruikers toch niet aandoen: geen enkele indicatie wat er aan de hand is (Is de schijf echt rot? Nooit gemerkt.), en wat daar dan op een veilige manier tegen te doen is. En  de user vragen voorschotelen over INodes waar geen mens van kan weten wanneer het slim is van de default af te wijken. </font>

<hr>

**Recuperatie 3**

Hierna was ook grub (het opstartprogrammaatje) corrupt. Ik kon niets meer starten, zelfs windows niet. Alleen opstarten vanaf de live-DVD werkte. 

Maar intussen had ik in ieder geval wel m'n data kunnen redden. /home/hans/, met alle Scala ge&euml;xperimenteer en m'n git- repositories naar de USB gekopieerd.

Die USB bleek later overigens Read-Only te zijn. Dat gold later ook voor een Ubutu partitie. <font color="red">Dat is iets waarvan ik niet als enige last heb, maar waar veel over geklaagd en gecorresponeerd wordt op internet, meestal door Ubuntu gebruikers.</font> Heel vervelend, met grote kans op dataverlies als je datgene wat je wilde redden opeens niet kwijt kunt.  

<hr>

Bij de volgende installatie durfde ik niets anders dan de default instellingen te gebruiken: het moest goed gaan, ik kon niet eens meer in Windows. De installatie lukte, en ook grub deed het weer. Alleen had Ubuntu nu een deel van een windows-schijf afgepakt in plaats van de eerder voor de dual-boot gereserveerde partities. 

<hr>

**Nog een installatie poging**

![schijven]({{ site.baseurl }}/assets/pictures/schijf.gif)

Omdat ik het toch wel zonde vond van de ruimte (een halve schijf, 450 GB voor een corrupte Ubuntu, en de werkende Ubuntu van 102 GB ten koste van Windows) heb ik Ubuntu nogmaals ge&iuml;nstalleerd, na formatteren van de corrupte partitie (met het idee het kleinere syteem later te verwijderen). De twee versies heb ik parallel ingericht volgens het Ubuntu-<a href="https://sites.google.com/site/computertip/directdoen" target="_blank">"10 dingen lijstje"</a>. 

Totdat: de fsck-vragen weer begonnen en de boel weer hing.<br> 
Zo is de situatie nu. Windows en het "SMALL"-systeem doen het gelukkig nog, maar het "LARGE"-systeem is weer onbenaderbaar.

<hr>

**Voorlopige conclusie**

Ik was echt heel enthousiast over Ubuntu, dus ik denk dat ik het nog niet opgeef. Misschien moet ik toch een ander systeem, met een gezondere schijf proberen.<br>
M'n vertrouwen is wel een beetje geknakt, evenals m'n uithoudingsvermogen. Ik heb een PC om te werken en te programmeren, en dan kun je niet die fsck's als een zwaard van Damocles voor zien te blijven. Daar heb het nu even mee gehad. 
