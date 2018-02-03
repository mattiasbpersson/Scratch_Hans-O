# Scratch - Bågskytten Hans-O

Hans-O (Hans-Olov) ska stå på en mur och försvara sig mot Mulle-vadarna som kommar fram ut sina hål och attackerar honom.
Kommer Mulle-vadarna fram till muren och slår på den så går den till slut sönder och Hans-O besegras. 
Så Hans-O ska kunna skjuta pilar på Mulle-vadarna som då försvinner.

Utveckling: https://scratch.mit.edu/users/Ratcher05/

Grafik: https://scratch.mit.edu/users/MaEk_Animations/

[Presentation (Google slides)](https://docs.google.com/presentation/d/1tH18PLq121Lf-I-n7h0owph1vQ9ijZxFO6_KBWH7MSA/edit?usp=sharing)

#### Innehållsförteckning
[Förberedelser](#förberedelser)  
[Ash](#ash)  
[Kasta besvärjelse](#kasta-besvärjelse)  
[Moorgerna kommer](#moorgerna-kommer)  
[Gravitation](#gravitation)  
[Extra saker](#extra-saker)  

## Förberedelser
* Hitta igen följande projekt och spara ner alla sprites i din ryggsäck: [https://scratch.mit.edu/projects/200419789/](https://scratch.mit.edu/projects/200419789/)
* Skapa ett nytt projekt. 
* Rensa bort katten.
* Skapa en bakgrund. 
Det viktiga är att muren är grå och gräset en annan:

![Background](images/ground.png "Bakgrund")

## Hans-Olof

### Lägg till Hans-Olof
Vi vill att Ash ska stå på marken då vi startar. Fötterna ska röra översidan av marken.

Flytta in Ash från ryggsäcken till ditt projekt

Ställ Ash på marken (dra ner Ash tills hen står på marken och titta vilken y-koordinat som då anges i fönstret):

* När flaggen trycks
* Gå till mitt på skärmen och i höjd med gräset (koordinaterna du såg innan)
* Gör spiten 2 ggr så stor (kanske inte behövs)
* Vänd spriten till höger

![Ash ground](images/ash_groundnew.png "Ash ground")

### Få Ash att glida vänster och höger
Vi gör så att Ash kan glida över skärmen.

* För alltid
  * Om man trycker på d-tangenten
    * Vänd dig till höger
    * Repetera tills man inte trycker d-tangenten
      * Gå 4 steg i riktningen (höger)
  * Om man trycker på a-tangenten
    * Samma som ovan, fast vänster

![Ash walk](images/ash_walk.png "Ash walk")

Vad hade hänt om man gjort så här:

![Ash walk](images/ash_walk2new.png "Ash walk")

### Animera Ash
Vi gör så att Ash ser ut att gå över skärmen 

* När flaggan trycks
* För alltid
  * Om man trycker på d-tangenten
    * Repetera tills man inte trycker d-tangenten
      * Vänta en kort stund
      * Ta nästa kostym
  * Om man trycker på a-tangenten
    * Samma som ovan
  * Byt till kostymen "stå"
  
![Ash walk](images/ash_walk_version1.png "Ash walk")

Vad blir skillnaden om man gör så här:

![Ash walk](images/ash_walk_version2.png "Ash walk")

## Kasta besvärjelse
### Förberedelser
Flytta in den besvärjelse du vill använda (hjärtat eller stjärnan) från ryggsäcken.


###Kasta besvärjelse version 1
När spelar trycker mellanslag så ska besvärjelse kastas mot muspekaren. Då besvärjelsen träffar kanten ska den försvinna
Se till att besvärjelsen alltid startar på samma plats som Ash och att den är gömd:

* När man trycker på flaggan, göm mig
* Då mellanslag trycks ner
  * Flytta mig dit där Ash står
  * Visa mig själv
  * Vrid mig så jag pekar mot muspekaren
  * Repetera tills jag träffar en kant
    * Flytta 10 steg i den riktning jag pekar åt
  * Göm mig då jag har träffat en kant

![Spell version 1](images/spell_version1.png "Spell version 1")

Problem: Det går bara att kasta en besvärjelse i taget!

###Kasta besvärjelse version 2
När spelar trycker mellanslag så ska en klon skapas av spriten.

* När mellanslag tangenten trycks ner
* Skapa en klon av mig själv
* Flytta mig till dit där Ash står


* Då jag startar som en klon
* Visa mig själv
* Repetera tills jag träffar kanten
  * Flytta 10 steg i den riktning jag pekar åt
* Ta bort mig själv (klonene)


* När man trycker på flaggan
* Ta bort alla kloner (rensa)

![Spell version 2](images/spell_version2_new.png "Spell version 2")

Problem: När vi trycker på mellanslag flera ggr blir det för många besvärjelser.

###Kasta besvärjelse version 3
När vi trycker mellanslag, kolla om vi är en klon innan vi skapar en klon.

Skapa en variabel som heter "is clone". Som gäller för bara denna sprite.

* När man trycker på flaggan
* Sätt variablen "is clone" till "no"


* När man trycker på spange-tangenten
* Om variablen "is clone" är "no"
  * Samma som innan
  
  
* När jag startar som en klon
* Sätt variablen "is clone" till "yes"
* Samma som innan


![Spell version 3](images/spell_version3_new.png "Spell version 3")

## Moorgerna kommer
### Förberedelser
Lägg in Moorgen i ditt projekt. Den som ser ut att ligga på marken.

Visa sen en Moorg så du ser hur den ser ut och att den rör sig som den ska. 
Det här är i princip samma sak som vi gjorde då vi la till Ash

![Moorg Start](images/moorg_start.png "Moorg start")

### Slumpmässig Moorg
Se till att det skapas en ny klon  vid slumpmässigt tillfälle

* När man trycker på flaggan
* Göm mig själv
* För alltid
  * Vänta ett slumptal antal sekunder (1-10)
  * Skapa en klon av mig själv

![Moorg Random](images/moorg_random.png "Moorg random")

### Moorg kommer version 1
Se till att Moorger kommer från vänster och attackerar.

* När jag startar som en klon. 
* Visa mig och lägg mig på i kanten på skärmen i höjd med marken. 
* Se till så att jag pekar in mot mitten av skärmen.
* Tills jag träffar Ash eller jag blir träffad av ett hjärta - repetera:
  * Flytta 10 steg i den riktning du pekar (mot mitten)
  * Repetera 4 ggr 
    * Nästa kostym
    * Vänta kort stund
  * Om vi träffar kanten, byt riktning
* Ta bort klonen
  
![Moorg walk 1](images/moorg_move_version1.png "Moorg walk 1")

### Moorg kommer version 2
Vi vill att det ska komma Moorger från både höger och vänster.

* Välj ett slumpmässigt tal mellan 1 och 2. 
* Om det är 1, gör som vi gjorde innan.
* Om det är 2, se till att jag hamnar vid andra kanten och pekar mot mitten.

![Moorg walk 2](images/moorg_move_version2.png "Moorg walk 2")


### Moorg kommer version 3
DRY - Don't repeat yourselves. (Refaktorering)

Har man samma kod på flera ställen är det lättare att göra fel.

Flytta de delar som är lika i ett eget block.

* Skapa ett nytt block som heter MooveMoorg
* Flytta in allt från "repeat until"/"repetera till" i definitionen av det nya blocket.
* Lägg till det nya blocket.

![Moorg walk block](images/moorg_move_block.png "Moorg walk block")

![Moorg walk 3](images/moorg_move_version3.png "Moorg walk 3")

## Gravitation
Vi vill göra så att Ash ska kunna hoppa. 


###Gravitations block
Skapa en ny variabel som heter "speedy"

* När flaggan trycks
* För alltid
  * Ändry y-positionen med speedy
  * Minska hastigheten med 1
  * Repetera tills vi inte rör vid marken
    * Öka y-värdet med 1
    * Sätt hastigheten till 0

![Gravitation](images/block_gravitation.png "Gravitation")
 
Ändra start positionen för Ash till 0,0. Vad händer? 
 
###Hoppa

* När w-tangenten trycks
* Sätt hastighen (speedy) till 12

![Ash hoppa](images/ash_jump.png "Ash hoppa")
 

## Lägg till livspoäng
Vi vill att spelat slutar om man träffas av 3 Moorger.

I Ash spriten, skapa en ny variabel som heter HP (för alla sprites).

* När vi trycker på flaggan
* Sätt HP värdet till 3
* För alltid:
  * Om vi rör vid MoorgWalk-spriten
    * Ändra HP värdet med -1
    * Vänta 0.5 sek
  * Om HP är noll
    * För alltid
    * Stoppa allt

![Moorg walk 3](images/ash_hp_version2.png "Moorg walk 3")
 
### Extra saker
* En "Game Over" skärm
* Cooldown på spells
* Flygande Moorger
* Kasta olika spells.
* Ash besvärjelser ska falla mot marken då de kastas.
* Ändra så att man inte kan hoppa hela tiden (kanske bara dubbel-hopp).
* Moorgerna vänder om de träffas av Love.



 









