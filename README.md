# Arboreal
Tommy Kärnström FEND17<br/>
Individuell examination 1<br/>
Sidan finns på [Github Pages](https://tomkaar.github.io/Arboreal/).
> Startup-företaget Arboreal behöver en ny hemsida för sin affärsidé. Skapa denna sida.

> Arboreal är en prenumerationstjänst för företag. Tjänsten innebär att man får sitt kontor inrett med växter med hjälp av experter från Arboreal. Sedan betalar man en månadskostnad för att få nya växter levererade och placerade på kontoret varje månad eller vecka beroende på vilken prisplan man har valt. Arboreal har sin kundgrupp bland små till medelstora IT-företag i stockholmsområdet.

## Output från HTML Validering
> "Document checking completed. No errors or warnings to show.""

## Output från CSS Validering
### Warnings
> "Imported style sheets are not checked in direct input and file upload modes"<br>
Detta är från att ha laddat typsnitt från Google Fonts med import metoden.

### Errors
> "This document validates as CSS level 3!"

## Feedback
1. Om möjligt försöka förkorta din css.
2. Göra om telefon nummer till länk så att man kan ringa vanliga samtal eller skype samtal när man klickar på den.
3.  Du skulle kunna ha tel, facebook och twitter i din footer istället för att ha en extra navigations bar som du inte har en användning utav.
4. Om det är en css varning som är möjlig att bli av med, du kanske skulle kunna göra det.

## Svar på Feedback
1. Ja, det fanns upprepningar i CSS och jag kunde skapa nya klasser för att minska koden.
2. Det har var en väldigt bra ide, ska definitivt se till att göra det!
3. Håller med till 50%. Det kan ses som onödigt att ha en likadan navigations meny i botten av sidan, speciellt då samma meny är sitter fast i toppen när man skrollar. Men jag vill inte ta bort den då den på mindre enheter ex. mobiler fyller en funktion. Skulle kunna kolla på att ändra innehållet i footern men jag tänker inte flytta tel och sociala medier loggorna från kontakt sektionen, de hör hemma där.
4. Jag kunde har varit mer tydlig och förklarat var varningen betyder. Det den säger är att den inte kommer att den inte kommer att validera innehållet i den länk jag länkat till. Det är en varning som inte riktigt går att få bort om jag vill använda Google Fonts.


## Breakpoints
Jag valde ha använda mig av två breakpoints, 1000px och 768px.

### 1000px
Den här Breaking pointen är endast till för att ändra style på två sektioner på sidan, "Themes" och "Price". Texten började vid denna punkt att flyta ut och ta mycket plats och layouten började långsamt att ändras och såg inte längre bra ut. Jag ville inte vänta tills 768px, vilket är min huvud Breakpointen på den här sidan men det hade inte sett klokt ut.

### 768px
Det här är min huvud Breakpoint där man går från Desktop till Tablet/ Mobil. Här ändras layouten totalt och anpassas till mindre enheter. Menyn blir till en Hamburgemeny som man måste klicka på för att öppna istället.

## Responsivt Mönster
Jag använder en blandning mellan Tiny Tweak och Mostly Fluid. För naviagatinoen använder jag min egen version av Overlay.


## Fallback

### \@support
Man önskar att supporten för \@support var bättre speciellt för webbläsare som IE som faktigst behöver den. Jag kände inte att jag behövde använda mig av den så mycket. Men den var ganska trevlig och lätt att använda, kan defenetivt tänka mig att den kan komma till större användning senare.

Problemet jag har med det när jag kollar på \@support är att supporten för ex. Flexbox och rem är större än supporten för \@support. IE 9 och 10 supportat t.ex. dessa två men inte support. Att använda \@support för flexfox känns därför väldigt onödigt då den tar bort funktioner man faktigst kan använda.

### IE10 och IE9
Jag har testa sidan och det funkar utan problem på IE10, den funkar även utan några större problem.

Internet Explorer har ett problem med att använda `background-attatchment: fixed;` som jag använder på parallax scrolling effekten ovanför "Pricing" sektionen. När man scrollar hoppar bakgrundsbilden vilket är väldigt jobbigt när man besöker sidan.

På IE8 och tidigare använde jag conditional stylesheets för att endast stänga av den effekten på alla browsers som är IE9 och tidigare. På IE10 finns det inga conditional stylesheets men jag hittade ett 'hack' för att få samma resultat. Detta stänger av allting på IE9 och IE10. [Länk](https://www.impressivewebs.com/ie10-css-hacks/)

<code>
@media screen and (min-width:0\0)
</code>

### IE8 och tidigare
På IE8 är supporten för allt eller iallfall det mesta är lika med 0. När jag kodade använde jag float som bas och eftersom den inte kan använda sig av flexbox kommer den ignorera allt som har med flex att göra.

Sidan ser lite annorlunda ut, iallafall om man kollar på 'Themes' delen. Bilderna och texterna ligger under varrandra och detta var ett medvetet val, på mindre enheter vill man att de går varannan, bild text bild text men inte på större enheter. Om jag är på en mindre enhet så jag fortfarande att det ska se bra ut (bild text bild text) inte ha bild text text bild. Därför valde jag att använda `order` för att byta plats på dem på större skärmar.

### Semantisk HTML
Använde [HTML5Shiv](https://github.com/aFarkas/html5shiv) för att kunna använda Semantisk HTML på äldre webbläsare.
