---
title: Eagle cheat sheet
autor: Matyáš Vaňhát
date: 2023-02-02 12:00
categories: [Knihy, NeFikce, Elektřina]
tags: [elektřina, eagle, tipy]
toc: true
img_path: /img/eagle/
---


>🔗 Dělat vše ve vrstvě 16
{: .prompt-tip }

1. View - odškrtat dolní políčka
    
    ![Desktop](Untitled6.png)
    
2. View - Grid → mm, ale defaultní hodnoty
    
    ![Desktop](Untitled1.png)
    
3. Odpory, kondenzátory a cívky hledat v **rcl →** používat evropské značky (odpory ⇒ 0207) → za lomítkem 10

    ![Desktop](Untitled2.png)

1. Když nemůžu najít součástku, za název dám *****
2. Některé IO nemají NAPÁJENÍ→ PAK → INVOKE → PWR→ Objeví se piny pro napájení
    
>Když součástka nemá napájení, kliknu na Properties → Infoservis
{: .prompt-tip }
    
3. Základní svorkovníce → Ak300/počet pinů, který je nutný zadat — modrá se šroubky
4. PAD - čistá ploška
5. PIN - klasický hřebenový PIN
6. Propojovat vždy pomocí **NET**
    
    ![Desktop](Untitled3.png)
    
7. Nezapomínat na GND
8. Polygon → lepší plošňák → méně frézování
9. Po zhotovení schématu dám generate/switch to board (zelená nahoře) 
    
    ![Desktop](Untitled4.png)
    
10. Zase vypnout políčko jako v bodě **[1.]**
11. Grid → mm → default
12. Edit → design rules → load → pravidla pro frézování (E33 → název frézky) — pro školní frézku
13. Umístím součástky na plošňák
14. Ve vlastnostech upravím souřadnice na celá čísla (vypadá to pak lépe)
15. Žluté čáry odpovádají propojům
16. Ratsnest - je dobré na to kliknout po umístění součástek do boardu 
    
    ![Desktop](Untitled5.png)
    
17. Jak nastavit polygon
18. Route Airwire a propojím natvrdo kontakty
19. Když se mi kříží cesty, musím udělat “tunel” na druhou stranu - v top vrstvě propojit - přidat body **Via** v buttom vrstvě
20. Polygon tlačítko, obkleslím si schema, signál dám na GND - může vyhodit chybu pokud ji vynutí, klinu na “name” v nástrojích nalevo→ klknu pravým tlačítkem myši na hranu polygonu a název změním na signál, který chci jako polygon (většinou GND)
21. Vlastnostni polygonu → Isolate → dát nejméně 0,4mm - ideálně 1.0 nebo 0.8 podle tloušťky frézky
22. Vždy vložit text na desku (tlač. text) → font → vektor → vel. písma 1,8 a více