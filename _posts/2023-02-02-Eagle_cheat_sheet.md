---
title: Eagle cheat sheet
autor: Matyáš Vaňhát
date: 2023-02-02 10:00
categories: [Elektřina]
tags: [elektřina, eagle, tipy]
toc: true
img_path: /img/eagle/
---


>Dělat vše ve vrstvě 16
{: .prompt-warning }

1. View - odškrtat dolní políčka
    
    ![Desktop](Untitled6.png){: width=50% height=50% .w-75 .normal}
    
2. View - Grid → mm, ale defaultní hodnoty
    
    ![Desktop](Untitled1.png){: width=50% height=50% .w-75 .normal}
    
3. Odpory, kondenzátory a cívky hledat v **rcl →** používat evropské značky (odpory ⇒ 0207) → za lomítkem 10

    ![Desktop](Untitled2.png){: width=50% height=50% .w-75 .normal}

4. Klasická tlačítka jsou v switch_omron. Zbytek hledáním switch*
5. Když nemůžu najít součástku, za název dám *****
6. Některé IO nemají NAPÁJENÍ→ PAK → INVOKE → PWR→ Objeví se piny pro napájení
    
>Když součástka nemá napájení, kliknu na Properties → Infoservis
{: .prompt-tip }
    
7. Základní svorkovníce → Ak300/počet pinů, který je nutný zadat — modrá se šroubky
8. PAD - čistá ploška
9. PIN - klasický hřebenový PIN
10. Propojovat vždy pomocí **NET**
    
    ![Desktop](Untitled3.png){: width=50% height=50% .w-75 .normal}
    
11. Nezapomínat na GND
12. Polygon → lepší plošňák → méně frézování
13. Po zhotovení schématu dám generate/switch to board (zelená nahoře) 
    
    ![Desktop](Untitled4.png){:.w-50 .right}
    
14. Zase vypnout políčko jako v bodě **[1.]**
15. Grid → mm → default
16. Edit → design rules → load → pravidla pro frézování (E33 → název frézky) — pro školní frézku
17. Umístím součástky na plošňák
18. Ve vlastnostech upravím souřadnice na celá čísla (vypadá to pak lépe)
19. Žluté čáry odpovádají propojům
20. Ratsnest - je dobré na to kliknout po umístění součástek do boardu 
    
    ![Desktop](Untitled5.png){:.w-50 .right}
    
21. Jak nastavit polygon
22. Route Airwire a propojím natvrdo kontakty
23. Když se mi kříží cesty, musím udělat “tunel” na druhou stranu - v top vrstvě propojit - přidat body **Via** v buttom vrstvě
24. Polygon tlačítko pro uzemnění nevyužitých částí PCB -> obkleslím si schema, signál dám na GND - může vyhodit chybu pokud ji vynutí, klinu na “name” v nástrojích nalevo→ klknu pravým tlačítkem myši na hranu polygonu a název změním na signál, který chci jako polygon (většinou GND)
25. Vlastnostni polygonu → Isolate → dát nejméně 0,4mm - ideálně 1.0 nebo 0.8 podle tloušťky frézky
26. Vždy vložit text na desku (tlač. text) → font → vektor → vel. písma 1,8 a více