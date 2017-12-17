# Arboreal
Tommy Kärnström FEND17<br/>
Individuell examination 1<br/>
Sidan är live på GitHub Pages. Klicka här.
> Startup-företaget Arboreal behöver en ny hemsida för sin affärsidé.<br/>
> Skapa denna sida.

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
- Göra om telefon nummer till länk så att man kan ringa vanliga samtal eller skype samtal när man klickar på den.
-  Du skulle kunna ha tel, facebook och twitter i din footer istället för att ha en extra navigations bar som du inte har en användning utav.
- Om det är en css varning som är möjlig att bli av med, du kanske skulle kunna göra det.

## Svar på Feedback



## Breakpoints


## Fallback

### \@support
Man önskar att supporten för \@support var bättre speciellt för webbläsare som ie9 och tidigare men så är inte fallet. Den känns ganska menigslös i många lägen speciellt om man kollar på supporten för t.ex. flexbox och rem som har bättre support än support.

Jag kan tänka mig att den i framtiden när t.ex. flex börjar anses gammalt kan vara väldigt användbar, men just nu ser jag inte riktigt hur den skulle användas. Det är kanske därför man inte ser eller hör talas om det så mycket?

### ie9, ie8 och tidigare
Jag har kunnat testa sidan och det funkar utan problem på IE10, den funkar även utan några större problem på IE9 men man märker att supporten för flexbox är nästan icke existerande. Det är ingenting som inte går att fixa med fallbacks.

IE8 är där allt går sönder, supporten för allt eller iallfall det mesta är lika med 0.

### Semantisk HTML
Fallbacken för semantisk html är inte bra och det går inte att använda på äldre webbläsare därför valde jag att använda `div` istället. IE8 supportar det inte alls och det går därför inte att styla någonting och IE9-11 supportar det till viss del.
